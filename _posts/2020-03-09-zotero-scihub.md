---
layout: post
title: Zotero搭配Sci-Hub，真香！
date: 2020-03-08 23:1:00
tags: 
- Zotero
published: true
---

由于之前在推文[更新版｜Zotero搭配Sci-Hub，真香！](https://mp.weixin.qq.com/s/QMSG24tgn4z8ShfE9pVYMg)中使用的Sci-Hub的`.se`近期挂掉了，因此有必要对本文进行更新下。

目前（截止2020.04.15），可用的Sci-Hub域名有以下几个：

- [https://sci-hub.tw](https://sci-hub.tw/)
- [https://sci-hub.ren](https://sci-hub.ren/)
- [https://sci-hub.si](https://sci-hub.si/)
- [https://sci-hub.shop](https://sci-hub.shop/)

如果你想及时获取Sci-Hub最新可用网址，可以到[青柠学术的GitHub网站](https://iseex.github.io/scihub/ "Sci-Hub最新可用网址查询")查看，我已经帮大家汇总好了。

我近期在Zotero中使用的是`.ren`域名，理论上以上四个都可以使用，大家可以自行更换为其中一个。

顺便把我的完整代码贴出来：

```
{
    "name":"Sci-Hub",
    "method":"GET",
    "url":"https://sci-hub.ren/{doi}",
    "mode":"html",
    "selector":"#pdf",
    "attribute":"src",
    "automatic":true
}
```

这里再提醒一下：

> 如果你没有使用任何代理，由于网络环境问题，可能会有少部分从Sci-Hub下载的PDF出现损害的情况，这时你可以考虑将上述代码中的`https`改为`http`，或者更换其他可用的域名，情况可能会好转。另外，可以逛逛本文在[知乎的评论区](https://zhuanlan.zhihu.com/p/112141757 "Zotero + Sci-Hub知乎评论区")，讨论的人还蛮多，说不从会有其他网友贡献更多好的办法。

除了改动部分，以下内容保持和之前的一致。👇

---

Sci-Hub有多香大家都知道！

Zotero有多香，你看了我的教程就知道了！👇

[Zotero ，打造最佳文献生态（合集）](https://mp.weixin.qq.com/s/V6nIE24UefJWi3HbydccaA)

那要是Zotero+Sci-Hub，岂不是无敌了！

今天就教大家在Zotero内集成Sci-Hub，实现在Zotero中免费下载99%的文献！

### 从Zotero PDF retrieval谈起

从Zotero 5.0.56版本开始，Zotero迎来了`PDF retrieval`功能。详情可见Zotero官网的文章[“Improved PDF retrieval with Unpaywall integration”](https://www.zotero.org/blog/improved-pdf-retrieval-with-unpaywall-integration/ "Improved PDF retrieval with Unpaywall integration")

该功能会在你用Zotero Connector保存文献时，自动检查Unpaywall上是否有可供下载的免费文献。

> Unpaywall能免费下载文献，但你不要以为它和Sci-Hub一样是非法的。其实Unpaywall是个非盈利性合法组织，它整合了数千个Open Access期刊或数据库，将免费文献集中之后开放API，从而供其他平台使用。

假如你在网页端保存的文献是Open Access的，Zotero Connector就会将PDF同文献条目一起抓取，比如下面这样。

![](https://tva1.sinaimg.cn/large/00831rSTly1gco4ykyxfmj30ja0eqdgm.jpg)

当然，对于已经在Zotero中却还没有PDF附件的文献条目，点击右键菜单中的`Find Available PDF`，即可下载文献，比如下面这样。

![](https://tva1.sinaimg.cn/large/00831rSTly1gco4zvgy6dj30hs0dkta7.jpg)

但是，毕竟Unpaywall只支持OA文献，而OA文献又只是少数。也就是说，通过Unpaywall无法解决付费文献的下载问题。

不过幸运的是，作为一款开源软件，Zotero的开发者为很多功能带来了可定制的能力，方便用户根据自己的喜好自定义。

`PDF retrieval`功能也不例外，Zotero允许用户自定义PDF解析器（custom PDF resolvers），也就是说你可以将其他网站作为PDF解析器，来替代Unpaywall。

详情可以访问Zotero官网链接[Custom PDF Resolvers](https://www.zotero.org/support/kb/custom_pdf_resolvers "Custom PDF Resolvers")

这为我们将Sci-Hub作为PDF resolver带来可能！

考虑到PDF resolver是内置在Zotero中的，这能保证我们能稳定使用该功能，就算Zotero更新了也丝毫不用担心，这一点就比使用第三方插件要有保障得多！

下面具体介绍如何将Sci-Hub作为PDF解析器！

### 设置Sci-Hub作为PDF解析器

PDF resolvers的设置在Zotero的Config Editor中。

我们打开Zotero的首选项，进入`Advanced-->Config Editor`。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200415094411.png)

搜索`extensions.zotero.findPDFs.resolvers`，如下。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200415094458.png)

双击`extensions.zotero.findPDFs.resolvers`，默认情况下是只有一对`[]`。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200415094558.png)

删除`[]`，并将以下代码粘贴进去。

```
{
    "name":"Sci-Hub",
    "method":"GET",
    "url":"https://sci-hub.ren/{doi}",
    "mode":"html",
    "selector":"#pdf",
    "attribute":"src",
    "automatic":true
}
```

然后点击OK。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200415094635.png)

到此就成功将Sci-Hub配置为PDF解析器了，也就是说替代了默认的Unpaywall。

现在，无需重启Zotero，即可调用Sci-Hub免费下载文献了。

这里顺便提三点：

1. 在`"url":"https://sci-hub.ren/{doi}"`中，目前可用的域名有`.tw`、`.ren`、`.si`、`.shop`，大家可以挑选其中一个，哪个用起来体验更好就用哪个。（当然，由于Sci-Hub经常更换域名，保不准改天哪个域名就挂了，或者有新的域名出来，因此此处的代码未来也会根据需要进行更新）
2. 从`"url":"https://sci-hub.ren/{doi}"`还能看到一点。由于Sci-Hub是通过`doi`下载文献的，因此该PDF解析器也需要doi。也就说你的文献必须要有doi，如果doi是空缺的，便无法通过PDF解析器免费下载文献。幸运的是，对于缺失doi的文献，我们可以通过插件[zotero-shortdoi](https://github.com/bwiernik/zotero-shortdoi/releases "zotero-shortdoi")插件一键抓取doi（参考文章[zotero-shortdoi + Sci-Hub，让99%的文献都能被免费下载！](https://mp.weixin.qq.com/s/9UAMrbfHKnmG4tZ7rvnnGA)）。
2. `"automatic":true`，如果设置为true，Zotero会自动下载保存到Zotero中的文献的PDF。比如你用Zotero Connector保存了一些文献到Zotero，它便会自动帮你从Sci-Hub下载文献，并附在相应文献条目下。如果你不需要自动下载，可以设置为`"automatic":false`。

使用方法前面介绍过，主要有两种：

#### 第一种：Zotero Connector

通过Zotero Connector保存的文献，会自动下载PDF，无需任何操作。（看不到进度条，下载速度取决于网速）

#### 第二种：Find Available PDF

选中单篇或者多篇文献，手动点击右键菜单中的`Find Available PDF`，会弹出单独的窗口显示下载进度。同样，下载速度取决于网络速度。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200415095318.png)

关于`下载速度取决于网络速度`有下面两点需要注意；

- 如果你未开启任何网络加速器（比如梯z），即正常使用网络，可以认为Find Available PDF的进度接近你手动从Sci-Hub下载文献的速度。大家应该都体验过，不开启加速器的情况下，Sci-Hub的访问速度还是比较慢的，甚至有时候PDF加载不出来。
- 假如你开启了加速器，推荐使用全局代理模式，而不是PAC模式，因为两种情况下Find Available PDF的进度差异比较大（当然如果你不介意下载速度，使用PAC模式也是可以的）。不过提醒一下，下载完文献，记得切回到PAC模式，因为全局模式下Zotero无法同步文献到坚果云。

到此，本文就介绍完了！

可以看到，搭配Sci-Hub后，Zotero变得更加完美了！这就是开源软件的魅力，它能带来无限的想象空间。

如果你在使用中有什么问题，欢迎留言讨论！