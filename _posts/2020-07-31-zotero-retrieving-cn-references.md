---
layout: post
title: 重磅！Zotero中文文献识别！它来了！
date: 2020-07-31 22:36:00
tags: 
- Zotero
published: true
---

近期，收到一封来自开发者**l0o0**的GitHub邮件。从邮件中我得知：一个重磅Zotero插件`Jasminum`诞生了！

为开发者疯狂打call👍

**万众期待的Zotero中文文献识别功能终于来了！**

来，直接上结果！

![单篇中文PDF的元数据识别](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200730000650.gif)

![批量中文PDF的元数据识别](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200730000809.gif)

**看完结果，下面来细说**。👇

### 重磅插件Jasminum诞生了

大家应该知道，在之前，如果拖入了一个PDF文件到Zotero中，只有英文文献能够自动识别（Retrieve Metadata），即能够抓取英文文献的元数据，但是中文文献是不支持的。

这是因为Zotero抓取元数据的功能是通过提取英文PDF内的部分文字内容，并和数据库进行对比来实现的。

这导致Zotero对中文PDF的元数据抓取一直没有得到支持。

所以，对于中文文献，大家一般在浏览器端用Zotero Connector来抓取文献的题录以及PDF。

尽管已经能够满足需求，但是知网等中文数据库的Zotero Connector翻译器偶尔会出现bug（不少粉丝和学员都反映），一定程度上影响了使用体验。

**今天这一切将迎来改变！**

插件`Jasminum`（中文名：`茉莉花`）为Zotero带来了中文文献的元数据抓取能力。

下面一起来看看。

在插件`Jasminum`的[GitHub网页](https://github.com/l0o0/jasminum "Jasminum插件GitHub主页")，可以看到该插件的功能介绍，也可下载`Jasminum`插件的`xpi`[文件](https://github.com/l0o0/jasminum/releases "Jasminum下载")。

（网速不好的，可以在公众号后台回复`Jasminum`获取插件）

![Jasminum插件GitHub主页](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200729234553.png)

![Jasminum插件功能介绍](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200729235053.png)

下载插件后，在Zotero进行安装。

![成功安装的Jasminum插件](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200730001437.png)

Jasminum插件目前主要有三个功能：

1. 根据知网上下载的文献文件来抓取引用信息（就是根据文件名）
2. 拆分或合并 Zotero 中条目作者姓和名
3. 为知网的学位论文PDF添加书签

#### 中文文献元数据识别

第一个功能是大家最为关心的，我已经在本文开头用动图进行了效果演示，这里再看一遍。

![演示：中文PDF的元数据识别](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200730000809.gif)

值得注意的是，**目前该插件只支持知网文献的识别**，其他中文数据库（比如万方）尚未支持，但是相信知网足以能够满足大部分人需要了。

**原理方面，它是通过文献的文件名进行识别和数据库匹配的（不同于Zotero自带的英文文献抓取原理），而且支持PDF和CAJ两种格式。**

具体来说，你的文件名需要是以下4种格式之一。

1. title_author.pdf/caj
2. title.pdf/caj
3. titlePart1_titlePart2_author.pdf/caj
3. titlePart1_titlePart2.pdf/caj

且author的汉字姓名为4字以内。👇

![需注意文件名格式](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200730002532.png)

之所以是以上4种格式，是因为一般从知网下载的文献名称都是以上4种格式之一。

比如这个样子。

![知网下载的文献名称常见格式之一](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200730002845.png)

下载了中文文献后，将它们拖入Zotero，然后选中文献（单篇或者批量），点击右键菜单中的**Retrieving CNKI Metadata**，即可完成元数据的抓取。（元数据主要用来参考文献排版）

中英文Zotero下的`Jasminum`菜单如下。👇

![英文菜单](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200730003319.png)

![中文菜单](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200730003803.png)

这里还要提醒一下，由于`Jasminum`插件是通过文件名来识别的，因此如果文件名不符合上述四种格式是无法识别的。

不过这也代表着：**如果你从其他中文数据库（万方）下载了一篇中文文献，且碰巧该文献在知网中也有，那么只要该文献的名称符合上述四种格式，也是可以成功抓取元数据的（亲测）。**

以上就是对`Jasminum`插件的知网中文文献元数据识别功能的介绍，下面介绍一下该插件的第二个功能：作者姓名的拆分或合并。

#### 作者姓名的拆分或合并

一张动图演示下作者姓名的拆分或合并。👇

![演示：作者姓名的拆分或合并](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200730004317.gif)

关于作者姓名的拆分或合并，是为了方便在PDF命名中完整显示作者的姓名。

之前在下面这篇推文中，介绍过使用ZotFile通配符的方法实现该功能。

[Zotero文献PDF命名，如何完整显示作者姓名？](https://mp.weixin.qq.com/s/9uwJHsO5u0gS6FCzv_q52w)

我个人更推荐上文中的方法，因为它是全局生效的。`Jasminum`插件则需要在手动选择文献后，才能完成作者姓名的拆分或合并。

#### 为知网的学位论文PDF添加书签

**为知网的学位论文PDF添加书签**，需要首先下载[PDFtk server](https://www.pdflabs.com/tools/pdftk-server/)。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200730010101.png)

这里就不多介绍了，感兴趣的可以自己捣鼓捣鼓。

### 下载

**Jasminum插件下载**：`青柠学术`公众号后台回复关键词`Jasminum`。

### 致谢

最后，再次感谢开发者**l0o0**的优秀作品`Jasminum`！

**Zotero变得更好用了，Zotero的中文生态更加完善了！**