---
title: 神器！一款让Zotero具备文献预览功能的插件！
date: 2019-02-20 13:55:00
categories:
- 文献管理
tags:
- Zotero
- Zotero 预览
typora-root-url: ../../iseex.github.io
---



假定你是一个Zotero用户，现在问你这样一个问题：“你眼中的Zotero最大的缺点在哪？（特别是相对于Endnote）”



相信很多初学者的答案是：Zotero没有文献预览功能。

确实，在不安装任何插件的情况下，如果想要在Zotero中阅读某个文献，需要该文献条目，然后会在默认的PDF阅读软件中打开，如果想在一堆文献中查找一篇文献（不记得文献内容的情况下），我们必须一一打开每篇文献查看，这会导致PDF阅读软件出现一排密集的标签页。由于PDF阅读软件往往不能秒速打开文件，这种方式势必会影响文献的查找效率，特别是文献很多的情况下。再者，如果不及时关闭不需要的标签页，打开PDF很多时，PDF阅读软件很容易崩溃。所以，这种糟糕的阅读体现肯定不是任何Zotero用户希望的，特别是习惯了Endnote在右侧区域实时预览文献的用户。

那么，有没有什么办法解决上述问题呢？答案是：有。

Zotero作为一款如此受欢迎的开源文献管理软件，广大的开发者们肯定也考虑到了上述问题，并因此开发了好用的插件来武装Zotero，让其具备文献预览功能。

这款插件就是quicklook，下面具体介绍其使用方法。

访问quicklook的[Github链接](https://github.com/mronkko/ZoteroQuickLook#zoteroquicklook)可查看quicklook插件在`Windows`、`Mac`和`Linux`上的使用方法，[访问](https://github.com/mronkko/ZoteroQuickLook/releases)可下载quicklook插件（.xpi格式）。

> 这里补充下quicklook的设计思想。使用过Mac电脑的都知道，在Mac上按空格键可快速预览文件，该功能大大提高了效率，深受欢迎。quiklook正是想让Windows等其他操作系统也具备该功能。

由于`Windows`电脑暂时不在身边，下面就以在`Mac`上安装quicklook为例就行介绍。

1. 在上面给出的quicklook下载链接下载用于Mac的quicklook插件，如下图所示。  


   ![](/assets/images/posts/zotero/pdf-preview01.jpg)

2. 打开Zotero，tools->add-ons，打开插件安装界面，安装上面下载的zoteroquicklook.xpi，安装完如下图所示。


   ![](/assets/images/posts/zotero/pdf-preview02.jpg)

3. 到这里配置工作就搞定了，很简单吧。下面就是具体使用方法了。一旦安装了quicklook，在Zotero中选定一个文献条目，按下空格键，就能快速甚至极速打开文献，在弹出的预览窗口中可以翻页、放大查看，再按下空格键即可快速关闭预览窗口。如果配合上下箭头键，就能通过键盘在一堆文献中快速查找到需要的文献。此处需要注意的是，如果选定文献条目并按下Enter键，则是用Mac自带的预览软件打开文献。

   所以可以发现，这里的逻辑在于：quicklook打开和关闭非常迅速，占用内存很小，极大地提高了使用体验，逼近实时预览的效果。关注**猫Q学术派公众号**可观看我上传的具体使用效果的视频。

到这里，在`Mac`上使用quicklook便介绍完了，是不是很简单。不过需要强调的是，在`Windows`上的配置方法有些不同，除了安装quicklook插件外，还需要配以一款quicklook.exe的软件，大家可以自行摸索。

`Mac`和`Windows`上配置quicklook的所需的插件我已经从Github上下载下来，[点击这里](https://pan.baidu.com/s/1xc8yRtO11dVWsX7xSBjgxQ )可下载，密码：bbwf。

-----

*zoteroquicklook预览插件的用法纠正（更新于2019年2月20日*）

-----



之前给大家介绍过一款叫做zoteroquicklook的插件，可以让Zotero具备文献预览功能，从而让Zotero变得更加便捷（见上文）。不过，后来有一位阅读了我这篇文章的网友告诉我，我对zoteroquicklook插件的使用方法介绍有误。为此，我再次阅读了GitHub对zoteroquicklook插件的使用方法。发现确实有问题，不过该问题针对Windows平台。在这里，感谢下这位不知名的网友提供的信息！

下面我将zoteroquicklook插件在Windows 版本Zotero上的使用方法纠正下。

1. 第一步同以前一样，到[GitHub](https://github.com/mronkko/ZoteroQuickLook)上下载zoteroquicklook.xpi文件，并安装到Zotero上。
2. 下载软件QuickLook到Windows，在GitHub上提供了最新版本（以后使用过程中，为保证更好的使用体验，也要记得更新），[点击这里](https://github.com/QL-Win/QuickLook/releases)下载。说明下，其实打开QuikLook.exe即可使用，不用安装，只需要记住解压后的文件夹的路径即可。这里，我将其拷贝到了`C:\Program Files`中，方便查找。
3. 接着很重要的一步，也是之前遗漏的一步。在Zotero的菜单栏，点击Edit-->Preferences-->Advanced-->Advanced Configuration-->Config Editor，接着出现一个警告窗口，选择I accept the risk，如下图：
   ![](/assets/images/posts/zotero/accept-the-risk.png)
4. 在弹出的窗口中搜索`extensions.zoteroquicklook.customviewcommand`，双击修改value值为上一步的QuickLook软件的路径，比如我的路径为`C:\Program Files\QuickLook-3.6.4\QuickLook.exe`。如下图所示：
   ![](/assets/images/posts/zotero/config-editor-value.png)
5. 重新启动Zotero，选择一个文献条目，按下`空格键`即可预览PDF了，再按下空格键，关闭预览。结合键盘上的方向键，即可快速预览多篇文献，而且可以发现预览窗口的响应速度很快。

以上才是zoteroquicklook插件的正确使用方法。可以发现，按照正确方法来之后，Zotero的预览体验已经非常接近Mac上了！

说完预览插件的基本使用方法，这里再拓展点内容。

如前面所述，有了zoteroquicklook插件之后，按下空格键便可以预览文献，那么，假如通过预览你想要认真阅读（甚至做笔记）下该文献，这时就该用专业的文献阅读软件打开，来进一步阅读。zoteroquicklook就为我们考虑到了这点，方法如下：

下面是某篇文献的预览窗口，这里我标注了窗口上面几个好用的功能。

![](/assets/images/posts/zotero/quicklook-open-pdf.png)

可以看到，如果你想精读这篇文献，你就可以点击上图第一个箭头处的按钮，即以Windows系统默认的PDF应用（可以在电脑设置中修改）打开文献，或者点击第二个箭头处的按钮，即选择用其他应用打开文献。这里推荐先在电脑中设置下默认的PDF应用，比如我设置的应用为知之阅读（Zhizhi Reader），这样即可快速以你想用的软件来精读文献了。

还有个设置，也值得关注下。打开Zotero，点击Edit-->Preferences-->General-->Open PDFs using，这里可以自定义为喜欢的文献阅读软件，比如我同样设置为知之阅读，如下所示。这样一来，当你非常熟悉某篇文献时，即可用`鼠标双击`该文献条目，即可以知之阅读打开它了。

![](/assets/images/posts/zotero/open-pdfs.png)

总结下上面涉及到的文献打开方式：

- 按下`空格键`，实现文献预览。在预览窗口可以再选择用其他应用打开文献。
- 直接`鼠标双击`文献，即可打开文献，方便精度和批注。

> 就介绍到这里，赶紧按照上面步骤亲自操作一遍吧！祝科研顺利，文献阅读多多！更多内容可移步微信公众号“猫Q学术派”