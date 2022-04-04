---
layout: post
title: 升级macOS Big Sur后，哪些生产力工具不兼容了？
date: 2020-11-18 22:36:00
tags: 
- Mac生产力
published: true
---



大苏尔来了！

> **11月13日，macOS Big Sur正式版发布**，而且上来就是11.0.1版，想必新系统已经被苹果打磨得差不多了！

我也是第一时间体验了下，昨天晚上成功从Catalina升级到Big Sur！

本文就简单说下我对新系统的感受，同时提一下我遇到哪些生产力工具出现了不兼容的情况，想必这也是很多学术人比较关心的。

### Big Sur初体验

Big Sur的UI整体上向iPad OS靠近。

下面挑几个变化比较大的地方说下。

#### 状态栏

状态栏是此次Big Sur变化最大的地方之一。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114175825.png)

有以下几点值得关注：

**状态栏的图标间距增大，但同时左边的App菜单字体变小。或许**，美观的同时，也要塞下更多的内容吧。

状态栏的背景跟随壁纸变化，这个设计会导致在使用部分壁纸时，**状态栏的图标和背景区分度不明显，太丑了！**

控制中心变得好看了，但也仅仅是变好看了而已...

![控制中心](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114180818.png)

通知中心的设计与iPhone以及iPad的负一屏一致，能够显示更多信息。


![通知中心](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114185643.png)

值得一提的是，**状态栏最右边终于能够直接显示日期了**，之前只显示周几和时间。

#### 访达

访达的UI同样和iPad的文件管理器靠近，变得更加清爽了！

![访达](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114190021.png)

#### Safari

功能上的变化就不提了，新版Safari的UI上基本和iPad版一致，工具栏的高度提高了，着实有点不习惯，没有那种简洁的感觉了...有点小失望。

![Big Sur - Safari](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114190241.png)

![iPad - Safari](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114190241.png)



#### 图标

Big Sur的App图标整体上使用圆角矩形，与iPad OS一致。

**不过，这也将原本漂亮的拟物风图标变得丑的不忍直视...**

最丑的该属：

![词典](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114191629.png)

![预览](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114191730.png)

有人肯定担心，**会不会以后Mac系统就不允许其他App出现异形图标，非得采用圆角图标呢？**

其实不然，官网并非强制开发者使用圆角图标，比如官方App库乐队，图标的元素并未完全限制在圆角轮廓内。👇

![库乐队](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114192016.png)

（我觉得这是最好看的官方App图标了）

所以，还是期望开发者们能保留App图标的特色，千篇一律的圆角图标将大大减弱macOS系统的魅力。

### 生产力App兼容性

升级到Big Sur后，不少软件都出现了兼容性问题，有的直接不能用，有的出现UI不适配的情况。

**特别地，我们更关心一些重度生产力工具的兼容性问题，比如Office、文献管理工具。**

下面列举几个我发现存在兼容性的App。

#### Zotero

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114193223.png)

尽管Zotero在这个月初就已经适配了Big Sur，请看更新日志。👇

![Zotero适配Big Sur](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114193411.png)


但是很多第三方插件并未即时适配，这就导致几乎所有第三方插件的设置界面，会出现活动标签页的标题无法显示的Bug，以ZotFile插件为例。👇

![Zotero第三方插件UI未适配](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114193613.png)

尽管不影响使用，但是确实不太美观，只希望第三方插件能够尽早适配。

**总之，目前没有发现Zotero在功能上的兼容性问题，可以放心使用。**

在Word中插入Zotero文献也一切正常。

![文献插入一切正常](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114194512.png)

#### Keyboard Maestro

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114194656.png)

工作流利器Keyboard Maestro直接就打不开了...

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114195114.png)

不知道Keyboard Maestro有什么用？可以看下面的推文。

[Mac词典打磨，第二弹！](https://mp.weixin.qq.com/s/6u626jmVysUjn9YLxC3tvA)

#### Final Cut Pro

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114195842.png)

更新到Big Sur后，我一直使用的Final Cut Pro 10.4.8版本不再兼容，直接打不开了...

想要继续使用，请下载安装[Final Cut Pro 10.5](https://www.macdo.cn/30848.html "Final Cut Pro 10.5")版本，该版本已适配Big Sur。

#### CleanMyMac X

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114200555.png)

我使用的CleanMyMac X 4.6.2功能上一切正常，但是UI出现不兼容问题，请看下图绿色箭头处。

![CleanMyMac X UI不兼容](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201114200753.png)

相信还有很多App存在兼容性问题，**不过好在一些日常必须的软件没什么问题，比如Office目前一切正常。**

所以，如果你不介意以上出现的兼容性问题，请放心升级Big Sur！