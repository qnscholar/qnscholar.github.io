---
layout: post
title: 我的 LaTeX 实验笔记模板，请收下！
date: 2021-09-19 22:36:00
tags: 
- LaTeX
published: true
---



理工科研究生的科研生活，往往离不开各种实验。

> 做好实验记录和笔记是一个很好的习惯，对于**摸索实验参数、发现实验现象、积累论文数据**都是有利的。




有的人喜欢拿个小本本记笔记，有利于加强记忆，但是缺点是容易丢。

随着各种云笔记的涌现，越来越多的人喜欢**记电子笔记**，比如wolai的模板中心就有一个「实验记录」模板。

![wolai 模板中心 - 实验记录](https://gitee.com/qnscholar/figurebed/raw/master/img/20210919184521.png)

我个人也更喜欢电子笔记，**不会丢失，容易修改和整理，而且可以多端同步，便于随时随地查看。**

读博的时候，我主要用下面两个工具记实验笔记：

1. **iPhone备忘录**：主要用于快速记录第一手笔记，简单快捷，同步方便。
2. **LaTeX笔记模板**：博一时自制的一个模板，用于笔记的后期整理，特别针对繁琐步骤的关键实验。

可能有人会问，LaTeX那么麻烦，用它做实验笔记是不是太费劲了？

坦白说，博一时，我用LaTeX记录实验笔记，主要是为了加强对LaTeX的熟练程度。

因为我那个时候在跟着《LaTeX入门 刘海洋》这本书学习LaTeX，自制LaTeX实验笔记模板相当于学以致用。

下面，将我的LaTeX实验笔记模板分享给大家，LaTeX爱好者们可以了解下。


#### LaTeX实验笔记模板

既然是自制，我对它的颜值还是有些要求的。😂

如下图，首先我用CorelDraw设计了一个笔记封面。

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;box-shadow: 0px 4px 20px -5px #84A1A8;
  object-fit:contain;" src="https://gitee.com/qnscholar/figurebed/raw/master/img/20210919192205.jpg" alt="往期精彩">

<span style="line-height:1;padding:0px 20px;font-size:12px;display:block;text-align:center;color:gray;">封面</span>

「我的实验笔记」这几个字的字体是：**书体坊安景臣钢笔行书**，如果你也喜欢，可以借鉴下。

ISEEmicro算是我**课题组的名字**，用了CorelDraw中的渐变字体。

最下面是**我的姓名**：H.S. Xu。

配置封面图片的代码如下图所示，替换成你做好的封面即可。

![配置封面图片](https://gitee.com/qnscholar/figurebed/raw/master/img/20210919194808.png)

还要提一下，该LaTeX模板默认适配Mac，如果你是Windows电脑，将字体改成下面的即可。

```LaTeX
\setCJKmainfont[BoldFont={黑体}]{楷体}
\setCJKsansfont[BoldFont={黑体}]{楷体}
```

字体配置所在位置。👇

![](https://gitee.com/qnscholar/figurebed/raw/master/img/20210919195213.png)


最后，给大家看一下**笔记模板的封面、目录和正文的样子。**（简洁风，不喜勿喷🤭）


<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;box-shadow: 0px 4px 20px -5px #84A1A8;
  object-fit:contain;" src="https://gitee.com/qnscholar/figurebed/raw/master/img/20210919192205.jpg" alt="往期精彩">

  <span style="line-height:1;padding:0px 20px;font-size:12px;display:block;text-align:center;color:gray;">封面</span>  

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;box-shadow: 0px 4px 20px -5px #84A1A8;
  object-fit:contain;" src="https://gitee.com/qnscholar/figurebed/raw/master/img/20210920082432.jpg" alt="往期精彩">

 <span style="line-height:1;padding:0px 20px;font-size:12px;display:block;text-align:center;color:gray;">目录</span> 



<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;box-shadow: 0px 4px 20px -5px #84A1A8;
  object-fit:contain;" src="https://gitee.com/qnscholar/figurebed/raw/master/img/20210919195700.jpg" alt="往期精彩">

<span style="line-height:1;padding:0px 20px;font-size:12px;display:block;text-align:center;color:gray;">正文</span>

#### 下载

***LaTeX实验笔记模板下载***：`青柠学术`公众号后台回复`实验笔记`获取。

Ps：请以XeLaTeX方式编译。