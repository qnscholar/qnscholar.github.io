---
layout: post
title: Zoteor中存在重复文献，如何确定论文中引用的是哪一篇？
date: 2020-08-11 22:36:00
tags: 
- Zotero
published: true
---



的时候，我们会不小心往Zotero导入了重复文献，这可能会导致一种情况：

> 假如在写论文时引用了该文献，但是后期需要补全该文献的题录信息时，就不好判断到底对应了Zotero中的哪一篇，因为有重复文献存在。

**在Zotero中，每篇文献都有一个ID，就算是重复的文献，它们的ID也是不一样的**，所以你必须找对你所引用的是哪一篇文献，然后才去修改题录信息。

今天就介绍一下如何实现快速定位。

#### 快速定位重复文献

首先在Zotero的`Preferences--Cite-->Word Processors`处，取消勾选**Use classic Add Citation dialog**，如下图所示。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200811171847.png)

假如在一篇论文中引用了以下文献。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200811171952.png)

将光标放置在正文中引用文献的数字序号处，然后点击菜单栏`Zotero-->Add/Eidt Citation`，弹出下面的窗口。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200811172140.png)

单击想要修改题录信息的文献，会自动出现一个小面板，此时点击**Open in My Library**。

![Open in My Library](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200811172405.png)

即可自动在Zotero中定位到该篇文献，如下所示。👇

![文献自动定位](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200811172454.png)

至此，就成功从庞大的文献库中找到该篇文献，接着在它的属性面板修改题录信息即可。

今天就介绍到这里，下一期会介绍**如何批量提取Word中的所有参考文献到Zoteo**，敬请期待！
