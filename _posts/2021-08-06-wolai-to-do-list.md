---
layout: post
title: 使用wolai制作To Do List，超好看巨实用！
date: 2021-08-06 22:36:00
tags: 
- wolai
- 笔记生态
published: true
---




[wolai专栏](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzAxNzgyMDg0MQ==&action=getalbum&album_id=1685169420177833985&scene=21&from_msgid=2650464256&from_itemidx=1&count=3#wechat_redirect)已经推送了很多期了～


从朋友圈，我也看到了很多粉丝在使用wolai。

最近有粉丝留言说，希望推送wolai在生活、科研、学习等方面的使用案例。



今天，向大家介绍如何使用wolai制作好看又实用的**To Do List**，期望在时间管理方面发挥一定作用。

#### 先看结果

咱先看结果。

To Do List的展开效果如下。👇

![展开效果](https://gitee.com/qnscholar/figurebed/raw/master/img/20210806142405.png)

颜值还是可以的吧～🤭

下面是折叠起来的效果，简洁的同时又能看到进度信息。

![折叠效果](https://gitee.com/qnscholar/figurebed/raw/master/img/20210806144611.png)

实现起来非常容易，下面来看看。

#### 实现步骤

以我个人的需求为例，这里我将To Do List分成了三个部分：

1. 公众号推文
2. 学习
3. 工作

为了让空间显得不那么拥挤，我在页面右上角打开「**自适应宽度**」。

![打开「自适应宽度」](https://gitee.com/qnscholar/figurebed/raw/master/img/20210806145711.png)

首先，通过`/zdlb`命令创建三个折叠列表，分别命名为公众号推文、学习和工作。

通过拖动块，将三者并排放置。

![并排放置](https://gitee.com/qnscholar/figurebed/raw/master/img/20210806150050.png)

然后，展开折叠列表，通过`/jdt`命令创建进度条。

![建进度条](https://gitee.com/qnscholar/figurebed/raw/master/img/20210806214300.png)

在进度条的块菜单中，打开「**自动模式**」。

![打开「自动模式」](https://gitee.com/qnscholar/figurebed/raw/master/img/20210806223214.png)



再次在进度条的块菜单中，复制「**行内块引用链接**」。👇

![复制「行内块引用链接」](https://gitee.com/qnscholar/figurebed/raw/master/img/20210806223121.png)



粘贴到相应折叠列表的名称后面，得到下面的效果。

![粘贴「行内块引用链接」](https://gitee.com/qnscholar/figurebed/raw/master/img/20210806222114.png)

接着在进度条下面通过`【】`快速输入待办列表，即可得到最终的效果。

![最终效果](https://gitee.com/qnscholar/figurebed/raw/master/img/20210806142405.png)

为了更好的视觉效果，可以在进度条的块菜单中**修改进度条的颜色**。

总之，这样的设计，不论是折叠模式还是展开模式，都能看到进度条显示。

本文就到这里，希望对你有所帮助！拜～