---
layout: post
title: 有个这个神器，制作LaTeX/Markdown表格变得如此简单！
date: 2020-04-16 22:36:00
tags: 
- LaTeX
published: true
---

LaTeX和Markdown作为`所想即所得`的排版语言，与Word等编辑器的`所见即所得`风格有明显不同。

Markdown还算简单的，但是不得不说LaTeX确实难到了很多小白，说是`从入门到放弃`丝毫不夸张。

（但是一旦你掌握了，你会被LaTeX的强大所折服，如果你是个颜值控，学习LaTeX是个不错的选择）

> 顺便提一句，Markdown编辑`Typora`已经基本做到了“所见即所得”。“所见即所得”的LaTeX编辑器其实也有，比如`texmacs`，但是并不推荐大家使用，因为一款需要编译的编程语言本身就不适合“所见即所得”。

要说LaTeX和Markdown把哪件原本很简单的事情变得复杂无比，那绝非`表格`莫属了！

现在有了Typora，Markdown表格制作现在已经变得很简单。毕竟Markdown只是一款轻量的排版语言，它制作的表格在格式上本身就是非常简易的。

LaTeX方面，`Excel2LaTeX`插件让表格制作变得更简单，但是得安装插件，略显麻烦！

今天向大家推荐一款很棒的工具[Tables Generator](https://www.tablesgenerator.com "Tables Generator")，它能帮助你快速制作LaTeX、Markdown、HTML、Text、MediaWiki等各种表格。

下图就是Tables Generator的网站截图。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200416084343.png)

首先选择想要生成的表格类型，比如是LaTeX Tables。

中间部分是表格编辑功能区，我们可以设置表格的**行列数、对齐、文字加粗/斜体、单元格的拆分\组合、单元格背景颜色**等等各种参数。总的来说，能满足基本需要了。

设置完表格格式，点击**Generate**，该表格对应的代码就在**Result**中显示了，复制所有代码到自己的编辑器即可。

#### LaTeX表格生成

以LaTeX为例，在TeXstudio中的编译效果如下。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200416090811.png)

**Tables Generator**另一个比较良心的地方在于，对于需要引入宏包的表格，它会在代码中以注释的形式告诉你需要引入哪些宏包。

比如下面这个表格，由于格式上设置了颜色，因此需要引入`xcolor`宏包。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200416090829.png)

同样，拷贝代码到TeXstudio中，并引入宏包`\usepackage[table,xcdraw]{xcolor}`，编译后得到下面的效果。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200416091059.png)

#### Markdown表格的生成

Markdown表格的生成就比较简单了，编辑好表格，将生成的代码拷贝到Markdown编辑器即可。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200416091251.png)

以Typora为例，轻轻松松就能预览表格的效果，如下。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200416091534.png)

到此，关于LaTeX​和Markdown表格的生成就介绍完了。

其他的诸如HTML和Text表格也很有用。

其中Text表格就是文本表格，很多人喜欢在.txt文档中写一些说明性的内容，比如readme文件，那么把制作好的Text表格拷贝进去就是个不错的选择，这会让你的txt文档更加好看，而且内容上更加丰富。