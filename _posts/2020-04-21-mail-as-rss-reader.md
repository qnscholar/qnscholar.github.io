---
layout: post
title: 为了更好地跟踪文献，我把邮箱“改造”成了Rss阅读器！
date: 2020-04-21 22:36:00
tags: 
- Zotero
- 文献检索与追踪
published: true
---

在上一篇推文[如何使用Zotero Rss跟踪最新文献（含关键词文献）？](https://mp.weixin.qq.com/s/eOvHbqvnSmtUYcAF4ao-yw)中，我向大家介绍了几种主流的文献管理方式：

- 创建跟踪/Create Alert，通过邮箱推送。
- Rss订阅整个期刊。
- Rss订阅特定关键词文献。

并得出了这么一个结论：

>  通过邮箱推送（主要是谷歌学术和Web of Science）方式可以跟踪任意关键词（或领域）的最新文献，无论你是什么专业，无论你想了解哪个方向的前沿学术动态，都毫无限制。然而Rss订阅的局限性就比较多了，因为并不是每个期刊都支持Rss订阅，更重要的是，缺乏一个学科覆盖广泛，且支持Rss订阅关键词文献功能的搜索引擎或数据库。**因此，邮箱推送方式是跟踪文献的最佳选择。无论现在还是将来**。

那么，大家是否思考过下面这些问题？

1. Rss订阅和邮箱推送在本质上究竟有什么区别？
2. 为什么邮箱推送方式渐渐成为主流？
3. 为什么Web of Science用邮箱推送取代了Rss订阅？这一改变有牺牲什么功能吗？
4. 邮箱推送是否也能改造成Rss订阅一样的效果？

为了回答上面几个问题前，我们可以沿着下面这个思路走。（要开始啰嗦了...）

从`数据传输`的角度看，Rss订阅和邮箱推送都是完成了`发`和`收`两个环节。

Rss源负责搜集文献信息，然后用一个Rss地址实现信息传递，进而完成了Rss订阅的`发`环节；通过Rss阅读器（比如Zotero Feeds）导入Rss地址，实现对文献的抓取，即完成了Rss订阅的`收`环节。

对于邮箱推送方式来说，当你创建了一个跟踪，其实相当于创建了一个筛选条件，数据库或者搜索引擎负责将符合筛选条件的文献，通过一个固定的官方邮箱发送到你的邮箱，即完成了邮箱推送的`发`环节；当你的邮箱收到邮箱后，你跟踪的文献便进入了你的收件箱，即完成了邮箱推送的`收`环节。

从`数据内容`的角度看，通过Rss订阅或邮箱推送方式，我们跟踪到的某篇文献包含的信息是基本一直的，有标题，有作者，有时间，有期刊，有网址。

因此，综合上面两个角度，Rss订阅和邮箱推送似乎没多大区别。

**那么，为什么用户会觉得它们两不一样呢？**

**这是因为这两种方式最后呈现给用户的文献信息流的展示方式不同**。对Rss订阅来说，跟踪的文献一般是存在一个文件夹中，整整齐齐，明明白白；对邮箱推送方式来说，收件箱会定期收到订阅的文献，但是在时间流上和其他邮件是穿插的，相对于Rss阅读器来说没有那么一目了然。

那么，**如果我们把邮箱中订阅到的文献进行分类管理，将它们从海量的邮件中单独归类到一个文件夹中，不就实现了和Rss阅读器差不多的效果吗？**

此时，就需要用到邮箱的邮件过滤器功能了。**通过创建精准的过滤条件**，将想要集中阅读的订阅文献归类到一个文件夹就可以了。

可以说几乎每一个邮箱都有过滤器功能，下面我就**以Gmail邮箱**为例，来演示如何让订阅到的文献自动归类到一个自定义的文件夹中。

### Gmail邮箱“改造”为Rss阅读器

打开Gmail邮箱，点击右上角的**小齿轮**按钮，并选择**设置**。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421082013.png)

在**设置**界面，选择**过滤器和屏蔽的地址**，并点击**创建新的过滤器**。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421082052.png)

在创建过滤条件之前，我们先查看任意一封Google Scholar文献推送邮件的**特征**。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421085240.png)

1. 发件人方面，所有Google Scholar的文献推送邮件都是通过官方邮箱`scholaralerts-noreply@google.com`发出的。
2. 邮件主题中会包含文献的关键词，并以双引号表示，比如`"acoustic tweezers"`，这一点非常重要。

根据以上两大特征，我们可以**实现以下两类文献过滤需求**。

1. 过滤全部Google Scholar推送的文献，便于汇总。
2. 过滤Google Scholar推送的特定关键词文献，便于分类。

那么，现在就开始设置过滤条件。👇

**假如想要过滤Google Scholar推送的全部文献**，只需将**发件人**设置为`scholaralerts-noreply@google.com`即可。

![过滤全部谷歌学术推送文献](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421085550.png)

**假如想要过滤特定关键词文献**，除了将**发件人**设置为`scholaralerts-noreply@google.com`，还要将**主题**设置为**搜索关键词**（以英文双引号括住），比如设置为`"acoustic tweezers"`。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421085932.png)

点击**继续**，为了将符合筛选条件的文献自动归类到一个自定义文件夹，需要勾选☑️**应用标签**。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421090111.png)

然后**新建一个想要的标签**即可。如果是筛选Google Scholar推送的全部文献，可以建一个诸如`Google Scholar Alerts`的标签；如果是筛选特定关键词的文献，不妨把标签命名为**关键词的名称**，比如`"acoustic tweezers"`，辨识度高，不会错乱。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421090224.png)

最后，点击**创建过滤器**，即可完成创建。

下面是我创建的两个过滤器，一个用于筛选Google Scholar推送的全部文献，一个用于筛选特定关键词的文献。创建成功后，左边就会以标签来分类管理相应的文献（实现了Rss阅读器的效果）。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421091000.png)

还有一点需要注意下，完成上面创建步骤后，只是对新邮件起作用，邮箱中之前收到的符合筛选条件的邮件还无法自动归类到相应的标签下，为了做到这点，我们可以**修改标签**。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421091454.png)

接着，点击**搜索**。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421091605.png)

所有符合条件的邮件都会搜索出来。👇接着，我们通过翻页将搜索邮件选中，并设定相应的标签，即可将实现将过去的邮件分类整理到对应的标签中。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421092157.png)

到此，即完成了所有设置。

下面，我们打开标签`Google Scholar Alerts`来看看其中的文献。

![邮箱“改造”成Rss阅读器](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421092517.png)

顺便贴一张Zotero Feeds的Rss文献订阅界面，进行对比。

![Rss阅读器文献订阅效果](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200421092759.png)

可以看到，**从文献流的展现形式上**，**被改造的邮箱**也能实现与Rss阅读器类似的效果；**从功能上看**，却突破了Rss阅读器跟踪文献的种种限制。

具体优势可以总结如下：

1. 任何关键词，任何领域，任何学科的文献都可以通过Google Scholar或Web of Science的邮箱推送服务，并搭配邮箱的过滤器功能，实现文献的分类管理。
2. 人人都有邮箱，不论是在电脑上，手机上还是iPad上，都能随时查阅跟踪到的最新文献信息，无需为挑选一款称心的Rss阅读器而烦恼。

以上仅仅是对Gmail邮箱的演示，其他邮箱也有相同的功能，根据自己的常用邮箱进行设置即可。（我还设置了浙大的教育邮箱，也是完全OK的）

本文内容到此结束，感谢阅读！

