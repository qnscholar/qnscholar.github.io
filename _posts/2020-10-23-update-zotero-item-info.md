---
layout: post
title: Zotero更新文献题录的一种思路
date: 2020-10-23 22:36:00
tags: 
- Zotero
published: true
---



很多人都期待Zotero能够支持更新文献题录的功能。

为什么呢？

因为可能少数文献还不是正式版的，又或者用[不同方法](https://mp.weixin.qq.com/s/sF5Q8XGvYg0ERA7FFaoxmw)抓取的文献题录信息也是有所差异的。

好消息是，**Zotero官方明确表示未来会上线更新文献题录的功能，相信官方也看到了广大用户的心声。**

那么，在该功能还未正式上线前，有没有什么思路可以间接实现题录更新呢？

今天就简单聊一聊。

### 第一步：通过DOI重新导入文献

之所以想更新题录信息，自然是希望更新到一个更全更新的题录。

这就涉及到怎么样能够获得更全的题录信息。

关于这一点，之前我在下面这篇推文中详细介绍过。

[为什么你导入的Zotero文献题录信息总是不够完整\?](https://mp.weixin.qq.com/s/sF5Q8XGvYg0ERA7FFaoxmw)

也就是说：**通过DOI导入文献的方式，往往能够抓取到最全的题录信息。**

既然如此，如果你是用了[zotero-shortdoi](https://mp.weixin.qq.com/s/ddJ_liehAU0fJ7M8B-Hrzg)插件，那么获取文献的DOI便是轻轻松松。

那么，我们就复制DOI。👇

![复制DOI](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201022173358.png)

然后通过DOI导入文献。

![通过DOI导入文献](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201022173547.png)

至此，就有了两个相同的文献条目，一条新的一条旧的。

![两个相同的文献条目](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201022173610.png)

接下来，当然是把旧的题录删掉，怎么删？两种方法。👇

### 第二步：两种方法可选

第一种方法，简单粗暴：先把旧条目下的PDF拖到新条目下，然后把旧条目删除，即可搞定。

第二种，通过Zotero的重复条目功能，如下。

![Duplicate Items](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201022174143.png)

因为第一步之后Zotero中出现了相同的条目，那么这两个条目便会自动出现在Zotero的Duplicate Items中。

点击待更新的条目，在右侧可以看到新旧题录的创建时间和相应的题录信息。

![新旧题录](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201022174406.png)

**合并条目之前，需要选择一个主条目（master item）。**

所谓主条目，即你最终要保留的题录信息。

![选择主条目](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201022174406.png)

比如上图，我选择了第二条，那最终的题录信息便是第二条的，就算第一条中有些字段第二条没有，合并之后也不会再有。

包括PDF附件，也只会保留第二条的。

合并之后，效果如下。

![合并之后](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201022175219.png)

至此，可以看到上述方法还做不到批量文献的题录更新，只能等待官方支持了。

如果本文对你有所帮助，欢迎**三连走起**！