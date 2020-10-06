---
layout: post
title: 如何使用Zotero插入脚注？（赠定制版csl）
date: 2020-10-01 22:36:00
tags: 
- Zotero
published: true
---



之前多次向大家介绍了Zotero的参考文献插入功能，毕竟这是刚需。

其实，Zotero也可以插入脚注和尾注，尽管对很多人来说可能用不到，但是还是有必要了解一下。

最近有学员在微信群让我帮忙修改一个脚注格式，这让我对Zotero的脚注插入功能有了更多关注，因此今天就介绍下，并赠送给大家我定制过的GB/T 7714脚注格式。

### Zotero脚注和尾注

首先解释下什么是脚注和尾注。

在编辑长文档或书籍时，通常会对文档中的某些词语进行解释，或是要引用某参考文献，这时候就可以插入脚注和尾注，来注释文本。

> **脚注**一般位于页面的底部，作为对文档某处内容的注释，如添加在一篇论文首页下端的作者情况简介；而**尾注**一般位于文档的末尾，列出引文的出处等。 

下面介绍下，如何在Zotero中使用国标格式的脚注和尾注。

进入Zotero首选项，点击**Get Additional Styles**。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200929182810.png)

进入Zoteor的参考文献格式库。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200929182942.png)

搜索7714，点击安装下图所示格式。


![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200929183159.png)

安装完毕后，打开Word文档，点击Zotero菜单下的**Document Preferences**。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200929183651.png)

选择格式`China National Standard GB/T 7714-2015 (note, Chinese)`。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200929183836.png)

从上图中，**如果选择Footnotes，代表插入脚注；如果选择Endnotes，代表插入尾注**。

**插入脚注后的样子如下所示：**

![插入脚注](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200929212840.png)

即脚注序号为阿拉伯数字，注释内容在本页面的末尾。

**插入尾注后的样子如下所示：**

![尾注](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200929213223.png)

即尾注序号为罗马字母，注释内容在本文档的末尾。

到此，似乎自带的`China National Standard GB/T 7714-2015 (note, Chinese)`的格式一切都挺好。

但是，如果重度使用过就会发现，如果引用的是学位论文，且该学位论文的题录信息中有URL，则它的引用效果如下。

![学位论文的引用效果](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200929214214.png)

可以看到以下几个问题：
1. 文献类型显示的是D/OL，而不是D；
2. 额外增加访问日期（accessed time），即图中的[2020-09-27]，有点多余；
3. 末尾增加URL链接。

倒不是说这样的格式是错的，但是很多用户并不想要这样的显示效果，想要更简化点的。

其实，以上问题是一个学员想要改进的地方。

为此，我为他定制了一个版本，定制版csl插入脚注/尾注的效果如下。

![定制版效果](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200929214934.png)

可以看到以上问题通通解决了。

那么，这里提一下：**以中文文献来说，什么情况下文献题录的URL中会有链接呢？**

经过测试，如果使用[茉莉花（Jasminium）插件](https://mp.weixin.qq.com/s/vJng35zaX6LQ4xmKofhCRw "茉莉花（Jasminium）插件")从知网PDF抓取题录信息，会把URL信息抓取下来。

所以，如果你想要更简化的脚注/尾注效果，请使用定制版的CSL，这就分享给大家。👇

### 下载

**定制版GB/T 7714脚注/尾注格式下载**：`青柠学术`公众号后台回复`7714脚注`获取下载链接。