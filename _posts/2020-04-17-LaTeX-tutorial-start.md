---
layout: post
title: LaTeX | 为学术论文排版而生【入门篇】
date: 2020-04-17 22:36:00
tags: 
- LaTeX
published: true
---

**LaTeX专栏**又来了！

- 年久失修，**LaTeX专栏**之前推送的部分内容已经过时了，因此需要更新和扩充下。
- 之前**LaTeX专栏**部分文章的排版已经不适应现在的微信暗黑模式了，为了给大家带来更好的阅读体验，迫切需要调整排版。
- 有不少学员在微信群或者知识星球问起LaTeX相关的内容，因此有必要针对他们的问题，将相关答案补充进来。当然，**LaTeX专栏**后期还会推送更多新的内容，并在[荔枝微课](https://mp.weixin.qq.com/s/MTM6kzQJE--yhnOOB7txeg)录制原创视频。

在开始本文前，先给大家下一个基调：**精通LaTeX很难，但是让LaTeX满足日常排版需求并不难**。

Ok，准备入坑吧！

### 什么是LaTeX?

LaTeX是一种高质量的排版系统，在20世纪80年代由美国的**Leslie Lamport**开发（那时叫做TeX），并发展至今。

LaTeX主要用于长篇技术或科技文档排版，不过实际上它几乎可以用于任何类型的发行物的排版。

LaTeX鼓励用户不要过多地担忧写出来的文档的外观是怎么样的，而应该**专注在你所要写的内容上**。

举个例子，考虑下面的内容：

```
Introduction to  LaTeX
CATQ
April 2020

Hello world!
```

在最常用的文字处理软件**Word**中，如果想要产生以上内容，我们必须决定哪一部分采用什么样的格式，比如标题采用`18pt Times Roman` 字体，姓名采用`12pt Times Italic` 字体等。

这样的排版方式通常会产生两种后果：

- 作者需要花费很多时间在排版上。
- 往往排版的效果很糟糕，特别是涉及到大篇幅、多格式的时候。

而LaTeX的设计思想是：**排版的事情交给LaTeX就好，作者只需专注于写作。**

所以，在LaTeX中，你只需要这样输入：

```tex
\documentclass{article}
\title{Introduction to \LaTeX}
\author{CATQ}
\date{April 2020}
\begin{document}
   \maketitle
   Hello world!
\end{document}
```

如果要翻译一下上面的每一句代码，意思就是：

- 这篇文档的类型是**论文(article)**。

- 这篇文档的标题是**Introduction to LaTeX**。

- 这篇文档的作者是**CATQ**。

- 这篇文档的写作日期是**April 2020**。

- 这篇文档的内容是**Hello World**。

  

上述代码编译之后输出PDF，结果为：

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200417122324.png)

所以，看到了吧，用LaTeX排版文档就像是在写程序一样，而且风格有点类似`HTML`和`Markdown`这种标记语言，只是要比Markdown要复杂很多。

这就是为什么Markdown适合于博客或者文学创作这种对格式要求不是那么高的领域，而LaTeX更多用于学术论文排版，特别是涉及数学公式较多的数理/工程领域。

### 选择哪款工具？

LaTeX开发工具的类型非常之多，这里我就不一一列出来，因为这只会给新手带来困扰，并无益处。（如果你感兴趣，可以阅读[这个网页](https://www.latexstudio.net/archives/51801.html "LaTeX开发工具")）

既然你看了这篇文章，我就会直接告诉你我心目中最好的LaTeX开发工具。

首先需要说明的是，LaTeX由`编译系统 + 编辑器`两部分组成，简单点说，编译系统集成了LaTeX宏包，编辑器用于编写上面所述的LaTeX代码，即你需要写的内容。

**编译系统必须有一个，编辑器则可以有多个**。编辑器会自动调用编译系统对你所写的代码进行编译，从而输出最终的PDF文档。

LaTeX在`Windows`、`macOS`、`Linux上`都有相应的发行版。

下面主要说说Windows和Mac上LaTeX开发工具的选择。

#### Windows

Windows上我推荐大家使用`TeXlive`，这是目前主流的TeX发行版。

几乎每年更新一个版本，因此对宏包的维护非常及时高效。而且，TeXlive对中英文的支持都很不错

至于其他发行版比如`CTEX`，由于近些年CTEX更新较慢或者不再更新，很多宏包没有得到维护，因此不推荐大家使用。

下面提供三个下载TeXlive的渠道，有官网链接，也有Utah镜像，以及国内的清华大学、中国科学技术大学镜像。

推荐通过国内镜像网站下载，下载速度更快点，毕竟一个TeXlive安装包有好几个GB大小呢。

**官网**：https://www.tug.org/texlive/acquire-netinstall.html

**Utah镜像**：http://ctan.math.utah.edu/ctan/tex-archive/systems/texlive/Images/

**清华大学镜像**：https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/Images/

**中国科学技术大学镜像**：https://mirrors.ustc.edu.cn/CTAN/systems/texlive/Images/

大家选择当年最新的版本即可，比如最近刚出来的2020版TeXlive的安装包名称为`texlive2020-20200406.iso`。

顺便贴一个[TeXlive的安装方法](https://zhuanlan.zhihu.com/p/41855480 "TeXlive的安装方法")。

#### macOS

Mac上的TeX发行版就没有Windows上那么复杂了，只有`MacTeX`，可以很好地支持中英文。

同样，这里将MacTeX的下载链接贴出来，有官网和中国科学技术大学镜像可供选择，推荐使用中国科学技术大学镜像。

**MacTeX官网**：http://tug.org/cgi-bin/mactex-download/MacTeX.pkg

**中国科学技术大学镜像**：https://mirrors.ustc.edu.cn/CTAN/systems/mac/mactex/

#### 编辑器

LaTeX编辑器我推荐使用`TeXstudio`和`Sublime Text`。

**TeXstudio**的下载渠道主要有官网和Sourceforge。👇

TeXstudio官网：https://www.texstudio.org

Sourceforge：https://sourceforge.net/projects/texstudio/。

**Sublime Text**配置LaTeX环境的方法请参考我之前的推文：[【Sublime + LaTeX + 代码自动补全】，走起！](https://mp.weixin.qq.com/s/P8G1_nrhf9cEOd1ph-9DQQ)

LaTeX的【入门篇】就讲到这里，看完这篇文章你的任务就是：下载好TeX发行版和编辑器，并熟悉熟悉，下一期会推送LaTeX的语法，就要进入正题了！

所以，你入门了吗？