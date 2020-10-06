---
layout: post
title: zotero-shortdoi + Sci-Hub，让99%的文献都能被免费下载！
date: 2020-03-11 23:1:00
tags: 
- Zotero
published: true
---

昨天推送的文章[Zotero搭配Sci-Hub，真香！](https://mp.weixin.qq.com/s/q7fZJVZbFaL_xwtRxivD2w)，受到了广泛好评，毕竟好用的工具每个人都需要！

简单回顾下：通过将Sci-Hub配置为Zotero的PDF解析器，可以实现在Zotero内免费下载几乎所有文献！不论你在哪里，不论你用的外网还是校园网，统统不受限制！

昨天和大家特别提到过，Sci-Hub下载文献是需要doi的（网页端也是一样），因此在Zotero中调用Sci-Hub PDF解析器同样需要doi。

> doi可以看成文献的身份证，是它的唯一标识符，几乎每一篇论文（Journal Article）都有doi。网站https://www.doi.org可以通过doi解析每一篇文章的网页链接。



也就是说，要想免费下载文献，你Zotero文献的DOI栏不能是空缺的。👇一旦缺失doi，在右键菜单中是不会有`Find Available PDF`的，相当于没有了输入参数。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcppymyg53j31740q9jzh.jpg)

可是有些时候，用Zotero Connector在网页端保存或者PDF自动抓取得到的文献中，会有个别文献可能会缺失doi，这会给我们通过Sci-Hub下载文献造成不便。（虽然还有很多其他方式可以快速下载，以后介绍）

因此今天就介绍一款可以快速抓取文献doi的插件[zotero-shortdoi](https://github.com/bwiernik/zotero-shortdoi/releases "zotero-shortdoi")。这款插件我已经使用挺久了，好用又稳定，绝对不会让你失望，而且还支持批量文献的doi抓取。

从GitHub上下载最新版本，如下。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcpq6kyou5j31740q9acq.jpg)

安装到Zotero。（这个大家应该都会，不多说）

在Zotero的插件面板中中，它是以`Zotero DOI Manager`显示的。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcpq8wsy1fj30lq0is3zu.jpg)

这里，可能有人好奇了：为什么这款插件为什么叫做shortdoi呢？

有shortdoi，那肯定有longdoi。其实我们平常在使用的doi，都是longdoi。

下面两种常见形式都是longdoi，其实它们是等效的。唯一的区别在于第二个doi添加了https://www.doi.org域名。我前面说了，https://www.doi.org是通过doi解析文献的，因此每篇文献的doi前面其实都有这么个相同的域名。既然相同，自然可以省略，从而得到下面第一个doi这样子。

- 10.1016/j.nanoen.2018.11.062
- https://doi.org/10.1016/j.nanoen.2018.11.062

那么，可能有的人觉得这两个doi还是有点长了，特别是在参考文献排版时不够美观，因此就诞生了shortdoi，来缩短doi的字符长度。

任意选中一篇或多篇文献（原本缺失doi的或者有doi的），右键菜单如下。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcpqm9dz70j315n0oqgsj.jpg)

可以看到有三项子菜单：

- Get shortDOIs
- Get longDOIs
- Verify and clean DOIs

点击`Get longDOIs`和`Verify and clean DOIs`的效果几乎没有差异，都是抓取文献的longDOIs。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gcpqskf980j315n0ork0u.jpg)

**而且需要注意的是，只有longDOI才能被Sci-Hub所识别**。因此这里就不用管`Get shortDOIs`了，用不上。

获取到了DOI后，就可以右键文献，点击`Find Available PDF`从Sci-Hub下载文献了！

这里顺便介绍下zotero shortdoi插件的默认设置，还蛮重要。

点击Zotero菜单栏Tools-->DOI Manager Preferences。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gcpqymmwfaj315n0pd46o.jpg)

zotero-shortdoi插件会自动为新添加到Zotero中的文献添加DOI，这里建议大家勾选Long DOI作为默认DOI形式。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcpqzyoj2gj30gj0f03z5.jpg)

从上图还可以看到，对于未找到DOI的文献，zotero-shortdoi会自动分配一些标签，比如`Invalid DOI`、`Multiple DOI`等。一般情况不会发生，所以这里不用管。

到此就介绍完zotero-shortdoi的全部了！

感兴趣的快去把zotero-shortdoi + Sci-Hub这个强大组合搞起来！享受免费下载文献的乐趣吧！

