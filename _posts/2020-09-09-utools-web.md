---
layout: post
title: 秒开谷歌/谷歌学术，这到底是什么神器？
date: 2020-09-09 22:36:00
tags: 
- 效率工具
- Mac生产力
- Windows生产力
published: true
---



作为科研工作者，谷歌和谷歌学术或许是用得最多的两个搜索引擎了，几乎每天都要在浏览器打开很多次。

以我自己来说，不论是自己找文献，还是看到有粉丝在微信群或者QQ群求助文献，我都是首先选择谷歌学术来检索。

时间是宝贵的，效率是每个人都应该追求的。

**那么有没有什么方法，让我们使用电脑时，在任何时候任何地方都能够极速打开想要的网页，并进行检索呢？**

这便是今天想要说的主题了。

#### 直接看结果

首先，用几张动图演示几个玩法。

![秒开谷歌学术并直接检索](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909172124.gif)


![秒开谷歌官网](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909172124.gif)

![秒开谷歌/谷歌学术搜索框](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909172302.gif)

下面看看如何实现！👇

#### 网页快开

为了实现以上功能，要借助**uTools**这款神器。不知道什么是uTools？可以看前期的几篇推送。

1. [这个强大的插件工具集，让你效率翻倍！](https://mp.weixin.qq.com/s/-dPVrJn8DOxOKDuuPUdrNA)
2. [这款小众的OCR神器，居然好用到爆！](https://mp.weixin.qq.com/s/BVRbOd75u6BpXb3xv6PJ0A)
3. [又一个超级实用的文献翻译技巧！get起来！](https://mp.weixin.qq.com/s/bPC0seicGvVPRh-P9JzqIQ)
4. [这款时钟工具，兼具小巧和颜值于一身！](https://mp.weixin.qq.com/s/xvr-FoCqTuEH6bt-d6C-8A)
5. [这款取色神器，你的创作好帮手！](https://mp.weixin.qq.com/s/5HOJHtHVemGgtz7GInnfUQ)


然后，在插件中心找到**网页快开**插件，下载安装。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909173042.png)

在**已安装**标签页中，找到**网页快开**，并点击**网页快开设置**。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909173157.png)

根据自己的需要，勾选相应的搜索引擎，并记住**功能关键字**。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909173333.png)

常用的搜索引擎基本囊括其中，我启用的是**谷歌、百度、知乎、哔哩哔哩**。

不过**谷歌学术**不在默认的列表中，需要点击**我的自定义**进行自定义设置。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909173737.png)

功能关键字为`谷歌学术`，搜索表达式填写如下：

```
https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q={query}&btnG=
```

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909185646.png)

最后，设置下快捷键，我的快捷键设置如下。

![快捷键设置](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909190109.png)

到此，按下相应的快捷键即可使用了！

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909190314.png)

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909190519.png)

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909190532.png)

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909190540.png)

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200909190554.png)

顺便提一下，**如果搜索框内不输入任何内容，直接按下Ente，亦可打开官网主页，这点很实用。**

尽管很多软件也能实现快速调用搜索框，但是它们通常需要输入手动关键词才能启用某个搜索引擎，比如Alfred。

相比之下，**网页快开**插件就很完美了，这得益于uTools的快捷键功能。

当然，如果搭配Keyboard Maestro Editor还能玩出更多花样，大家可以自行探索！

#### 下载

**uTools下载**：`青柠学术`公众号后台回复`uTools`获取下载链接。

如果本文对你有所帮助，欢迎**三连走起**！