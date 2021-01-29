---
layout: post
title: 双向链接｜wolai又采纳了我的两个功能更新建议！
date: 2021-01-29 22:36:00
tags: 
- Zotero
- 双向链接笔记
published: true
---



自从上一次推送了wolai和Zotero的联动教程后，👇我一直思考如果想让wolai变成一个更具生产力的科研工具，还欠缺什么功能。

[重磅｜Zotero + wolai 双向联动教程](https://mp.weixin.qq.com/s/H8KOp4XkHta8C_48pzjzDA)

结合自己最近摸索双向链接笔记软件的感悟，我向开发者提出了两个功能更新建议。

幸运的是，就在这几天，wolai在最新版本中，已经支持了这些功能。

（当然，部分功能可能之前就已经在wolai的更新计划中了...）

下面，一起来看看。

### 页面内导入文件自动填充标题

之前在视频[重磅｜Zotero + wolai 双向联动教程](https://mp.weixin.qq.com/s/H8KOp4XkHta8C_48pzjzDA)中，提到了wolai导入Markdown的功能。

**wolai目前有两种导入文件的方式：**

#### 全局导入

全局导入，在右上角的菜单处。👇

![全局导入](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210128214705.png)

一直以来，wolai全局导入文件（比如Markdown）时，新的页面会以导入文件的文件名作为页面标题。

这一点确实很好，但是全局导入的一个特点是：**会自动新建一个位于根目录的新页面。**

但是大部分时候，我们的操作顺序是：先在某个目录下新建了一个页面，然后再将markdown等文件导入。

显然全局导入不符合我们的需要。

#### 页面内导入

此时，就必须用到页面内导入了。

**但是旧版wolai的页面导入功能存在一个问题**：导入的Markdown文件的文件名并不会自动填充为页面的标题，这会让Zotero与wolai的联动变得不够高效，需要手动填充页面标题。

所以，近期我向wolai提的第一个功能建议就是：**页面内导入文件时，将导入文件的`文件名`自动填充为`页面的标题`。**

简单演示下。👇

假如我有下面这样一个Markdown的文件（一个自动生成的Zotero笔记模板）。

![Markdown的文件](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210128220111.png)

这个markdown文件的文件名是一篇文献的标题（或者可以是CiteKey），而markdown的内容中是不包含文献标题的。

回到wolai，假如我在`文献阅读`目录下新建了一个文献笔记页面。

![页面内导入](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210128220544.png)

接着，按照上图箭头处**点击导入**，选择刚刚的Markdown文件。

![导入markdown](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210128220635.png)

此时可以看到Markdown的文件名（即文献名）自动填充为页面的标题了。

![自动填充页面标题](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210128220734.png)

显然，这是我们想要的结果。🌝


### 新页面的默认位置

第二个功能更新建议，来自于我使用双向链接笔记`Obsidian`的一点心得。

在Obsidian中有一个实用的功能是：**可以设置新建笔记的存放位置**。👇

![Obsidian- 新建笔记的存放位置](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210128221256.png)

比如我设置的是`Topics`文件夹。

**这个功能的使用逻辑在于**：我认为做文献笔记时，所有使用`[[]]`新建的主题（即对应一个新的markdown页面）都是一个`标签`，这个标签是我对这篇文献的一个标记，比如是`机器学习`，那么我希望所有的`标签`都放在一个目录下，也就是上述`新建笔记的存放位置`所设置的，方便以后集中复习。

所以，我将这个实用功能向wolai的开发者提了一下。

幸运的是，1月27号，在wolai的`0.6.5.24`版本中，这个功能上线了！（点赞一波wolai开发团队的高效👍）

![wolai 0.6.5.24版](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210128222145.png)


现在，在wolai的`空间偏好`设置中，可以设置

- 创建新页面的默认位置
- 今日速记默认位置

![空间偏好](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210128222359.png)

关于`创建新页面的默认位置`，需要了解的是：**在引用或者add.page域名快捷等方式创建页面时，会默认创建在指定页面下。**


举个例子，我打出`[[`，然后输入`机器学习`，按下Enter，即可创建一个叫做`机器学习`的新页面。


![引用新页面](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210128223419.png)

此时会发现，Topics文件夹下出现了一个名为`机器学习`的新页面。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210129094810.png)

完美！

以上就是对两个新功能的所有介绍！

希望wolai越来越好，也希望wolai成为科研人提高生产力的高效工具。