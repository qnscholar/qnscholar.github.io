---
layout: post
title: ZotFile + 同步盘，实现Zotero文献跨平台同步！
date: 2020-03-21 22:36:00
tags: 
- Zotero
published: true
---

说在前面：“Zotero｜打造最佳文献生态”是青柠学术主打的原创文献管理系列教程，错过的朋友可以通过下文了解。

[Zotero \| 打造最佳文献生态（合集）](https://mp.weixin.qq.com/s/yC-Bm9AfSkbk_z_Tl47Nog)

之前向大家介绍了两种方式实现Zotero文献的跨平台同步：【Zotero + 坚果云】、以及【Zotero Tablet + PDF Expert】。👇

[Zotero \| 用坚果云无限扩展文献存储空间](https://mp.weixin.qq.com/s/Vb7O_InuaHv354Kpkheryg)

[重磅 \| Zotero + Tablet，跨平台文献同步的新姿势！](https://mp.weixin.qq.com/s/uHOY2a_EZqJAQOrB2v9rFQ)

【Zotero + 坚果云】方式借助于坚果云WebDAV，实现了Zotero附件的同步，解决了Zotero自带存储空间过少的问题。

这种方式还有一个优势在于：可以实现在PC端的macOS、Windows，以及移动端的PaperShip、Zoo for Zotero之间无缝同步文献（含PDF）。

【Zotero Tablet + PDF Expert】方式很好地迎合了移动互联网时代人们的生活方式，喜欢用iPad办公或阅读文献的朋友值得尝试一下。

特别是当新一代iPad Pro喊出“你的下一台电脑，何必是电脑。”的口号后，有理由相信未来的移动端办公还有很多东西可以期待！另外，【Zotero Tablet + PDF Expert】和【Zotero+坚果云】可以同时使用，两者并不冲突！

今天介绍下另外一种实现Zotero文献同步的方式：【ZotFile + 同步盘】。不过，本文介绍【ZotFile + 同步盘】方式只是为了帮助大家更好地理解Zotero的同步机制，并不代表我推荐大家使用这种方式。

emmm...在正文开始之前，干脆先给三种方式打个分吧！

1. Zotero + 坚果云WebDAV + Papership🌟🌟🌟🌟🌟
2. Zotero Tablet + PDF Expert🌟🌟🌟🌟🌟
3. 【ZotFile + 同步盘】🌟🌟🌟

下面正式介绍【ZotFile + 同步盘】方式！

### 【ZotFile + 同步盘】的相关配置

在【ZotFile + 同步盘】同步方式中，Zotero并未负责`附件同步`的任务，而是承担了`链接附件同步`的角色。因为在这里，文献附件既没有占用Zotero自带存储空间，也未走WebDAV（比如坚果云）的流量。

这句话可能很多人看得有点懵...不慌，继续往下看，慢慢就明白了。

为了避免不同同步方式间的冲突，以下的所有设置仅仅针对【ZotFile + 同步盘】方式。

打开Zotero首选项（`Preferences`），在同步中，我们取消勾选文件同步（`File Syncing`），如下👇。做了这一步，就代表不采用Zotero自带的存储空或者WebDAV方式同步文献。

![](https://tva1.sinaimg.cn/large/0082zybply1gca6sjbp1qj30js0jcab9.jpg)

在`Advanced-->Files and Folders`中，👇我们需要设置下`Data Directory Location`，可以选择默认路径（比如我的是`/Users/iseexuhs/Zotero`）。也可以选择自定义路径，无需自定义为网盘路径，设置为本地路径即可，注意路径中最好不好包含中文。

![](https://tva1.sinaimg.cn/large/0082zybply1gca6tqtaj3j30js0inmyk.jpg)

安装ZotFile插件，在设置中，我们将`Source Folders for Attaching New files`设置为上一步`Data Directory Location`目录中`storage`文件夹的路径，即`Data Directory Location/storage`，如下。

![](https://tva1.sinaimg.cn/large/0082zybply1gca6xtif9ij30k60lvjt6.jpg)

该路径用于ZotFile监视Zotero数据目录中产生的新文件（比如拖入的一篇PDF或者从浏览器用Zotero Connector下载的一篇文献PDF）。

同样是上图，在`Location of Files`中，通过自定义，将其路径自定义同步盘中的一个文件夹，比如我设置的是OneDrive中的一个文件夹`OneDrive/Zotero/zotero_attachments`。

该目录的作用就是将监视到的`Source Folders for Attaching New files`目录中的新文件或者storage中的已有附件，通过Rename操作移动（非复制）到同步盘（比如OneDrive）中，占用的是同步盘的空间。

而且，值得注意的是，只有PDF被移动了，没有其他格式的文件。搭配上图中的`use subfolder defined by`还可对PDF进行分类，默认以`期刊名/年份`分类。

顺便提一下，在坚果云WebDAV同步方式中，PDF是存在storage中以无规则的8位数字和字母命名的文件夹内，这是一个很大区别。

接着，我们再来到Zotero首选项中，👇在`Linked Attachment Base Directory`（即`链接附件的根目录`）中，我们将路径设置的和上面一步的`Location of Files`一样。

![](https://tva1.sinaimg.cn/large/00831rSTly1gd0uozqm01j30js0inq4c.jpg)

这一步很多人有点迷，特别是`链接附件的根目录`这个词的含义。

我们可以这么理解，首先设置这个目录的目的是为`Location of Files`中的每个PDF都产生一个相对路径，一个相对路径即对应一个`链接文件`。

需要注意的是，这个路径仅仅是一个链接，并非一个文件，却又指向了文件。什么意思呢？相对路径的含义有点类似于快捷方式，但又不同于快捷方式，因为快捷方式其实是一个绝对路径。

我们首先需要弄明白，这里的链接文件产生以后，在文献同步过程中扮演着什么角色呢？👇

或者可以这么问：当这台电脑的文献通过同步盘同步到另外一台电脑后，我们如何在另外一台电脑找到每篇文献对应的PDF呢？其实，只要在另一台电脑的Zotero中将`Location of files`设置为同步盘的同一文件夹，`Linked Attachment Base Directory`也保持相同，那么，另外一台电脑的Zotero就能根据相对路径找到每篇文献的PDF了。

这里就体现了相对路径的作用，因为在这台电脑上，比如Mac上，同步盘的路径可能和另外一台电脑的同步盘路径不一样，比如在另一台电脑同步盘在D盘，可是在Mac上连D盘都没有。

现在，我们把根目录和相对路径做个加法，`根目录`+`相对路径`=`绝对路径`没有问题吧，得到绝对路径，自然就都能找到文献PDF。

不妨把上面设置的四个路径放在一块对比下，👇，便能很容易看到它们间的关系！

![](https://tva1.sinaimg.cn/large/00831rSTly1gd0smrzxvdj314c0lvtd5.jpg)

设置好路径后，我们测试下同步效果。

### 文献同步演示

随意在Zotero中建一个文件夹，拖入一篇PDF，等到自动抓取元数据后，用ZotFile进行PDF重命名（**这一步不可少！至关重要，否则无法同步文献**）

![](https://tva1.sinaimg.cn/large/0082zybply1gca7v1atm9j31400p0agi.jpg)

此时，可以看到在文献条目下，生成了一个`链接附件`，即PDF图标上加了个🔗符号，👇这和坚果云WebDAV方式的完全不一样，前面是PDF`链接`，后面是实实在在的PDF`文件`。

**这就直接导致了一个问题：采用`ZotFile链接附件方式`同步文献，在PaperShip是无法下载PDF附件的，因为附件数据既不在Zotero云端，也不在WebDAV端，PaperShip自然无法获取PDF。**

![](https://tva1.sinaimg.cn/large/0082zybply1gca7xnhhbpj31740q8q7k.jpg)

此时右击文献条目，选择`Show file`。可以看到，PDF链接对应的文件正是在前面`Location of Files`中设置的同步盘文件夹中。

**注意，如果我们省略ZotFile 重命名这一步，该PDF是无法自动从Zotero的storage文件夹内移动到网盘中的。**

![](https://tva1.sinaimg.cn/large/0082zybply1gca7zqvkbhj30oi0f8dh4.jpg)

下面我们拖入一个无法抓取元数据的PDF，如果直接用ZotFile重命名会提示失败，那是因为ZotFile重命名的根据是文献条目中的信息，没有文献条目自然无法重命名，无法重命名自然无法将PDF移动到网盘，也就无法同步。

此时，可以右键该PDF，选择`Create Parent Item`，即可生成文献条目。不过这种方式产生的文献条目信息是不齐全的，如果想要齐全，可以自行从浏览器用Zotero connector将文献保存到Zotero中，然后将PDF拖到条目下，再重新执行Rename，即可解决问题。

![](https://tva1.sinaimg.cn/large/0082zybply1gca85pp0ymj31400p0dk3.jpg)



看到这里可以发现，`链接附件`的优势在于同步盘的路径可以自由定义，几乎可以使用任何网盘。不足之处也蛮多的，比如删除了Zotero中的一篇文献后，是无法删除网盘中对应的PDF，这样会造成网盘冗余杂乱；此外，链接附件看起来总是很别扭！

如果你想更换同步盘，比如从OneDrive更换到坚果云，那么只需要更改对应的路径设置，然后全选所有文献，再次Rename，即可将PDF移动到其他同步盘。下图是在坚果云中，建立子文件夹（`subfolder`）对文献进行分类的一个例子。👇

![](https://tva1.sinaimg.cn/large/0082zybply1gca8metcd3j30oi0f8wff.jpg)

### 总结与对比

最后，将【Zotero官网自带存储空间】、【Zotero + 坚果云WebDAV】、【Zotero Tablet + PDF Expert】、【ZotFile + 同步盘】以及还未介绍【软链接 + 同步盘】五种同步方式进行对比分析。

#### 附件类型对比

同步`文件`型附件的有：

- 【Zotero + 坚果云WebDAV】
- 【Zotero Tablet + PDF Expert】
- 【软链接 + 同步盘】（以后介绍）
- Zotero官网自带存储空间

同步`链接文件`型附件的有：

- 【ZotFile + 同步盘】

#### 优劣势分析

**【Zotero官网自带存储空间】**👇

- 优势：

  - 官方存储空间安全可靠。

- 劣势：
  - 存储空间非常有限，完全不够用。

**【Zotero + 坚果云】**👇

- 优势：

  - 可以实现在PC端的macOS、Windows，以及移动端的PaperShip、Zoo for Zotero之间无缝同步文献（含PDF）。
  - 解决了Zotero自带存储空间不足的问题。
  - 同步速度快，坚果云体验好。

- 劣势：
  - 国内支持WebDAV的知名网盘公司估计也就只有坚果云了，没有其他好的选择。
  - 如果你的文献数量过多，或者当你把Zotero当作知识管理工具，而不仅仅是文献管理工具时，坚果云的免费空间估计不够你用。（我就是购买的专业版坚果云）
  - 无法对本地的PDF进行分类存储。

**【Zotero Tablet + PDF Expert】 ** 👇

- 优势：

  - 适合喜欢移动端办公的人群，以及iPad重度用户。
	- iPad、安卓平板、甚至手机都可以用该方式，几乎没有终端类型限制。
  - 可以与【Zotero + 坚果云】搭配使用。

- 劣势：

  - 受移动端PDF阅读软件的网盘同步机制限制，目前能把**主动式无缝同步**PDF做到最好的就数PDF Expert了，其他的尚未发现。

**【ZotFile + 同步盘】**👇

- 优势：

  - 几乎没有网盘类型限制，只要你的网盘空间够，你可以随意换。
  - 路径自定义程度高，如果换了个同步盘路径，重新Rename文献即可。
  - 有利于PDF的分类存储（通过`subfolder`）。

- 劣势：

  - 配置步骤繁琐。
  - 需要Rename才能同步。
  - `链接附件`不美观，总感觉怪怪的。
  - 删除文献条目，无法同时删除同步盘中的PDF。
  - 无法在PaperShip上下载PDF附件。

**【软链接 + 同步盘】**（以后介绍）👇

- 优势：

  - 几乎没有网盘类型限制，只要你的网盘空间够，你可以随意换。

- 劣势：
  - 无法在PaperShip上下载PDF附件。
  - 同步路径自定义程度非常低。


写了这么多，到这里差不多结束了。正如我在开头所说，写本文的目的是帮助大家更好地理解Zotero的同步机制，我个人不推荐采用【ZotFile + 同步盘】方式进行跨平台文献同步的。

当然，以上所有内容仅仅是个人对【ZotFile + 同步盘】方式的理解，如果哪里有误，欢迎指正！

