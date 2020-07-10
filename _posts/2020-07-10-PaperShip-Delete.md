---
layout: post
title: 同步出现问题？别再甩锅PaperShip了！
date: 2020-07-10 22:36:00
tags: 
- Zotero
published: true
---




> 同步出现问题？别再**甩锅**给PaperShip了！因为你忽略了关键的一步！下面听我一一道来。

前几天在下面这篇文章中，给大家了做了一期PaperShip的测评视频。

[全面测评 \| PaperShip的文献同步速度和批注体验究竟如何？](https://mp.weixin.qq.com/s/ObfwHWaQaXdc1X_iz9WxnA )

测评内容包括：**Zotero与PaperShip间的文献双向同步，批注双向同步，以及坚果云WebDAV的配置等。** 


值得欣慰的是，这些测评结果都是令人满意的。

可是，是否有PaperShip用户发现一个现象：**明明在Zotero中删除了某篇文献或者文件夹，怎么在PaperShip中还是存在，无论尝试同步多少次都没有用。**

不禁让人怀疑是不是PaperShip的同步出现问题了。

其实不然。

为了搞清楚这个问题，我们必须熟悉**Zotero的删除机制。**

前阵子，我在下面这篇推文中，向大家详细介绍了这方面的内容。

[Zotero的【删除】功能，竟然有这么多花样！](https://mp.weixin.qq.com/s/90S0plmWopkQMOY8Gn0NBw )

简单地说，Zotero的删除可以分为下面两类。

- 删除文献或文献集，但不移动到回收站。（如Remove Item from Collection）
- 删除文献或文献集，并移动到回收站。(如Move Item to Trash)

如果你在Zotero中将文献（或文献集）删除并移动到回收站了，其实，对应的文献的PDF依然存在云端，**除非你清空回收站。**（回收站是一种安全机制）

![清空回收站](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200709234314.png)

这会导致PaperShip在刷新同步之后，相应的文献**依然纹丝不动**，并未被删除。

所以，如果你在Zotero中选择的是**删除文献或文献集，并移动到回收站**，请先**清空回收站**，再同步文献。此时你便会发现PaperShip中对应的文献也删除了。

如果你在Zotero中选择的是**删除文献或文献集，但不移动到回收站**，请放心，无需清空回收站，PaperShip中对应的文献会正常删除。

![PaperShip](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200710144827.PNG)


总结一下就是：

- 想彻底删除文献，请记得清空回收站。
- 想移除文献，无需清空回收站。

你get了吗？

本文内容在我的微信视频号【青柠学术】也有同步更新，感兴趣可以关注下。

  

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200710145313.PNG)