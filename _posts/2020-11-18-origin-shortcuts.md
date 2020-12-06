---
layout: post
title: 掌握这几个快捷键，Origin绘图效率大大提升！
date: 2020-11-18 22:36:00
tags: 
- 数据统计与分析
published: true
---



平时进行科研绘图，Origin和GraphPad我都在用。

Origin主要用来数据的导入和处理；GraphPad用来最终的绘图，供论文发表用。

**Origin虽强，但是相比于GraphPad，在设计上相当的不人性，特别是在文件的命名方面，简直一个天上一个地下。**

这种时候，**有必要掌握一些Origin快捷键**，让原本不太人性化的设计稍微改善一下，以提高我们绘图的效率。

今天主要介绍两个快捷键，一个和文件的命名有关，一个和数据图的导出有关。

### Table和Graph的命名统一

在GraphPad中，数据表格（Table）和数据图（Graph）在内容和命名上都是关联的，成对出现，这种设计非常好，方便我们快速找到想要查看的内容和提高绘图的效率。

Origin就缺少这种友好的设计，如果不对数据图及时命名，要准确辨识那一列Graph，简直就是灾难！

![命名不关联的Table和Graph](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201117162152.png)

 既然如此，不妨通过快捷键快速实现工作流：`复制Table的名称-->重命名Graph-->粘贴Table的名称`。

这里需要知道一点，**在Origin中真正负责文件命名的字段并非是Name，而是下面的Long Name**。Short Name局限性太大，很多字符无法在名称中显示出来。

![文件名称字段Long Name](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201117162547.png)

选中一个Table，按下快捷键`Alt+Enter`打开属性（Properties）窗口。

![Table - Long Name](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201117163657.png)

在Long Name中，给Table起个名字，比如叫做`test`，然后复制Long Name的内容。

接着选中和该Table对应的Graph，再次按下快捷键`Alt+Enter`，将上面复制的Table名称粘贴到Long Name中，点击OK。

![Graph - Long Name](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201117163638.png)

如此一来，便能快速而又无误地将Table与Graph的名称统一起来。

#### Graph导出

选中想要导出的Graph，点击菜单栏`File-->Export Graphs-->Open Dialog`，便可以导出数据图。

![Graph导出菜单](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201117164208.png)

但这总显得不够高效，这里建议采用快捷键`Ctrl+G`，按下快捷键便可以快速弹出数据图导出界面。

![Graph导出界面](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201117164431.png)

看起来不起眼的两个快捷键`Alt+Enter`和`Ctrl+G`，用得好却能带来很大的效率提升！





  