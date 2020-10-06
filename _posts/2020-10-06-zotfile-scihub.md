---
layout: post
title: ZotFile + Sci-Hub，巧妙玩转PDF下载！
date: 2020-10-06 22:36:00
tags: 
- Zotero
published: true
---

ZotFile作为Zotero最重要的插件之一，在[附件重命名](https://mp.weixin.qq.com/s/n-pr7QoyDdYGfWcrXT78Fw)、[文献同步](https://mp.weixin.qq.com/s/0heWcOlwgrF6GHmPTc-poA)、[平板设置](https://mp.weixin.qq.com/s/uHOY2a_EZqJAQOrB2v9rFQ)等方面都发挥着重要作用。

### Attach New File功能

可是，很多用户忽略了它的一个小功能，也就是下图所示的`Attach New File`路径设置。

![新文件监控目录设置](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201006170242.png)

该路径用于监控指定路径内所产生的新文件（一般为PDF）。

一旦指定路径内产生了新文件，我们则可以将该文件作为某个文献条目的附件。

下面来看看该怎么用。

**推荐将该路径设置为电脑的下载目录**，如上图所示。

这是因为默认情况下，电脑浏览器（比如Safari）的下载路径为系统的Download文件夹。

设置完毕后，假如我们从网页下载了某篇文献的PDF到下载目录。

接着，在Zotero中选中一篇没有PDF附件的文献条目，然后右键选择`Attach New File`。

![Attach New File](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201006171342.png)

提示是否将该PDF设置为附件，点击OK。

![点击OK](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201006171426.png)

便可以将该PDF设置为这篇文献的附件。

![完成PDF附件的绑定](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201006171723.png)

那么，`Attach New File`功能究竟什么情况下能用到呢？

当你使用Zotero Connector从浏览器抓取文献时，很顺利地抓取到了题录，却因为各种原因无法抓取附件，比如**网络的问题、翻译器的问题、或者数据库权限的问题**。

那么此时不妨先把题录抓取到Zotero中，然后再想办法手动下载该文献的PDF，比如在SciHub中下载。

成功下载PDF至电脑的下载目录后，再利用`Attach New File`功能将该PDF绑定至相应文献。

### ZotFile + Sci-Hub搜索引擎

**还有一种搭配Zotero搜索引擎的玩法**，这里也介绍给大家。

很多时候，如果我们选择从Google Scholar或者Web of Science抓取文献，一些文献是无法抓取到PDF的（毕竟不是在期刊页面直接抓取）。

那么，和前面一样，我们先把题录抓取至Zotero。

选中想要绑定附件的某篇文献，观察其有没有DOI，如果没有可以通过[zotero-shortdoi](https://mp.weixin.qq.com/s/ddJ_liehAU0fJ7M8B-Hrzg)插件更新。

接着，点击搜索引擎列表内的Sci-Hub DOI。

![搜索引擎【Sci-Hub DOI】](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201006173413.png)

即可自动跳转到Sci-Hub上该文献的PDF链接。（前提Sci-Hub上有资源）

![跳转至Sci-Hub下载文献](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201006173546.png)

得益于Sci-Hub的强大，通常都能找到PDF。

接着，在上述Sci-Hub页面下载PDF至电脑的Download文件夹，再使用`Attach New File`绑定至文献条目，完美！

所以，到此可以看到，将Zotero的一些小功能结合起来，会有意想不到的效果。

### Sci-Hub搜索引擎源码分享

这里我把Sci-Hub搜索引擎的源码分享给大家。👇

**下载方式：**`青柠学术`公众号后台回复`SciHub引擎`。