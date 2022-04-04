---
layout: post
title: 重磅：Zotero + Connected Papers，打造可视化文献网络！
date: 2020-12-08 22:36:00
tags: 
- Zotero
- 文献分析
published: true
---





[Connected Papers](https://www.connectedpapers.com/ "Connected Papers")，一个广受欢迎的文献可视化工具，深受科研人员青睐。

如果你是第一次听说它，那真应该好好了解下。

> 将你感兴趣的论文输入到Connected Papers，Connected Papers便能够以**可视化的方式**，自动生成与该论文有关的**文献网络**，帮助你**挖掘出更多重要文献**。

先看一下Connected Papers的外观！

![Connected Papers深色模式](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201210082217.png)

![Connected Papers浅色模式](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201208171122.png)

**Connected Papers支持深色和浅色两种模式**，颜值还是很在线的。

那么问题来了，既然Connected Papers的输入参数是某篇文献，那么将其和Zotero结合岂不是很棒！

**今天这篇文章就介绍下Zotero和Connected Papers的联动方法**，后面还会推送另一篇详细介绍Connected Papers的使用方法。

### Zotero联动Connected Papers

为了实现Zotero与Connected Papers的联动，我写了一个Zotero搜索引擎。👇

![Zotero搜索引擎：Connected Papers](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201208173028.png)

选中一篇文献，然后在右上角的搜索引擎列表中选择**Connected Papers**，或者按下快捷键`CMD+E`或者`Ctrl+E`（前提是配置了[Zutilo](https://mp.weixin.qq.com/s/KtSAUPDlAzHbzBAVYi5AeA)）。

此时会跳转到浏览器，自动在Connected Papers内搜索该文献。

一般来说，搜索结果中的第一条就是该文献。👇

![搜索结果](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201208183214.png)

点击该文献，便会自动生成一个可视化的文献网络。（别说，还蛮炫酷的）

![可视化文献网络](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201208183403.png)

该网络反映了目标文献与其他文献的关系。

一般而言，距离目标文献**越近且圆圈⭕️越大**的文献越为重要。

***距离越近代表与目标文献相似度高，圈越大代表该文献的被引次数高，圈的颜色深浅反映该文献的发表年限远近。***

当然，Connected Papers还有更多有意思的功能，后面再专门推文介绍。

**总之，在文献分析工具中（其他的诸如HistCite、CiteSpace），Connected Papers的实用性还是很强的。**

下面介绍下Connected Papers搜索引擎的配置。


#### Connected Papers搜索引擎的配置

首先，在`青柠学术`公众号后台回复`Connected Papers`获取搜索引擎配置代码。

然后在Zotero的首选项中按照下图，打开Zotero的数据目录。

![打开Zotero数据目录](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201208184935.png)

然后进入文件夹`Zotero-->locate`，打开**engines.json**文件。

![打开engines.json](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201208185104.png)

然后将获取的配置代码粘贴到想要的位置，记得在后面添加`逗号`。

![粘贴搜索引擎配置代码](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201208185258.png)

保存代码，然后重启Zotero，便能从搜索引擎中找到Connected Papers了！

这里，对于Mac用户再补充一点：

如果你想通过快捷键一键调用Connected Papers搜索引擎，可以参考下面这篇文章，将Connected Papers的名称改为**N-Connected Papers**。

[如何更高效地使用Zotero搜索引擎？](https://mp.weixin.qq.com/s/FvnlnkToRnFtc1v7IQRmYA)

即代码为：

![N-Connected Papers](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201208190113.png)

搜索引擎是这个样子。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201208190043.png)

至此，选中某篇文献后，只需要分别按下`CMD+E`和`CMD+N`即可快速跳转到Connected Papers网站，对该文献建立可视化网络。

本文就到这里，如果对你有所帮助，欢迎文末三连！

---

`温馨提示`：如果想要获取**全部搜索引擎配置代码**（包含**一键查询中英文期刊影响因子**等信息的搜索引擎），可以文末加入会员，同时还可以获取近期青柠学术发布的**首个真正意义上支持中英文混排的GB/T 7714 Zotero参考文献排版格式**。


