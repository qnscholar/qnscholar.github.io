---
title: LaTeX | 为学术论文排版而生【文本篇】
date: 2018-08-25 11:00:00
categories:
- LaTeX
tags:
- LaTeX
---



这几天一直在想该按照什么样的结构去写这个$LaTeX$栏目，才能让大家更快的上手，甚至培养对$LaTeX$的兴趣。

$LaTeX$本身非常复杂，涉及的细节非常多，不可能全部介绍，笔者能力有限，也难以做到面面俱到。因此，几经思考之后，决定突出重点，按照**入门篇**、**文本篇**、**公式篇**、**浮动体篇**、**自动化工具篇**展开本次的$LaTeX$系列。

下面就开始$LaTeX$系列的第二篇**文本篇**，所谓**文本篇**，主要涉及文字、段落、字体、页面设置等。
# 从 Hello World 说起
大家应该都有这种感觉，每当我们学习一个新东西，我们都迫不及待看到一个由自己完成的结果，因为对我们来说这意味着**至少我会用了**。只有看到希望了，后面的步子才会越迈越快。

在工程领域，这就叫做`Hello World`。学习单片机时，点亮第一个发光二极管是`Hello World`；学习C语言时，程序成功编译并输出一个字符串，叫做`Hello World`；焊接`PCB`时，`LED`成功发光了，叫做`Hello World`。

那么，$LaTeX$里的`Hello World`就是：`新建文件->敲代码->编译->输出PDF`。

咱，一步一步来。

### 新建文件 

开始之前，先说一下小编的操作环境：
系统：`Mac OS X Sierra 10.12.2`
编译器：`MacTeX`
编辑器：`TeXstudio 2.12.2`

![操作环境](http://upload-images.jianshu.io/upload_images/2787497-ec0de1416878920b.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)  

编译器和编辑器的下载可以参考上一篇推送【入门篇】。操作环境不一样没关系，`Windows`用户推荐`TeXlive 2016 + TeXstudio`。

- 打开`TeXstudio`，界面如下。新建文件，并保存为`Hello World.tex`。注意$LaTeX$文件的格式为`.TeX`。
  ![TeXstudio界面](http://upload-images.jianshu.io/upload_images/2787497-d90c61b703ea87da.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 为了对中英文有更好的支持，编码方式采用`UTF8`，如下图红色方框所示处。`TeXstudio`默认已经设置好，我们不需要管。只是如果采用其他编辑器，保存时可能需要设置编码方式，不然中文可能无法显示。
  ![编码方式设置](http://upload-images.jianshu.io/upload_images/2787497-8c49f659a50663b6.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 敲代码


今天这个`Hello World`例程的目标就是输出`Hello World`。为此，我们在`TeXstudio`的代码编辑区敲入以下代码（后面再解释具体含义）。

   ```latex
\documentclass{article}
   \begin{document}
	    Hello World
\end{document}
   ```
### 编译


编译之前，我们需要设置$LaTeX$的编译方式。随着$LaTeX$的发展，出于不同的需要，出现了很多种编译方式，如`PdfLaTeX`、$LaTeX$、`XeLaTeX`等，这里我们一般采用`XeLaTeX`，因为这种方式对中文的支持较好。 具体设置方法是进入菜单栏`TeXstudio->Preferences`，在弹出的窗口的左侧面板点击`Build`，在`Default Compiler`项选择`XeLaTeX`，并点击`OK`完成设置，如下图所示。

![编译设置](http://upload-images.jianshu.io/upload_images/2787497-994d9f1806a47b6b.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

然后，点击下图所示**编译并预览按钮**，可以看到编译成功，没有出现错误，右侧输出效果的**预览**视图。

![编译输出](http://upload-images.jianshu.io/upload_images/2787497-dae43388fd51f4be.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 输出PDF

上面的**预览**视图还不算真正的输出`PDF`，其实在我们编译的时候，`PDF`文档已经在`Hello World.tex`的根目录生成了，找到就可以了。

到这里，就算完成了`Hello World`。

-------
# 语法讲解
###  $LaTeX$文档的基本结构

```latex
\documentclass{article}
    
\begin{document}
    
\end{document}
```
上述三行代码代表了一个$LaTeX$文件`必不可少`的三个部分。

`\documentclass{article}`表示该文档的类型是`期刊（aiticle）`，$LaTeX$还支持`report（报告）`、`book（书籍）`、`beamer（幻灯片）`等多种类型。

`\begin{document}`和`\end{document}`表示文档内容的**开始**和**结束**，也就是说，所有正文内容都写在其中。`\begin{document}`前的部分我们称为**导言区**，**宏包**我们都是写在导言区，后面会具体介绍。

此外，$LaTeX$中，我们用`%`表示注释，如：
    

```latex
\documentclass{article}
%这是导言区
\begin{document}
    
\end{document}
```
### 中文支持
在$LaTeX​$中，想要支持中文非常简单，通常有两种方式：
- 调用`ctex`宏包，`\usepackage[UTF8]{ctex}`，`[ ]`代表可选项，在$LaTeX$中这是非常常见的。`[UTF8]`表示该文档采用`UTF8`编码方式。    
- 由于现在$LaTeX$对中文的支持已经很完善，因此我们可以直接使用`\documentclass[UTF8]{ctexart}`，代表该文档是`中文论文（ctex+article`。推荐使用这种方式，因为对部分的宏包的支持较好。

用下面代码做个示范。
    
```latex
\documentclass[UTF8]{ctexart}
\begin{document}
  这是第一个\LaTeX 文档
\end{document}
```

编译输出，效果如下：

![中文支持](http://upload-images.jianshu.io/upload_images/2787497-15a44f84888a2b4a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
    

这里需要提一下，上面代码中的`\LaTeX`是专门用于显示$LaTeX$的logo。又如`\TeX`可以显示`TeX`的logo，大家可以自己试试。

### 行与段落
$LaTeX$中，在一行的末尾使用`\\`表示换行，即**另起一行**。而两次按`Enter`表示**另起一段落**，即`一个空行`表示另起一段落。当然也可以用`\par`表示另起一段落。如下面代码所示：
    
```latex
\documentclass[UTF8]{ctexart}
\begin{document}
  这是第一行。\\
  这是第二行。
    	
  另起一段落,另起一段落,另起一段落,另起一段落,另起一段落,另起一段落,另起一  段落,另起一段落。\par
  另起一段落,另起一段落,另起一段落,另起一段落,另起一段落,另起一段落,另起一段落,另起一段落。
\end{document}
```

效果如下：

![段落设置](http://upload-images.jianshu.io/upload_images/2787497-1023c4d538af63cf.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

可以看出，默认段首是缩进两格的，如果想取消缩进，可以在该段落前面添加`\noindent`语句。如：
    
```latex
\documentclass[UTF8]{ctexart}
\begin{document}
   \noindent
   Hello World
\end{document}
```

### 章节

如果文档类型为`article`，我们采用`\section{章节名}`、`\subsection{章节名}`开启一个**章节**或者**次级章节**。代码如下：
    
```latex
\documentclass[UTF8]{ctexart}
\begin{document}
   \section{这是第一章节}
   Hello World
   \subsection{这是次级章节}
   Hello World
   \section{这是第二章节}
   Hello World
\end{document}
```

效果如下：

![章节设置](http://upload-images.jianshu.io/upload_images/2787497-923ea625f136af70.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

正如大家看到的，默认情况下，第一级章节标题是**居中显示**的(注意，上图预览视图的第一行是**页眉**)，显然这不符合大多数需要，为此在导言区添加一些设置章节格式的代码即可，如下：
    
```latex
\documentclass[UTF8]{ctexart}
\CTEXsetup[name={第,章}]{section}
\CTEXsetup[format={\zihao{-3}\raggedright\bfseries}]{section}
\begin{document}
   \section{这是第一章节}
   Hello World
   \subsection{这是次级章节}
   Hello World
   \section{这是第二章节}
   Hello World
\end{document}
```

得到：

![章节修正](http://upload-images.jianshu.io/upload_images/2787497-7a26df583269b6f6.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 字体设置
#### 字体选择

$LaTeX$的字体蔟非常复杂，这里不多叙述，大家可以查查资料。下面代码是用于设置正文部分中英文的默认字体分别为`Roman Times New`和`楷体-简`（`Windows`上写**楷体**即可）。其中，`xeCJK`宏包用于设置中文字体，`fontspec`宏包用于设置英文字体，将其添加到导言区即可。

```latex
\usepackage{xeCJK}
\setCJKmainfont[BoldFont={黑体-简}]{楷体-简}

\usepackage{fontspec}
\setmainfont{Times New Roman}
```

#### 字体大小

$LaTeX$中设置字体大小的方式比较多。在文档类型为**中文论文**的情况下，我通常使用`\zihao{数字}`的方式来改变字体大小，**数字**的大小表示该部分文字为**几号字体**。如下所示：

```latex
\documentclass[UTF8]{ctexart}
\CTEXsetup[name={第,章}]{section}
\CTEXsetup[format={\zihao{-3}\raggedright\bfseries}]{section}
\begin{document}
     \section{这是第一章节}
     \zihao{2}
     Hello World
     \subsection{这是次级章节}
     Hello World
     \section{这是第二章节}
     Hello World
 \end{document}
```
效果如下所示：

![字体大小设置](http://upload-images.jianshu.io/upload_images/2787497-c69db956f5e2538b.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240) 如果只想改变某部分文字的大小，可以用一对大括号`{}`括住`\zihao{数字}`和**文字**，$LaTeX$中一对大括号`{}`表示一个**环境**，环境内的**格式控制语句**只对环境中的文字起作用。如：
    

```latex
{\zihao{3} Hello World}
```


### 页面设置
#### 纸张设置

$LaTeX$中可以通过**可选项**来设置页面纸张的大小（默认为`A4`）。代码如下：

```latex
\documentclass[UTF8,a4paper]{ctexart}   
```

#### 页边距

此外，$LaTeX$可以用`geometry`宏包来设置页边距，代码如下：

```latex
\usepackage{geometry}
\geometry{left=2.5cm,right=2.5cm,top=2.0cm,bottom=2cm}
```

#### 页眉页脚

$LaTeX$中用`\pagestyle`来设置**页眉页脚**，默认为页眉显示**章节标题**和**页码**，**页脚**为空。默认风格用下面的代码表示：

```latex
\pagestyle{headings}
```

如果要取消页眉页脚，用代码：

```latex
\pagestyle{empty}
```

> $LaTeX$的【文本篇】就到这里啦，更多丰富的格式设置需要大家多**查阅资料**来学习，这里推荐大家看看**刘洋海**的《LaTeX 入门》，一本很经典的$LaTeX$参考资料！