---
layout: post
title: Karabiner-Elements，键位定制神器！
date: 2020-09-13 22:36:00
tags: 
- Mac生产力
published: true
---



最近，我介绍的很多内容都涉及到快捷键，比如：

Zotero的Zutilo插件通过引入一系列快捷键，彻底提升了Zotero的使用效率；

- [重磅 \| 最强插件Zutilo，如何彻底改造Zotero使用效率?](https://mp.weixin.qq.com/s/KtSAUPDlAzHbzBAVYi5AeA)

为Mac词典配置快捷键`CMD+Shift+2`，大大提高查词效率；

- [Mac词典打磨，创造极致查词体验！](https://mp.weixin.qq.com/s/fyck4PpL6dmi7IhEmx12Xw)
- [Mac词典打磨，第二弹！](https://mp.weixin.qq.com/s/6u626jmVysUjn9YLxC3tvA)

为**沙拉查词+Alfred**组合配置快捷键`CMD+Shift+D`，打造极致文献翻译体验；

- [沙拉查词 + Alfred，打造最佳文献翻译体验！](https://mp.weixin.qq.com/s/m071TKFoogCkmZb-s1qyXA)

为uTools聚合翻译配置快捷键`CMD+Shift+E`，让文献翻译又多了一个极佳选择。

- [又一个超级实用的文献翻译技巧！get起来！](https://mp.weixin.qq.com/s/bPC0seicGvVPRh-P9JzqIQ)

> 等等这些各类玩法，都只有一个目的：**创造更为强大的生产力环境，让我们的电脑最大化发挥它的价值，服务于学习和科研。**

那么，可以发现，我们总是会优先使用比较顺手的快捷键组合，也就是说这些快捷键往往单手可以操作，而且误触概率较低。

可是，好用的键位总是有限的，你是否陷入了键位焦虑呢？

今天，便向大家介绍一下Mac上的键位定制神器**Karabiner-Elements**，它将通过**键位映射**帮助我们定制出更多顺手的键位。

#### 下载安装Karabiner-Elements

Karabiner-Elements （以下简称KE） 是一款 macOS 平台修改键位映射的免费开源神器。

在KE的[官网](https://karabiner-elements.pqrs.org "Karabiner-Elements官网")可下载该软件。

如果你访问官网速度较慢，可以在`青柠学术`公众号后台回复`KE`获取安装包。

#### 键位映射

KE可以进行各种类型的键位映射，今天主要介绍的是最具特色、使用最频繁的`caps lock`-->`cmd+option+control+shift`键位映射。

也就是说，当你按下了键盘上的`caps lock`键，就等同于同时按下了`cmd+option+control+shift`键。

那么，为什么要用`caps lock`键呢？

主要是因为这个键用得较少（大小写或者切换输入法时会用到），大部分情况下处于闲置状态，因此有必要将其利用起来。

还有一个原因是这个键的位置左手容易接触到，因此和其他按键搭配起来使用会较为顺手。

那么，为什么要映射到`cmd+option+control+shift`呢？

这是因为这四个键的组合几乎不可能与现有的快捷键冲突。

解释完什么，下面看看如何实现。👇

#### 实现方法

打开Karabiner-Elements，点击`Complex modifications`，然后点击左下角的Add rule。



![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200822232159.png)

自带的Example中就有想要的`caps lock`取代`cmd+option+control+shift`，直接enable即可。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200822232636.png)

如果想要导入更多rules，可以点击上图的import more rules from the internet，跳转到[下方网页](https://ke-complex-modifications.pqrs.org "导入更多rules")。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200822232906.png)

找到自己需要的，点击import即可。



![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200822233017.png)

导入成功后如下图所示，可以放心使用了！

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200822233219.png)

#### 搭配Keyboard Maestro Editor

Karabiner-Elements（KE）与Keyboard Maestro Editor（KM）搭配使用，才能最大化地发挥它的价值。

以一个最简单的例子来所，假如我想设置`caps lock+J`为Zotero的快捷启动键，便可以在KM中设置如下工作流。

![以设置Zotero启动快捷键为例](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200913195440.png)

当然，还有更多有趣的玩法，以后将结合实例具体介绍！

今天就介绍到这里，如果本文对你有所帮助，欢迎**文末三连**！

**顺便提一下**：公众号后台回复`KE`获取Karabiner-Elements安装包；回复`KM`获取Keyboard Maestro Editor安装包。