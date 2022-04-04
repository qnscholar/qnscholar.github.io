---
layout: post
title: Sublime + LaTeX + 代码自动补全，走起！
date: 2020-03-17 09:30:00
tags: 
- Mac生产力
- LaTeX
published: true
---

之前推送过两篇文章来介绍代码编辑神器Sublime Text，涵盖软件安装、配置、和更换主题等方面的内容。错过的朋友可通过下文了解。

[玩转Sublime Text 3 \| 软件安装与汉化（附下载链接）](https://mp.weixin.qq.com/s/eVKIuTIzkqEZsQxGcjZRSQ)

[玩转Sublime Text 3 \| 推荐几款非常棒的主题](https://mp.weixin.qq.com/s/BkBg5bbrXDCSN3xQIPFlXw)

今天聊一聊如何将Sublime Text配置成$\LaTeX$编辑器，且具备代码自动补全功能。注意：本文介绍的内容是针对macOS系统的。

首先我们需要安装软件Skim（获取方式：公众号后台回复`Skim`）。

安装完毕后，打开Skim，并点击菜单栏`Skim-->选项`，在下方窗口的`同步`标签页，勾选`检查文件变化`和`自动重新加载`，在`预设`处选择`Sublime Text`。

这样设置完后，Sublime中编译完成的PDF将自动通过Skim打开。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcxalzjshlj30dm0ayweu.jpg)

下一步是在Sublime TexT安装插件`LaTeXTools`。

打开Sublime Text，按下快捷键`CMD+Shift+P`，调出命令面板，输入`install`，并选择`Package Control:install Package`，如下所示，按Enter。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcx9q4qjs9j30pk0hmwf1.jpg)

搜索插件``LaTeXTools``，回车进行安装。

完成以上步骤后，即在Sublime中实现了$\LaTeX$环境的基本配置。（当然前提你的电脑上安装了MacTeX​内核）

不过这不是全部，如果想要在Sublime编写$\LaTeX$中文文档，还要做以下配置。

### Sublime中文LaTeX​文档配置

打开Mac电脑的终端，运行以下代码。

```
sudo tlmgr update --self sudo tlmgr install latexmk
```

在Sublime中，点击菜单`Sublime Text-->Preferences-->Package Settings-->LaTeXtools-->Settings-User`。

（如果是汉化版，则点击菜单`首选项-->Package Settings-->LaTeXtools-->Settings-User`）👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gcxb6tqxgwj315n0qmwjc.jpg)

在差不多400行处，增加下面两行代码。

```
"program" : "xelatex",
"command" : ["latexmk", "-cd", "-e", "$pdflatex = 'xelatex -interaction=nonstopmode -synctex=1 %S %O'", "-f", "-pdf"],
```

![image-20200317224218581](https://tva1.sinaimg.cn/large/00831rSTly1gcxb1jkzr9j30t90hm771.jpg)

在差不多380行处，将原来的`"builder": "traditional"`修改为`"builder": "default"`。👇

![image-20200317224324623](https://tva1.sinaimg.cn/large/00831rSTly1gcxb2p0whgj30t90hm0vu.jpg)

保存配置并关闭。到此，即为Sublime配置了$\LaTeX$中文文档编译能力。

还没结束，为了提高代码编辑效率，自动补全功能是必不可少的，就像在TeXstudio、TeXmaker等编辑器中一样。

### Sublime的LaTeX​代码自动补全

为了在Sublime中实现$\LaTeX$代码的自动补全功能，需要安装插件`LaTeX-cwl`，安装方法同前面安装`LaTeXTools`插件一样，即通过`Package Control`安装。

安装完毕，请重启Sublime。

### 效果演示

通过下面这段简单的代码演示$\LaTeX$中文文档的编写、编译和输出。

```latex
\documentclass[UTF8]{ctexart}

\begin{document}

学习 \LaTeX 使我快乐

\begin{enumerate}
\item 公式插入
\item 图片插入
\item 表格插入
\end{enumerate}

\end{document}
```

首先用一张动图演示下代码自动补全功能。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcxdj7mdoxg30oe0gkas0.gif)

从动图中可以看到，如果想要更加精准的补全，比如想要输入有序列表`\begin{enumerate}	`，我们可以输入\begine，那么`\begin{enumerate}	`会显示在第一条，按下回车，即得到下方代码。

```latex
\begin{enumerate}
\item 
\end{enumerate}
```

怎么样，还是很高效的吧！其他更多语句的自动补全，大家可以自行尝试下效果。

完整的代码编写完成后，效果如下所示，保存该`.tex`文档到本地。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcxc5we859j30q20i8aap.jpg)

此时按下`CMD+B`，即可编译该$\LaTeX$文档，如果编译不报错，则会自动在Skim中打开PDF。

为了更方便地预览编译结果，可以选择将Sublime和Skim并列显示。如下所示。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcxc9joc0sj315n0qnabe.jpg)

到此就介绍完【Sublime + $\LaTeX$ + 代码自动补全】的所有配置步骤了！如果你是个$\LaTeX$爱好者，不妨也去试一下！

总的来说，在Sublime中编译$\LaTeX$文档，能获得一个非常简洁的编辑环境，再加上Sublime和Skim都是轻量级的软件，因此整个编译过程会比较流畅。

