---
layout: post
title: Zotero + Web of Science，如何做文献泛读？
date: 2020-09-26 22:36:00
tags: 
- Zotero
published: true
---



今天，有学员在微信群提到「文献泛读」相关的问题，本文就聊聊如何使用Zotero + Web of Science做文献泛读。

> 这里说的文献泛读是指：**在大量文献检索后，希望通过阅读「摘要」粗略了解文章的主要内容，从而确定是否符合自己所需，以及是否值得进一步精度。**

所以，抓住关键词「**阅读摘要**」。

接下来看看如何实现。

### Zotero + Web of Science

打开[Web of Science](http://apps.webofknowledge.com "Web of Science官网")，选择**Web of Science核心合集**。👇

![Web of Science核心合集](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914180253.png)

根据自己的需要，检索相应关键词，比如是`Flexible Electronics`，得到以下结果，共有15232条记录。

![检索结果](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914191503.png)

根据你的需要对搜索结果进行排序。

其中，按照**被引频次**排序用得较多，可以优先筛选出影响力较高的文章；或者按照**日期**排序，可以查看最新发表的文献。

这里以**被引频次**排序为例。

![检索结果排序](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914180809.png)

然后点击**导出为其他文件格式**。

![导出为其他文件格式](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914191537.png)

根据自己需要，选择导出文献的数量， 比如我选择**记录来源：1-200**；「记录内容」选择**作者、标题、来源出版物、摘要**；「文件格式」选择**纯文本**。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914191619.png)

点击**导出**，会自动下载一个`.txt`文件。

打开txt文件，全选所有内容并复制。

![复制所有内容](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914192131.png)

打开Zotero，建立一个文献集（文件夹），比如叫做`WOS`。

然后，点击菜单栏`File-->Import from Clipboard`。
![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914192255.png)

Zotero便会自动将所有200条文献记录导入到`WOS`文件夹中。👇


![成功导入所有文献，并含摘要](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914192534.png)

核对一下数量，确实为200条，没毛病。

![共200条记录](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914192723.png)

而且，所有文献都包含「**摘要**」。

到此，就实现了我们的目标：**一次性导入大量包含摘要的文献**。

接着，就可以在Zotero内通过阅读「摘要」来挑选重点文章了。

建议[关闭左侧的目录](https://mp.weixin.qq.com/s/KtSAUPDlAzHbzBAVYi5AeA)，扩大右侧的属性面板，方便阅读摘要。


![调整阅读视图](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914193352.png)


对于重点文献，可以通过[颜色标签](https://mp.weixin.qq.com/s/qGsvW2V1OFrm_hGdUenkFg)进行标记。

![使用「颜色标签」标记重点文献](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914193606.png)

如果想进一步精度，可以直接调用Zotero右侧的View Online搜索引擎，跳转到期刊网页进行阅读。

![通过「搜索引擎」跳转到网页阅读](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914194152.png)

又或者，通过右键菜单**Find Available PDF**调用[SciHub](https://mp.weixin.qq.com/s/fFSdjhc09YzgztLzFCl8YQ)自动下载文献PDF，然后阅读，也是个非常不错的选择！

![调用SciHub下载文献](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200914195207.png)

这得益于：通过**作者、标题、来源出版物、摘要**从WOS导出来的文献不仅包含摘要，更包含DOI，因此可以直接调用SciHub下载文献，完美！

### 总结

可以看到，得益于Zotero的强大能力，我们可以挖掘出很多有趣的玩法！

如果本文对你有所帮助，欢迎**点赞、分享、转发**！