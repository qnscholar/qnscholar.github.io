---
layout: post
title: 【ZotFile+同步盘】方式如何切换到【Zotero+坚果云WebDAV】同步方式？
date: 2020-03-24 22:36:00
tags: 
- Zotero
published: true
---

前几天写了一篇推文[ZotFile + 同步盘，实现Zotero文献跨平台同步！](https://mp.weixin.qq.com/s/0heWcOlwgrF6GHmPTc-poA)，帮助大家更好地认识和理解Zotero的各种同步方式。

如果你是个Zotero新手，推荐你去阅读一下！

这篇推文发出来后，就有几位学员在微信群里说：我现在用的就是【ZotFile+同步盘】方式，我想换成坚果云WebDAV，该怎么办？

其实，这并不难，只要你真正理解了文章[ZotFile + 同步盘，实现Zotero文献跨平台同步！](https://mp.weixin.qq.com/s/0heWcOlwgrF6GHmPTc-poA)中的内容，你就能摸索出答案。

下面，我就介绍下如何从【ZotFile+同步盘】方式转到【Zotero+坚果云WebDAV】方式！

#### Zotero首选项设置

首先，在Zotero的`Preferences-->Advanced-->Files and Folders`中，需要进行一些设置。👇

![Zotero首选项设置](https://tva1.sinaimg.cn/large/00831rSTly1gd4nobg0bgj30j10hy75s.jpg)

对于`Data Directory Location`，无需改动，可以选择默认也可以自定义，反正是电脑本地的一个路径即可。

在`Linked Attachment Base Directory`下，点击`Revert to Absolute Paths`，将Zotero的附件链接方式恢复到**绝对路径方式**。

什么意思呢？就是说不再采用相对路径方式，而是使用`Data Directory Location`中设置的路径，而该路径就是文献PDF附件的绝对路径。

接着，我们再来看下ZotFile的设置。

#### ZotFile设置

点击Zotero菜单栏`Tools-->ZotFile Preferences`，来到下方窗口。👇

![ZotFile设置](https://tva1.sinaimg.cn/large/00831rSTly1gd4o0fqz8jj30h20ir407.jpg)

对于`Source Folder for Attaching New Files`，不要再让它监听Zotero的storage文件夹，因此，建议修改为电脑本地的**下载**文件夹路径，即macOS中的`Download`或者Windows中的`下载`，这一设置其实大有作用，以后会介绍。

对于`Location of Files`，一定要选择`Attach stored copy of file(s)`，否则无法切换到坚果云WebDAV方式，PaperShip中也无法下载PDF。

这一步的含义是ZotFile不再移动文献附件，而是直接采用storage文件夹的绝对路径。

到此，相关的路径设置就搞定了，下面需要将同步盘中的文献附件转移到默认的storage目录。

如果想要更快地转移，可以全选`My Library`中的文献，然后在右键菜单中点击`Rename Attachments`，即可将文献附件从同步盘转移到默认的storage目录。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gd4od98q5fj313z0n1tje.jpg)

同时，文献附件的图标也会从【PDF logo + 🔗】变为【PDF logo】。👇

![绝对附件](https://tva1.sinaimg.cn/large/00831rSTly1gd4ojjr0m5j31400n645p.jpg)

Ok，文献附件转移完毕后，就彻底取消了【ZotFile + 同步盘】方式的所有设置。

接下来，如果你想要切换为【Zotero + 坚果云WebDAV】方式，可以到`Preferences-->Syncing`进行相关的设置。

![](https://tva1.sinaimg.cn/large/00831rSTly1gd4onb65m3j30go0ldq4f.jpg)



具体的设置方法和注意事项请参考下面几篇推文，这里不重复介绍。

[Zotero \| 用坚果云无限扩展文献存储空间](https://mp.weixin.qq.com/s/Vb7O_InuaHv354Kpkheryg)

[方法更新 \| Zotero或者PaperShip绑定坚果云WebDAV时，验证失败怎么解决？](https://mp.weixin.qq.com/s/2QhDmtWu6ISgDZ9FrIdIBw)

本文到此就结束了，下课。

