---
layout: post
title: 重磅｜如何批量提取Word中的参考文献至Zotero？
date: 2020-08-13 22:36:00
tags: 
- Zotero
published: true
---




上一期向大家介绍了**Zotero中存在重复文献的情况下，如何确定Word中引用的是哪一篇？**

[Zoteor中存在重复文献，如何确定论文中引用的是哪一篇？](https://mp.weixin.qq.com/s/WBjft3TqjEwBMqcXmaURsA)

写该篇推文时，我突然想起来之前学员在微信群问到的一个问题：**如何批量提取Word中的参考文献至Zotero？**

于是我稍微探索了一番，并找到了答案。

在揭晓答案前，不妨思考下：**为什么我们想要批量提取Word中的参考文献至Zotero？**

我个人觉得最大的原因是：

> 对于在Word中引用的这些参考文献，我们希望能够**批量提取**，并在Zotero中找到它们，而且能够**一键归类**（比如放在一个文献集中），方便后期统一修改题录信息。注意这里说的**在Zotero中找到它们**指的是：找到的正好是在Word中插入的那些文献，是一一对应的关系。

所以这里的核心是**批量提取**和**一一对应**。

下面我们来看看解决方案。

#### 批量提取Word中的参考文献至Zotero

假如我在一Word文档中引用了3篇文献。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813082038.png)

**且该参考文献是通过Zotero或者Mendeley导入的，文献域代码以及正文中的引用序号依然保留（这点很重要！！）。**

保存该Word至本地。

访问网站[Reference Extractor](https://rintze.zelle.me/ref-extractor/ "Reference Extractor")。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813082429.png)

Reference Extractor，顾名思义，就是参考文献提取器。

按照下图所示，点击**选择文件**，将前面保存到本地的Word文档上传到网站。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813082606.png)

一切正常的话，会立即显示参考文献提取结果。

如下图所示，“**3 references extracted**”显示成功提取了3篇文献，并识别出了参考文献的排版格式为**journal-of-micromechanics-and-microengineering**，参考文献的输出代码也给出来了（可以修改输出格式）。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813083621.png)

到此，非常重要的一步。👇

正如前面所说，假如该Word中的参考文献都是从Zotero中插入的，而且我们希望在Zotero中一次性筛选出它们。

那么，如下图所示，我们点击**Select in Zotero**，并选择**Select xx item(s) for user library xxxx**。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813085057.png)

接着会弹出是否允许打开Zotero，点击**允许**即可。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813085258.png)

**此时，见证奇迹的时刻！**

这三篇文献会自动在My Library中处于选中状态（分散排列的，往下滚动可查看全部选中的文献）。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813085350.png)

接着，非常重要的一步，假如想要将这些参考文献归类在一个文献集中，我们可以提前建好一个文件集，比如叫做**Citation**，然后在上述的文献选中状态下，一键将它们拖拽到**Citation**文献集中。

最终形成下面的效果，完美！

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813085914.png)

**还有一种方法是通过强大的插件Zutilo实现**。👇

[重磅｜最强插件Zutilo，如何彻底改造Zotero使用效率?](https://mp.weixin.qq.com/s/KtSAUPDlAzHbzBAVYi5AeA)

首先在电脑任意的地方（比如微信的文件传输助手），将一个标签文字（比如叫做Citation）拷贝到系统剪贴板。

然后，在上述的文献选中状态，右击，并选择`Zutilo-->Paste tags from clipboard`（需要在Zutilo的首选项中调出该菜单）。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813090656.png)

此时，所有参考文献都被赋予了**Citation**标签，如下图。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813091025.png)

接着我们只需要通过**Citation**标签来筛选出所有参考文献即可。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813091127.png)

是不是也很方便啊！

至此，本文的核心内容就介绍完了！

最后，顺便提一下Reference Extractor网站的另外一个功能，也就是下图的**Copy to clipboard**。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813091311.png)

假如该Word文档是别人的，**即Word中的参考文献不是从自己的Zotero中插入的**，那么，如果你想将这些参考文献提取到你的Zotero中，此时就该使用**Copy to clipboard**功能了！

点击**Copy to clipboard**，然后打开Zotero，并点击菜单栏`File-->Import from clipboard`。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813091749.png)

此时，所有参考文献就自动导入到Zotero中了！


![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200813091740.png)


