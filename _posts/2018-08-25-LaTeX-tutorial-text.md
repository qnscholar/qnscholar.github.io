---
title: LaTeX | 为学术论文排版而生【入门篇】
date: 2018-08-25 10:59:00
categories:
- LaTeX
tags:
- LaTeX
---



今天开始$LaTeX$第一篇推送，有种自己入坑，还有带着大家入坑的感觉(笑哭)。所以，在你继续往下阅读之前，我郑重说一下：

>
LaTeX不简单。

好，准备入坑吧！

### 什么是LaTeX?
LaTeX是一种高质量的排版系统，在20世纪80年代由美国的Leslie Lamport最初开发（那时叫做`TeX`），并发展至今。$LaTeX$最主要用于长篇技术或科技文档排版，不过实际上它几乎可以用于任何类型的发行物的排版。

可以说，$LaTeX$并不是一个文字处理器，$LaTeX$鼓励用户不要过多地担忧写出来的文档的外观是怎么样的，而应该专注在你所要写的内容上。

举个例子，考虑下面的内容：

```
Introduction to  LaTeX
SEEK
Jan 2017

Hello world!
```
在最常用的文字处理软件Office Word中，如果想要产生以上内容，我们必须决定哪一部分采用什么样的格式，比如标题采用`18pt Times Roman 字体`，姓名采用`12pt Times Italic `字体等。这样一种排版方式通常会产生两种后果：

- 作者需要花费很多时间在排版上。
- 往往排版的效果很糟糕。

而LaTeX的设计思想是：
> 排版的事情交给$LaTeX$就好，让作者专注于写作。

所以，在$LaTeX$中，你只需要这样输入：
```latex
\documentclass{article}
\title{Introduction to  LaTeX}
\author{SEEK}
\date{Jan 2017}
\begin{document}
   \maketitle
   Hello world!
\end{document}
```
如果要翻译一下上面的每一句代码，意思就是：
- 这篇文档的类型是`论文(article)`。
- 这篇文档的标题是`Introduction to LaTeX`。
- 这篇文档的作者是`SEEK`。
- 这篇文档的写作日期是`Jan 2017`。
- 这篇文档的内容是`Hello World`。

所以，看到了吧，用$LaTeX$排版文档就像是在写程序一样，而且风格有点类似`html`和`markdown`这种标记语言，只是要比`markdown`要复杂很多。这就是为什么`markdown`适合于博客或者文学创作这种对格式求不是那么高的领域，而$LaTeX$更多用于学术论文排版，特别是涉及数学公式较多的数理工程领域。
### LaTeX 的特点
总结一下$LaTeX$的特征就是：
- 排版期刊论文、技术报告、书籍、演示文稿。
- 对包含`章节`、`交叉引用`、`图表`的长篇文档具有很强的格式控制能力。
- 可以排版`复杂的数学公式`。
- 自动产生`目录`、`文献引用列表`和`索引序号`。
- 多国语言支持，能够很好的`支持中文`。
- 多种风格的`字体`支持。
- 开源且多平台支持，如`OS X`、`Windows`、`Linux`。

### 选择哪款工具？
每当我们学习一个`新的东西`，可能都会困惑从哪一步开始学习，那么作为学习过$LaTeX$的过来人，我想说的是首先`选好工具`。
> 君子性非异也，善假于物也。

$LaTeX$的开发工具非常之多，这里我不一一列出来，因为这只会给新手带来`困扰`，并无益处。既然你看了这篇文章，我就会直接告诉你我心目中最好的$LaTeX$开发工具。

首先需要说明的是，$LaTeX$由`编译系统+编辑器`两部分组成，简单点说`编译系统`集成了$LaTeX$宏包，`编辑器`用于编写上面所述的$LaTeX$代码，即你需要写的`内容`。且`编译系统`必须有一个，`编辑器`可以有多个，不同的`编辑器`会自动调用相同的`编译系统`对你所写的代码进行`编译`，从而输出最终的`PDF文档`。

下面小编说说`Windows和Mac`上$LaTeX$开发工具的选择（小编没用过`Linux`）。

☞ `Windows:`
- `Windows`上能支持`中英文`的`编译系统`主要有：`CTEX`和`Texlive `套装。其中`CTEX`是由国内学者开发的支持`中文`的$LaTeX$套装，方便排版`中文`文档。小编学习$LaTeX$起初也是一直用的`CTEX`套装，不过近些年`CTEX`更新较慢，很多`宏包`没有得到维护，给使用带来一些不便。`TeXlive`套装是目前更新`速度最快`、`宏包`最齐全、对`中英文`支持最好的编译系统，小编后期一直使用`TeXlive`。
- `Windows`上的编辑器我推荐`TexStudio`，`开源免费`。我个人觉得是最好用的$LaTeX$编辑器，支持代码`自动提示、补全`等功能。虽说`CTEX`、`Texlive`套装自带`TexWorks`编辑器，不过功能太单一，一般不采用。

```
CTEX传送门：http://www.ctex.org/CTeXDownload

Texlive 2016 传送门：
- 链接1：http://mirror.hust.edu.cn/CTAN/systems/texlive/Images/
- 链接2: http://www.latexstudio.net/archives/6544

TeXStudio传送门：https://sourceforge.net/projects/texstudio/

```

☞ `Mac OS X:`
- `Mac`上的`编译系统`就没有`Windows`上那么复杂了，只有`MacTeX`，可以很好地支持`中英文`。
- `Mac`上最好的$LaTeX$编辑器，个人依然认为是`TeXStudio`，`TeXStudio`有`Mac`版本哦。

```
MacTeX传送门：http://tug.org/mactex/

TeXStudio for Mac传送门：
https://sourceforge.net/projects/texstudio/

```

$LaTeX$的【入门篇】就讲到这里，看完这篇文章你的任务就是：下载好编译系统和编辑器，并熟悉熟悉，下一期会推送$LaTeX$的语法，就要进入正题了！


> 所以，你入门了吗？希望你不要从入门到放弃哦😯
