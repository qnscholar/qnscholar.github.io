---
layout: post
title: Zotero Connector保存知网文献时，如何解决作者的“姓”和“名”分开抓取的问题？
date: 2020-03-04 12:25:00
tags: 
- Zotero
published: true
---

很多Zotero用户在抓取知网文献时，发现作者的“姓”和“名”是分开抓取的，也就是非连续的，比如作者“张三丰”，以姓“张”和名“三丰”分开显示，那么这种情况会造成什么后果呢？

以下面这篇文章为例。

![](https://tva1.sinaimg.cn/large/00831rSTly1gchsec1fqkj31740q8jvk.jpg)

可以看多作者“张一丹”的姓和名分别以“张”和“一丹”填充在Author的`Last`和`First`中，这会造成当我们用Zotero或者Zotfile重命名PDF时，PDF名称中无法完整显示作者的全名。

比如上面这篇文献用Zotero重命名后PDF的名称为“张 - 2013 - 高温环境下声表面波射频识别标签的研究.pdf”，而很多人期待的效果是“张一丹 - 2013 - 高温环境下声表面波射频识别标签的研究.pdf”。

尽管姓和名分开显示对于通过Zotero的office加载项排版参考文献不会造成影响，但是无法在PDF名称上显示全名总有点不尽人意。

这个问题有位粉丝在在青柠学术交流群向我提过，开始时我想着能否通过修改Zotfile的Rename Rules来实现。

![](https://tva1.sinaimg.cn/large/00831rSTly1gchsn0g2faj30k60lv0uc.jpg)

但是我发现目前Zotfile还没有哪个通配符能够实现显示作者的全名，顶多通过`%F`显示“姓+名字的第一个字或字母”。

既然如此我就想着从源头解决这个问题，也就是说如果Zotero Connector在抓取知网文献时，不将作者的“姓”和“名”分开，那不就自然而然解决了这个问题吗！

因此我修改了.CNKI.js脚本，将该脚本覆盖Zotero原始的.CNKI.js，并更新Zotero Connector的translators。不知道如何覆盖？可以参考文章[Zotero Connector支持中国知网「期刊和硕博论文」PDF直接下载了！](https://mp.weixin.qq.com/s/JA0ZPKQC4n0rznzuuVbCig)

再次抓取知网文献时，即可让作者的全名全部显示在Author中的`Last`中，即全名都填充在姓（Last Name）中。

这样一来以Zotero默认的Rename规则即可实现以下PDF命名效果，即实现了想要的格式。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcht77u19bj31740q878g.jpg)

再上一张一次性抓取多篇知网文献的效果截图，是不是看起来舒服很多了！

![](https://tva1.sinaimg.cn/large/00831rSTly1gcht9q8fm0j31740q810y.jpg)

这里顺便提一下，Zotero Connector在谷歌学术抓取中文文献时不会出现上述问题，因此如果你不嫌麻烦可以用谷歌学术抓取，尽管谷歌学术的中文文献没有那么齐全。

#### 修改版.CNKI.js下载

我已经将修改版.CNKI.js分享到我的知识星球，需要的可以加入星球获取。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gchtdlieauj30ku1eadjr.jpg)

