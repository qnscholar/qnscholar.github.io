---
layout: post
title: Typora也能做思维导图？做笔记的又一个绝佳选择？
date: 2020-11-10 22:36:00
tags: 
- 笔记生态
- 效率工具
published: true
---



之前多次推文介绍了Typora这款优秀的Markdown编辑器。

- [Typora，每一位写作能手的Markdown利器！](https://mp.weixin.qq.com/s/CkFfWqyhde1OTOp9KMLlxw)
- [如何为Typora更换一个漂亮的主题？](https://mp.weixin.qq.com/s/Fm_9lE79HWZO0J4QxlcHgg)

最近，我试图将Zotero和Typora结合，**打造一个文献/笔记一体化的管理生态。**

在正式推出该教程之前，有必要把一些基础的内容介绍下。

今天就从笔记中常用的**思维导图**讲起。

在笔记中运用思维导图，可以方便我们归纳一些知识点，一目了然，便于记忆。

### Typora思维导图

其实Typora也可以做思维导图，尽管从语法上并不叫做思维导图，但是却形似思维导图。

Typora的流程图（Flow Chart）语法可以做出思维导图效果。

#### 横向思维导图

Typora的流程图分为横向和纵向的流程图。

具体来说，是通过mermaid语言的代码块来实现的。

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;
  object-fit:contain;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201110171820.png" alt="往期精彩">

  <span style="line-height:1;padding:0px 20px;font-size:12px;display:block;text-align:center;color:gray;">横向思维导图 - 代码示例</span>

以横向的流程图来说，加入我们输入以下代码。


即

```
graph LR
A[青柠学术]-->B[博主]
A-->C[Up主]
A-->D[社群]
B-->E[公众号]
B-->F[知乎]
C-->H[B站]
C-->I[荔枝微课]
D-->J[知识星球]
D-->K[微信群]
```

便能够生成以下思维导图的效果。

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;
  object-fit:contain;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201110172046.png" alt="往期精彩">




很良心的一点是，Typora支持实时预览代码块，也就是能够实时看到生成的思维导图，如下所示。

![实时预览思维导图](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201110172018.png)

写这样一个思维导图代码其实非常简单。

其中`mermaid`为代码块的语言，`graph LR`代表横向流程图。

框图中的每个节点用`ABCD...`代替，**相同字母代表同一节点**，节点内容在`[]`内填写。

以上是横向流程图，下面看下竖向思维导图。

#### 竖向思维导图

把`graph LR`改为`graph TD`，即为竖向思维导图。

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;
  object-fit:contain;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201110172640.png" alt="往期精彩">




即
```
graph TD
A[青柠学术]-->B[博主]
A-->C[Up主]
A-->D[社群]
B-->E[公众号]
B-->F[知乎]
C-->H[B站]
C-->I[荔枝微课]
D-->J[知识星球]
D-->K[微信群]
```

效果如下。

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;
  object-fit:contain;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201110173643.png" alt="往期精彩">




### Typora其他图表语法

除了Flow Chart，Typora还支持更多图表语法，可以按需使用。

这里列举几个。

#### Sequence Diagram（时序图）

时序图的代码示例如下：

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;
  object-fit:contain;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201110174556.png" alt="往期精彩">

 

即
```
sequenceDiagram
    Alice->>+John: Hello John, how are you?
    Alice->>+John: John, can you hear me?
    John-->>-Alice: Hi Alice, I can hear you!
    John-->>-Alice: I feel great!
```

效果如下：

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;
  object-fit:contain;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201110174520.png" alt="往期精彩">





#### State Diagram（状态图）

状态图的代码示例如下：

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;
  object-fit:contain;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201110175021.png" alt="往期精彩">





即

```
[*] --> Still
Still --> [*]
Still --> Moving
Moving --> Still
Moving --> Crash
Crash --> [*]
```
效果如下：

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:200px;
  height:100%;
  object-fit:contain;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201110175138.png" alt="往期精彩">





#### Pie Diagram（饼图）

饼图的代码示例如下：

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;
  object-fit:contain;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201110175308.png" alt="往期精彩">





即
```
pie title Pets adopted by volunteers
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 15
```
效果如下：

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;
  object-fit:contain;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201110175353.png" alt="往期精彩">



### Mermaid在线编辑器

如果你记不住以上语法规则，不妨使用网站Mermaid Live Editor。

左边选择需要的图表模板，输入内容，右边便可预览效果。

![Mermaid Live Editor](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201110180837.png)

你可以复制代码，还可以将生成的图表下载下来，或者获取URL。

虽然介绍了这么多，但是真正常用的就是流程图（Flow Chart）。

