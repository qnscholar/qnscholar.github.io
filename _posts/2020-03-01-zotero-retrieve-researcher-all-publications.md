---
layout: post
title: 重磅｜Zotero如何一次抓取某个作者发表的全部论文？
date: 2020-03-01 12:37:00
tags: 
- Zotero
published: false
---

很多时候，我们想要知道某个学术大佬都发表了哪些论文，以便通过阅读他的著作激发一些灵感。最好还能知道哪些论文引用量高，从而重点阅读。

作为科研小白，刚来实验室的时候对本课题组的研究方向还不清楚，这时搜集一下师兄师姐发表过的论文，想必阅读一遍下来便会对该方向有个系统的了解。

今天给大家介绍一个非常重要的技能：用Zotero一次性抓取某个作者发表的`全部论文`，还能显示每篇论文的`引用量`。👇

---

本文必备工具：

1. 能够访问谷歌学术，这个靠自己。
2. Zotero Connector
3. Zotero
4. Zotero Scholar Citations 插件

---



### 谷歌学术主页文献抓取

考虑到绝大部分科研工作者都有谷歌学术主页，这里一般会包含他的全部学术成果。再者，Zotero对谷歌学术的支持非常好，因此我们就通过谷歌学术来实现。

访问谷歌学术https://scholar.google.com/[](https://scholar.google.com/)。

右上角登录自己的谷歌账号，然后点击左上角的My profile，即可进入个人谷歌学术主页。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gcecipu3wdj31740pn76g.jpg)

在个人主页，如果你想要了解的科研工作者已经被你添加到合作作者（Co-authors）中，比如你的师兄师姐，或者课题组的老师，便可以从右下角点击头像进入他的谷歌学术主页。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcecmz7zvcj31740pn0y3.jpg)

当然，如果是其他作者，可以直接在右上角搜索框🔍进行搜索。

比如搜索我毕业的师兄“Jinkai Chen”。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gcecs0wknvj31740pngnd.jpg)

点击头像进入我师兄的谷歌学术主页。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcect8b6yvj31740pnwjl.jpg)

此时，可以看到右上角的Zotero Connector变成了一个`文件夹`的形状，代表本页面的文献可以抓取。

在开始抓取前，跟大家说一个决定抓取成败的关键一步：判断谷歌学术是否需要`人机验证`。

> 如果一次性向谷歌学术发送太多的请求，谷歌会认为可能是人机在操作，因此会加入人机验证这一步骤，也就是经典却有点烦人的看图识别。

因此，我们先不急着抓取文献，我们再回到谷歌学术主页，任意搜索点什么，比如我输入`saw`。

你看，说不定正巧需要人机验证。（如果之前大量使用了谷歌学术，可能会出现）

![](https://tva1.sinaimg.cn/large/00831rSTly1gced2qlu6sj31740q775t.jpg)

点击“I'm not a robot”，完成烦人的识图环节。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gced54krqbj31740q7418.jpg)

验证成功后，即可正常显示搜索结果，这代表我们完成了人机验证。

![](https://tva1.sinaimg.cn/large/00831rSTly1gced60fg8yj31740q779n.jpg)

我们回到想要抓取文献的谷歌学术主页。

![](https://tva1.sinaimg.cn/large/00831rSTly1gced7hakowj31740q7af0.jpg)

如果一个作者发表的成果特别多（超过20篇），谷歌学术会将文献列表折叠起来，此时我们需要往下滚动，点击`SHOW MORE`，直到所有文献全部显示出来，这样Zotero Connector才能一次性抓取所有文献。

所有文献显示出来后，我们先在Zotero中新建个文献集，比如以作者姓名命名为`Chen JK`，用于存放将要抓取的文献。

接着，我们点击右上角的Zotero Connector图标。

弹出文献选择窗口，我们选择全部`Select All`，并点击OK。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcedbb0v1ij30jt0c5tap.jpg)

接着，会显示Zotero Connector的文献抓取进度，可以看到还能自动抓取一些文献的PDF（开源或者作者分享了PDF）。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcedfzly4qj31740q70yz.jpg)

由于文献较多，等待几分钟才能完成所有文献的抓取。

抓取完成后，在Zotero中可以看到这个作者的全部论文都在新建的`Chen JK`中了，而且免费PDF也成功下载了，爽歪歪。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcedjyogcwj31740q8qb2.jpg)

`全部论文`的抓取完成了，接下来就是如何显示文献的`引用量`。

### 文献引用量显示

之前我分享过能够显示文献引用量的[Zotero Scholar Citations](https://mp.weixin.qq.com/s/44ADU_pE5-9n2DxY3d_IEg)插件，现在我们就用上它。（最近又琢磨了些用好这款插件的一些技巧，以后再谈）

全选所有文献，点击右键菜单中的`Update citation(s)`。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcedtx4bzij31740q8gvh.jpg)

这里可能又会遇到人机验证问题。由于Zotero Scholar Citations插件需要通过谷歌学术抓取文献的引用量，因此文献过多时会造成请求太频繁，谷歌会要求人机验证。这个目前无解，Zotero Scholar Citations的[GitHub上有相关的说明](https://github.com/MaxKuehn/zotero-scholar-citations)。

提示需要人机验证消息如下。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcedzbeugtj31740q7jy3.jpg)

按照要求完成人机验证即可。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gcee01sdiij30oo0q7gmg.jpg)

人机验证完毕后，重新点击`Update citation(s)`，即可成功显示全部文献的引用量。

引用量会显示在`Extra`中，我们可以将该列显示出来，并按照引用量降序或者增序排列，一目了然，如下👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gcee3z4z1gj31740q8wly.jpg)

这样一来便可以从引用量多的文献开始读起。

顺便提一下为何有些文献的引用量显示`ZSCC:NoCitationData`，这一般是因为该文献信息不全，造成Zotero Scholar Citations插件无法检索到，详解请移步[GitHub](https://github.com/MaxKuehn/zotero-scholar-citations)。

到此介绍完毕，如果有任何使用问题，欢迎下面留言或者加入青柠学术交流群进行讨论。

