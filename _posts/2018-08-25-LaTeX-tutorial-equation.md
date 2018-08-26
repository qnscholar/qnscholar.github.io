---
title: LaTeX | 为学术论文排版而生【公式篇】
date: 2018-08-25 13:45:00
categories:
- LaTeX
tags:
- LaTeX
---

> 一步一坑，继续LaTeX系列的第三篇【公式篇】，前面介绍过【入门篇】和【文本篇】。在公式编辑方面，LaTeX具有独到甚至统治性的优势，大批用户投入$LaTeX$的怀抱。今天就一起见识下它的魅力吧！


#### 论数学公式
对于理工科、经济学等方向的学生和科研人员来说，难免要与数学公式打交道，比如写报告、发表学术论文。从我自己和周围的朋友来看，排版数学公式永远是件麻烦事，特别是当公式很多很复杂时。

比如在`Word`中，插入公式很容易引起行距的变化，需要多次调整，且很容易出现**牵一发而动全身**的典型`Word`风格（此处忽略`Word`排版大神）。此外在`Word`中给公式编号也是要经过很多步骤，就算借助`MathType`也无法实现一键完成编号的程度。

目前排版数学公式的方法最常见的是：

- `Word`中自带的**插入公式**功能。

- 借助`Mathtype`。

上面这两种方法，要么折磨人，要么根本满足不了需要，这里不多说，大家都懂！：）

今天就向大家介绍排版数学公式的王者$LaTeX$。

☟，准备入坑！


#### LaTeX 数学公式语法

假如现在我们要用$LaTeX$排版**勾股定理**，编写下面的代码即可：

```latex
$a^2 + b^2 = c^2$
```
得到的效果就是：

$$a^2+b^2=c^2$$

什么！这么简单，等等，没你想得那么简单：）

因为$LaTeX$也算是一种编程语言，所有内容都需要通过代码实现，从上面勾股定理的实现代码可以看出都是由**字母搭配各种符号**构成。这里有两点：

- 字母是都知道，这不是问题。
- $LaTeX$编辑公式涉及到的符号特别多，先不说知道什么时候用哪个符号，你连把这些符号记住就不太可能了（累觉不爱，且行且珍惜：））

不过，有办法解决，后面再说。继续$LaTeX$语法。

☞ **行内公式**

所谓行内公式(`inline math`)即指公式不单独成行，而是在一句话的中间。行内公式有三种表达方式：

- `$...$`
- `\(...\)`
- `\begin{math}...\end{math}`

我们一般习惯使用`$...$`。比如我要表达**频率等于速度除以波长**这么一句话，$LaTeX$代码如下：

```latex
频率$f$等于速度$v$除以波长 $\lambda$
```

效果如下：

$$频率f等于速度v除以波长\lambda$$


是不是很简单的呢：）


☞ **行间公式**

行间公式(`display math`)指单独成行的公式，分**单行公式**和**多行公式**（后面再说）。行间公式的表达方式也有三种：

- `$$...$$`
- `\[...\]`
- `\begin{displaymath}...\end{displaymath}`

同样，一般习惯使用`$$...$$`。比如使用下面的代码实现**二次函数**的一般表达式：

```latex
$$ f(x)= ax^2 + bx + c $$
```
运行得到效果：

$$ f(x)= ax^2 + bx + c$$

怎么，是不是依然很简单，：）继续往下看。

☞ **公式编号**

公式编辑好后，往往需要对其进行编号，即公式有编号且编号自动增加。实现公式编号需要在导言区调用`{amsmath}`宏包，还得使用`equation`环境。给**二次函数一般表达式**编号的全部实现代码如下：

```latex
\documentclass[UTF8]{ctexart}
\usepackage{amsmath}
\begin{document}

\begin{equation}
         f(x)= ax^2 + bx + c 
\end{equation}

\end{document}

```
运行得到效果：

$$f(x)= ax^2 + bx + c  \qquad  (1) $$

但是，单单做到这一步还不够，因为往往文档都是有章节的，且经常碰到公式编号跟随章节序号变化的要求。这一点$LaTeX$早就为我们考虑了，而且实现方法非常简单（绝对秒杀`Word`和`MathType`）。

方法就是导言区添加：`\numberwithin{equation}{section}`

因此修改前面的代码为：

```latex
\documentclass[UTF8]{ctexart}
\usepackage{amsmath}
\numberwithin{equation}{section}
\begin{document}

\section{Math}
\begin{equation}
 f(x)= ax^2 + bx + c 
\end{equation}

\end{document}
```
运行得到效果：

$$ f(x)= ax^2 + bx + c  \qquad  (1.1)$$

到这里，可以发现用$LaTeX$编辑公式是这么简单高效。

####  你可能不知道的 MathType 功能

先设想一下：

如果能先在`MathType`里编辑好公式，然后直接拷贝到`LaTeX`里进行排版，那该有多好！这样便能将`MathType`**可见即可得**的风格与`LaTeX`**所思即所想**的风格结合起来。

事实是`MathType`确实能做到，下面具体说一下。

首先在`MatyType`中编辑好自己需要的公式，比如二次函数根的表达式：

  ![编辑公式](http://upload-images.jianshu.io/upload_images/2787497-2deafc57b09682d6.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在菜单栏选择**剪切并拷贝预置**

  ![MathType设置](http://upload-images.jianshu.io/upload_images/2787497-7d969dd47687a124.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

选择`MathMl 或 TeX`，点击确定，完成设置。

  ![MathType设置](http://upload-images.jianshu.io/upload_images/2787497-ce62ef8257c9fe13.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
然后全选编辑器好的公式，`Ctrl+C`复制。在`LaTeX`编辑器（比如`TeXstudio`）粘贴，得到：
{% highlight latex linenos%}
{% raw %}
\[x = \frac{{ - b \pm \sqrt {{b^2} - 4ac} }}{{2a}}\]
{% endraw %}
{% endhighlight %}

这里可以看出，默认情况下`MathType`采用**行间公式**`\[...\]`。

编译代码得到：

  ![编译输出](http://upload-images.jianshu.io/upload_images/2787497-49d04b0297a9892f.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


到此完成。所以可以看到，通过上述方法，我们可以在`MathType`中先编辑好比较复杂的公式，特别是涉及很多符号的公式，然后拷贝到`LaTeX`中。当然，有时满足需要，可以稍微修改下粘贴到`LaTeX`的代码，以得到更好的公式排版效果。


> 就讲到这里！