---
title: 深入探究下Zotero是如何帮我们管理好文献的！
date: 2019-01-06 00:00:00
published: true
tags:
- Zotero
categories:
- 文献管理
typora-root-url: ../../iseex.github.io
---

之前用大量篇幅介绍了Zotero的功能、安装问题、以及相关的插件，但是一直没有系统地、详细地说明白为什么Zotero擅于管理文献，有哪些强大的功能是我们没有发掘的呢！今天就向大家道来。

## 标签功能

我在一开始接触Zotero的时候就被它强大的标签功能吸引了，可以说这是Zotero相对Endnote的一个很大的优势。那么，标签功能有哪些好处呢？为一个文献添加标签，可以方便我们快速地在大量文献中搜索到它。比如有一篇讲人工智能的综述，考虑到后面写文章写报告会经常需要参考它，可是又担心时间久了找不到这篇文献了，那么此时就可以给它一个“人工智能”的标签，以后需要的时候直接点击该标签即可找到这篇文献。

### 如何添加标签

点击某个文献条目，在右侧属性面板的Tags中可以为它添加标签，如下图所示：

![](/assets/images/posts/zotero/add-tags.png)

有的时候，当我们将一篇PDF文献导入到Zotero的时候，Zotero会自动提出这篇文献中的标签（往往是文章的关键字），当我们点击该文献时，标签会全部列出来，这样就会导致很多我们不需要的标签产生了，因为添加标签的目的就是为这篇文献添加对我们重要的**标记**，标签多了自然不方便我们管理。如下图所示：

![](/assets/images/posts/zotero/many-tags.png)

不论是我们手动添加的标签，还是Zotero自动提取的标签，都会在左下角的面版中列出。如下图所示：

![](/assets/images/posts/zotero/tags-display.png)

由于Zotero自动提取的标签往往非常多，这样会导致我们在上图一大片标签中找到自己需要的标签变得困难。那么想到的办法是，如果自定义的标签能全部排在前面就好了。我的方法是：在每个自定义的标签前加下划线`_`。这样一来，自定义的标签便全部列在最前面了，查找起来非常方便。

### 为标签添加快捷键和颜色

为了更加高效便捷地利用标签功能，很多开发者让标签功能更加出色。相信大家都有这样的需求，比如看到了一篇很重要的文献，但是暂时没时间看，此时最担心的是后面想看它的时候找不到它了。那么我们是不是可以专门设一个标签，叫做**_read later**呢，而且按下键盘上的某个数字就可以立即给它**_read later**标签，省得手动打字添加标签。现在就教你如何做。

Zotero可以允许设置10个这样的标签（这里姑且叫做高级标签），也就是可以设置10种不同颜色和不同快捷键的标签。

1. 右击某个想要添加颜色和快捷键的标签，可以看到三个菜单项，分别是**assign color**、**rename tag**、**delete tag**，这里我们选择**assign color**，在弹出的窗口中即可设置颜色和快捷键（数字1-10），如下：
   ![](/assets/images/posts/zotero/assign-color.png)
   比如，这里我为**_read later**设置了绿色，和快捷键2，这样当我选中某个文献，然后按下键盘上的数字2，即可为它添加**_read later**标签。
2. 当然，还可以添加其他需要的高级标签，我就根据自己需要，添加了四个常见标签，分别为**_emphasis**、**_read later**、**_reading**、**_read already**，分别表示重要、稍后阅读、正在阅读、已读。而且这四个标签会自动以四种不同颜色呈现在最前面，方便点击，如下图所示：
   ![](/assets/images/posts/zotero/super-tags.png)

## 搜索功能

Zotero具有强大的搜索功能，可以在全部的文献中搜索，也可以只搜索某个文件夹。如下图，Zotero可以按照三种方式搜索。

![](/assets/images/posts/zotero/search.png)

即可以按照标题、年限、标签等多种属性来搜索，当然也可以全文搜索，这是可以选择Everything，这个功能有时非常有用。

## My  Publications

Zotero自带一个叫做**My Publications**的文件夹，这个文件夹不仅仅是存放自己发表的学术成果这么简单，还可以用来设置是否将这个文件夹的内容公开，即是否和网友们分享。这一点，感兴趣的可以自己了解下，在Zoteor网站的个人账户里有更详细的说明。这里需要提的是：

> 如果想要保存文献到My Publications，是不能直接将PDF拖到该文件夹的，必须从Zotero其他文件夹中的文献移动过去。

这里展示下我个人的My Pulications文件夹。

![](/assets/images/posts/zotero/My-publications.png)



## Group Libraries

科研的时候，为了及时跟踪研究领域的最新进展，往往我们会阅读同行的论文。又或者，可以把本实验室的师兄师姐发表过的论文看看，这时候就很有必要单独建立一个文件夹来存这些论文。Zotero自带Group Libraries文件夹，在这个文件夹下可以建立多个自文件夹，方便管理相关文献。当然也可以到Zotero网站的个人账户里设置这些Group Libraries是否公开等。这里介绍下如何创建Group Libraries。

1. 在菜单栏新建Group，填写名字（比如我填的是ISEEmicro），如下图：

   ![](/assets/images/posts/zotero/group-libraries.png)

2. 新建后，在Zotero的Group Libraries的下面就会出现ISEEmicro。右击ISEEmicro，便可以继续在ISEEmicro下面建立子文件夹，用来存放不同学者的文章。如下图所示：

   ![](/assets/images/posts/zotero/group-libraries-foldes.png)

3. 与My Pulications不同的是，可以直接从电脑中拖拽PDF到Group Libraries中。至此，Group Libraries搞定。

## PDF预览

由于Zotero不内建PDF预览器，之前我介绍过安装quicklook作为PDF预览器，不过实际发现在Windows上，quicklook打开较慢，也经常奔溃，已经严重影响体验。后来，我又找到了两款软件，分别是SumatraPDF和知之阅读，很适合作为Zotero的文献预览器。其中，SumatraPDF非常精简，打开速度超快，功能简单，适合作为PDF的阅读器（但不适合作为PDF批注软件，因为该软件不能做批注）。知之阅读器，打开速度也挺快，最重要的是它是我见过的最好用、最优秀的文献批注软件，[点击这里](http://www.zhizhireader.com)可进一步了解和下载。这里贴出官网介绍知之阅读器的照片，后面会专门介绍这款阅读器，感兴趣的可以提前了解。

![](/assets/images/posts/zotero/zhizhi-reader.png)