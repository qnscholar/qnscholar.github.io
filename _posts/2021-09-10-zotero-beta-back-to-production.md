---
layout: post
title: Zotero Beta版如何完美降级到正式版？
date: 2021-09-10 22:36:00
tags: 
- Zotero
published: true
---



帮助青柠er们解决问题，我乐此不疲。

前阵子，在推送了下面这篇推文后，有很多粉丝问：**有没有办法将Zotero从Beta版降级到正式版？**

[谨慎使用Beta版Zotero！原因必看！](https://mp.weixin.qq.com/s/73BPpyQbCon8OED41OloEg)

这几天，我在[Zotero论坛](https://forums.zotero.org "Zotero论坛")寻找解决办法，并用Zotero小号进行方法验证。

下面就介绍下Zotero从Beta版降级到正式版的办法。

#### 为什么要降级？

尽管Beta版Zotero的内置PDF阅读器深受很多用户喜欢，但同时也出现了很多插件无法工作或者不稳定的情况，比如ZoteroQuickLook、Mdnotes等，极大地影响了使用体验。

因此，很多用户迫切希望降级到正式版。

#### 降级步骤

其实在早期的时候，对于Beta用户，直接用正式版安装包覆盖安装，即可顺利回到正式版。

自从Beta版Zotero提供了[内置PDF阅读器](https://mp.weixin.qq.com/s/MWKSpWfD3pTWuW-Q5dgKwQ)后，降级时会提示数据库不兼容。

那么，自然就会有人提问如何降级了？这不，在[Zotero论坛](https://forums.zotero.org/discussion/89943/revert-from-beta-to-production "解决方案")找到了官方答案。👇

![Zotero论坛](https://gitee.com/qnscholar/figurebed/raw/master/img/20210910150843.png)

下面，我以Mac版Zotero进行演示。（Win版同理）

假如你现在用的是[Beta版Zotero](https://www.zotero.org/support/dev_builds "Beta版Zotero")，如下。（Beta版界面丑爆了）

![Beta版Zotero](https://gitee.com/qnscholar/figurebed/raw/master/img/20210910151441.png)

首先，从官网下载[正式版Zotero](https://www.zotero.org/download "正式版Zotero下载")。

**覆盖安装，或者先卸载Beta版，再安装正式版Zotero。**（经测试，两种方式均可以保留原来的同步、插件等设置）

安装完正式版Zotero后，打开，**此时会提示数据库不兼容**。👇

![提示数据库不兼容](https://gitee.com/qnscholar/figurebed/raw/master/img/20210910152005.png)

不用慌，解决办法很简单。👇

首先，我们退出Zotero应用。

然后，进入Zotero的数据目录。不知道的可以看下图。👇

![](https://gitee.com/qnscholar/figurebed/raw/master/img/20210910152357.png)

在Zotero数据目录中，删除`zotero.splite`文件。

![](https://gitee.com/qnscholar/figurebed/raw/master/img/20210910152600.png)

重新打开Zotero，👇此时不再提示数据库不兼容，而是一个初始界面，我们点击右上角的**同步按钮**。（确认之前的同步设置依然保留着）

![](https://gitee.com/qnscholar/figurebed/raw/master/img/20210910152846.png)

出现下面的提示，我们点击同步。

![](https://gitee.com/qnscholar/figurebed/raw/master/img/20210910153030.png)

很快，文献及其附件同步成功。👇

![](https://gitee.com/qnscholar/figurebed/raw/master/img/20210910153150.jpg)

到此，就完成了从Beta到正式版的降级。

<blockquote data-tool="科技兽" style="border-top: none;border-right: none;border-bottom: none;font-size: 0.9em;background: url(https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210519013028.png) 10px 10px / 40px no-repeat rgb(31,79,137);overflow: auto;color: inherit;border-left: 0px;padding: 1.2em 2em;margin-bottom: 2em;margin-top: 2em;text-align: center;border-radius: 10px;"><p style="font-family: Optima-Regular, Optima, PingFangSC-light, PingFangTC-light, &quot;PingFang SC&quot;, Cambria, Cochin, Georgia, Times, &quot;Times New Roman&quot;, serif;text-align: justify;line-height: 26px;margin-top: 1em;margin-bottom: 0.3em;font-size: 14px;color: rgb(255, 255, 38);"><strong style="color: #fc8705;">注意事项</strong><br  />一旦降级到正式版，原本在Beta版Zotero的内置PDF阅读器中所作的批注就会丢失。</p></blockquote>

