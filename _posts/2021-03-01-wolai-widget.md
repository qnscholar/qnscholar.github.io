---
layout: post
title: wolai嵌入小组件！试一试？
date: 2021-03-01 22:36:00
tags: 
- 双向链接笔记
published: true
---



小组件（Widgets），是iOS 14和macOS Big Sur的新特性。

颜值无敌，看一眼都觉得心情舒畅。

比如下面是我的MacBook Pro小组件截图。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210301190451.png)

那么，以颜值和优雅著称的wolai，如果也能用上小组件那岂不是很棒。

其实，wolai的**嵌入内容**命令`/qrnr`，可以实现小组件的嵌入。

![嵌入内容 - /qrnr](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210301192544.png)



问题是，命令有了，小组件哪里来？

今天就分享一个小组件网站[indify](https://indify.co)。

### indify

访问indify网站，首先注册一个账号。

登入后，可以看到网站的界面，简洁美观。

![indify](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210301191747.png)

上图便是目前indify提供的几种小组件，**包括天气、生命进度条、名言名句、时钟、相册集等等**，还在继续扩充中。

我个人比较喜欢天气☁️小组件，下面以它为例介绍。


将鼠标放置在天气小组件上方，即可出现Create widget字样。

![Create widget](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210301192253.png)

单击进入。

你可以设置城市（比如我所在的是杭州）、温度单位、显示天数、字体颜色、深色模式等等参数。

![设置天气小组件](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210301192706.png)

创建完毕后，点击左下角的COPY LINK按钮，以拷贝该小组件的链接。

![拷贝链接](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210301192907.png)

### wolai嵌入小组件

分别看看小组件和wolai在浅色模式和深色模式下的样子。

#### 浅色模式

打开wolai，输入命令`/qrnr`，粘贴小组件链接。

![wolai - 粘贴小组件链接](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210301193143.png)

嵌入天气小组件成功，看起来还可以吧。

![wolai - 嵌入天气☁️小组件](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210301193132.png)

点击小组件，还可以对它的大小进行调整。

![调整小组件的尺寸](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210301193415.png)

#### 深色模式

将小组件和wolai都切换到深色模式，效果如下。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210301193608.png)

可以看到，小组件的背景和wolai的背景存在一定色差，这是因为indify适配的对象是Notion。

看看Notion嵌入该天气小组件的样子，背景完美融合在一起，视觉效果更好。

![Notion - 天气小组件](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210301194748.png)

顺便对三者的深色背景取色看一下：

- wolai：RGB (37,37,40)
- Notion/小组件：RGB (47,52,55)


### 对wolai的期待

我倒是觉得，wolai未来可以开发官方的小组件库，如此一来，对小组件的设计、丰富性、适配度等方面都能把控得更好，继续发扬一流的设计能力和超高的审美水平。

当然，这部分可以作为付费服务。