---
layout: post
title: Zotfile+同步盘，实现Zotero文献跨平台同步！
date: 2020-02-26 22:36:00
tags: 
- 文献管理与信息分析
- Zotero
---

粗略码字，待重新编辑。

-----

之前向大家了采用【Zotero+坚果云】组合实现Zotero文献同步。这种方式借助于WebDAV，实现了Zotero附件的直接同步，且在macOS、Windows、和PaperShip端都可以下载并查看PDF。站在Zotero的角度，这种方式的特点是“文件同步”。

今天介绍下采用【Zotfile+同步盘】实现Zotero文献同步。从Zotero的角度，这种方式并非“文件同步”，而是“文件链接同步”，具体什么含义我们往下看。

为了避免冲突以及易于理解，下面的设置仅仅针对【Zotfile+同步盘】方式。

打开Zotero首选项，在同步中，我们取消勾选附件同步，如下👇。

![](https://tva1.sinaimg.cn/large/0082zybply1gca6sjbp1qj30js0jcab9.jpg)

在advanced-Files and Folders中，我们设置下Data Directory Location，可以选择默认，也可以自定义路径，无需网盘路径，本地路径即可。注意路径中最好不好包含中文。

我设置的是`/Users/iseexuhs/Zotero`，可以看到是个本地目录。

![](https://tva1.sinaimg.cn/large/0082zybply1gca6tqtaj3j30js0inmyk.jpg)

安装Zotfile插件，在设置中，我们将Source Folders for Attaching New files设置为上一步Data Directory Location路径中的storage文件夹，即`Data Directory Location/storage`，如下。该路径用于Zotfile监视Zotero产生的新文件（比如拖入一篇pdf或者从浏览器用Zotero Connector下载一篇文献），那么，监视到了新文件做什么呢？继续往下看。

同样是下图，在Location of Files中，通过自定义，将其路径自定义同步盘中的一个文件夹，比如我设置的是OneDrive/Zotero/zotero_attachments。

该目录的作用就是将上一步路径中监视到的新文件移动（非复制）到同步盘中，而且是实实在在的pdf移动，占用网盘的空间。相当于产生了几个pdf，就移动几个pdf，注意到了吗，只有pdf，没有其他文件，搭配下图的`use subfolder defined by`还可对pdf进行分类，默认以`期刊名/年份`分类。而坚果云WebDAV方式中，pdf是存在storage中以8位数字和字母命名的文件夹内。

![](https://tva1.sinaimg.cn/large/0082zybply1gca6xtif9ij30k60lvjt6.jpg)

接着，我们再来到Zotero首选项中，在Linked Attachment Base Directory中，我们将路径设置的和上面一步Location of Files一样。

这一步很多人不太理解，特别是`链接文件的根目录`这个词的含义。我们可以这么理解，首先设置这个目录的目的是为Location of Files中每个pdf都产生一个相对路径，一个相对路径即一个`链接文件`，准确来说是`文件链接`，因为这个路径仅仅是一个链接，并非一个文件，却又指向了文件。什么意思呢？

这个相对路径有点类似于快捷方式，但又不同于快捷方式，因为快捷方式其实是一个绝对路径，而这里的链接文件产生以后，在文献同步过程中扮演着什么角色呢？意思就是这台电脑的文献通过同步盘同步到另外一台电脑后，我们如何在另外一台电脑找到每篇文献对应的PDF？只要在另一台电脑将Location of files同样设置为同步盘的相同文件夹，而Linked Attachment Base Directory也保持相同，那么，另外一台电脑就能根据相对路径找到每篇文献的pdf了。

这里就体现了相对路径的作用，因为在这台电脑上，比如Mac上，同步盘的路径可能和另外一台电脑的同步盘路径不一样，比如同步盘在另一台电脑的D盘，可是在Mac上连D盘都没有。

所以我们把两个关键词提取出来，即根目录和相对路径，`根目录`+`相对路径`=`绝对路径`没有问题吧，得到绝对路径，不论多少台电脑同步，都能找到文献PDF。

![](https://tva1.sinaimg.cn/large/0082zybply1gca75vznj5j30js0inq4c.jpg)

把以上设置的四个路径对比下。如下👇

![img](https://tva1.sinaimg.cn/large/0082zybply1gca7puvo2qj30k00akdgq.jpg)

设置好路径后，我们测试下同步效果。

随意在Zotero中建一个文件夹，拖入一篇PDF，等到自动抓取元数据后，用Zotfile进行pdf重命名（一定不可少，至关重要，否则无法同步）

![](https://tva1.sinaimg.cn/large/0082zybply1gca7v1atm9j31400p0agi.jpg)

此时，可以看到，在文献条目下，生成了一个`链接文件`，即pdf加个锁链的图标，和坚果云WebDAV方式的PDF图标不一样，也就是说一个是`链接`，一个是`文件`。也就是我们前面设置Linked Attachment Base Directory中设置的路径的真实的表现形式。

![](https://tva1.sinaimg.cn/large/0082zybply1gca7xnhhbpj31740q8q7k.jpg)

此时右击文献条目，选择show file。看到了，链接背后的文件正是前面Location of Files对应的同步盘。

注意如果我们省略zotfile 重命名这一步，该pdf是无法自动从被监听的zotero的storage文件夹内移动到网盘中的。

![](https://tva1.sinaimg.cn/large/0082zybply1gca7zqvkbhj30oi0f8dh4.jpg)

下面我们拖入一个无法抓取元数据的Pdf，如果直接用zotfile会提示失败，那是因为Zotfile重命名的根据是文献条目中的信息，没有文献条目自然无法重命名，无法重命名自然无法将pdf移动到网盘，也就无法同步。那我建议右击pdf，选择create parent item，即可生成文献条目。不过这种方式文献条目的信息是不齐全的，如果想要齐全，可以自行从浏览器用Zotero connector 保存到zotero中，然后将pdf拖到条目下，再重新执行rename，即可解决问题。

![](https://tva1.sinaimg.cn/large/0082zybply1gca85pp0ymj31400p0dk3.jpg)



那么，`链接文件`的优势在于同步盘的路径可以自由定义（全选文献，再rename一次即可），劣势在于就算删除了zotero中的一篇文献，也无法删除网盘中对应的pdf，这样会造成网盘冗余杂乱。

如果你想更换同步盘，比如从OneDrive更换到坚果云，那么只需要更改对应的路径设置，然后全选所有文献，在此Rename，即刻将pdf移动到其他同步盘。下图是存到坚果云，并建立子文件夹进行分类。

![](https://tva1.sinaimg.cn/large/0082zybply1gca8metcd3j30oi0f8wff.jpg)

