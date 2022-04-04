---
layout: post
title: Zotero的【删除】功能，竟然有这么多花样！
date: 2020-05-04 22:36:00
tags: 
- Zotero
published: true
---

最近不断有学员或粉丝问道：**为何从Zotero删除文献后，附件依然保留在坚果云中？这很占空间啊！**

为此，非常有必要专门写一篇推文来讨论下这个问题。

先下个结论：

- 如果你采用`坚果云WebDAV`方式同步文献，从Zotero中删除文献后，是`可以`将其在坚果云中的附件彻底删除的。
- 如果你采用`ZotFile + 同步盘`方式同步文献，从Zotero中删除文献后，常规情况下，是`无法`将其在同步盘中的附件删除的。这点我在之前的推文[ZotFile + 同步盘，实现Zotero文献跨平台同步！](https://mp.weixin.qq.com/s/0heWcOlwgrF6GHmPTc-poA)中介绍过。

下完结论，我们先从Zotero的`删除`功能说起。

### Zotero的“删除”功能

在Zotero中，任意选一篇文献，右键单击。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504094127.png)

可以看到，和`删除`有关的选项菜单有两个：

- “Remove Item from Collection”，即“从文献集中删除”。
- “Move Item to Trash”，即“移至回收站”。

那么，这两个删除有什么区别呢？

下面以`坚果云WebDAV`同步方式为例，来详细解释下。

#### Remove Item from Collection

`从文献集中删除`，**只是把文献从当前所在文献集中删除，并不会将其从我的文库和它所在的其他文献集中删除，更不会将其附件从本地删除，也就无法将其从坚果云中删除。**

之所以说“**它所在的其他文献集**”，是因为有些时候，很多Zotero用户需要把同一篇文献同时归类在不同文献集中。

注意，是通过拖拽文献条目的方式将其复制到其他文献集中，而不是将同一篇文献分两次保存到不同文献集中（比如拖拽PDF或者Zotero Connector保存）。

这是两个完全不同的概念，**前者只会在本地保存一份PDF附件，后者会在本地保存两份PDF附件。**

顺便提一下，针对后者，会在`Duplicate Items`中显示重复的文献，通过`Merge`功能即可将多篇重复的文献合并为一篇文献。

（⚠️对于已经做过笔记或者修改的文献，使用此功能需要慎重，因为在合并中会丢失部分信息）

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504100303.png)

#### Move Item to Trash

`移至回收站`，是将文献条目及其PDF附件都移至回收站，一旦执行该操作，**该文献在所有它存在的文献集中的条目将全部删除，并且PDF附件也会移至回收站。**

**但是，仅仅完成这一步其实并不彻底。**

所谓`Move Item to Trash`，只是将文献移至Zotero的回收站中。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504101419.png)

**但是，文献的PDF其实还保留在本地并未删除。**

这有点类似Windows或者Mac电脑的回收站或废纸篓功能，如果不清空回收站，你可以随时从回收站中恢复之前删除的文献。

所以，**这其实是一种安全机制**，而且是必要的。毕竟对科研工作者而言，文献是非常重要的资料。

那么，**如果想让文献的附件彻底地从本地删除**，只需要右键Zotero的**Trash**，并选择`Empty Trash`。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504102052.png)

### 演示如何彻底删除文献在坚果云中的附件

上面说了通过`Empty Trash`可以将文献的附件从本地删除，这里的本地指的是Zotero的`Storage`文件夹。（在`Zotero首选项-->高级-->数据存储位置`中可以找到）。

**那么，从本地删除是否就意味着从坚果云中删除了呢？**（可参考[详解【Zotero+PaperShip+坚果云】文献生态的同步机制！](https://mp.weixin.qq.com/s/olEovZrzrapKQALUMxtGtA)）

为了让大家更加信服，我来演示下。

因为是为了验证能否从坚果云中删除附件，为此我先在坚果云客户端查看下**最近更新**，可以看到上一次更新时间是`10:25`。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504105219.png)

假定我想删除Zotero中的下面这篇文献。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504103903.png)

通过右键菜单的`Show File`，我们打开该文献在本地的附件。可以看到附件是保存在一个以8个字符命名的本地文件夹中，没有毛病。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504104006.png)

接着，我右键文献，选择“**Move Item to Trash**”，即将其移至回收站。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504104112.png)

打开Zotero的回收站看下，该文献确实移至回收站了，没毛病。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504113023.png)

通过`Empty Trash`，我们清空回收站。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504104342.png)

清空完毕，干干净净。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504104418.png)

此时发现，前面通过`Show File`打开的本地附件窗口自动消失了，因为不存在了自然就消失了，验证了确实删除了本地附件。

到此还未结束。

由于Zotero的`Storage`文件夹和坚果云WebDAV是关联的，本地少了或者多了什么文件，执行同步之后，坚果云也会增加或者删除相应的文件。

为此，我们选择Zotero的`My Libraray`，并点击右上角的`同步`按钮。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504105100.png)

同步完成后，再查看下坚果云的**最近更新**，可以看到新增了两条删除记录，时间为`10:29`。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504105453.png)

而且这两个被删除的文件的名称是一样的，只是后缀不一样。我们打开坚果云官网的Zotero目录，可以看到每一条文献都对应着`.zip`和`.prop`两个格式的文件。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504105702.png)

所以可以确信，`10:29`分的两条删除记录，**意味着我刚刚从Zotero中所删除文献的附件彻底从坚果云中清除了。**

也就是说，你的坚果云存储空间腾出来了一丢丢。

到此，就完成了对粉丝的问题“**为何从Zotero删除文献后，附件依然在坚果云中？这很占空间啊！**”的回答。

### Zotero“删除“快捷键

除了通过右键菜单完成`删除`动作，通过快捷键实现也是一个非常不错的选择，这也是我平时的使用习惯。

以Mac版Zotero为例，`Delete`键对应着**Remove Item from Collection**，`CMD+Delete`键对应着**Move Item to Trash**。

对于Windows版Zotero，可以参考[Zotero官网快捷键介绍](https://www.zotero.org/support/kb/keyboard_shortcuts "Zotero官网快捷键介绍")页面

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200504111219.png)

### 总结

通过上面详细的介绍，相信大家对Zotero的`删除`功能有了一个深度的认识！

更多Zotero方面的内容，可以阅读本文头部的专辑**Zotero \| 打造最佳文献生态**。

