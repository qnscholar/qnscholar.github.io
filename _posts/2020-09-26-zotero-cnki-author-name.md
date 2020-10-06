---
layout: post
title: Zotero｜更新知网翻译器后，如何实现作者姓和名的合并抓取？
date: 2020-09-27 22:36:00
tags: 
- Zotero
published: true
---



前阵子，在下面这篇推文中向大家介绍了新版知网的Zotero翻译器（translator）。

[无法抓取知网文献？该更新translator了！](https://mp.weixin.qq.com/s/84V5kmV9wwxrmhLSt0r-HQ)

可是，很多粉丝和学员反映：更新到新版翻译器后，抓取知网文献时，作者的姓和名又是分开的了，如下图所示。

![作者的姓和名分开](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200926162331.png)

其实，作者的姓和名分开显示是符合规范的，所以开发者依然坚持这么写。

但是很多用户还是希望不要分开显示，主要有以下两个原因。

**第一**，Creator处无法显示完整的作者姓名。👇

![Creator](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200926162948.png)

**第二**，对PDF进行重命名时，无法显示完整的作者姓名。

![PDF命名](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200926163244.png)

尽管在[之前的文章中](https://mp.weixin.qq.com/s/9uwJHsO5u0gS6FCzv_q52w)，介绍了通过Zotfile通配符可以解决这个问题，但是在姓名之间会多一个**逗号**，很多人不是很喜欢。

![姓名之间有逗号](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200926163820.png)

那么，今天再次分享一个经过我修改过的CNKI.js（**文末下载**），下载之后，通过[此处的方法](https://mp.weixin.qq.com/s/84V5kmV9wwxrmhLSt0r-HQ)进行翻译器的替换更新，即可实现知网文献作者的姓和名合并显示。

👇效果如下。***不论是Creator还是PDF命名形式，都符合大家习惯的方式。***

![更新后：姓和名合并显示](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200926165038.png)

不过，精彩还未结束，***后面还会介绍另外一种一劳永逸的方法，敬请期待！***

#### 下载

**修改版CNKI.js下载**：`青柠学术`公众号后台回复`知网作者`获取下载链接。