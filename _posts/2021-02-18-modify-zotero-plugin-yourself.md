---
layout: post
title: 小白如何自己修改Zotero插件？
date: 2021-02-18 22:36:00
tags: 
- Zotero
published: true
---



很多Zotero用户，有时想自己修改某个插件，使其更符合自己的需求。

但是又不知道怎么做？

完整写一个Zotero插件，那是码农干的事情！但是，修改一个插件，有时并没有那么难。

今天就介绍一下小白如何简单修改Zotero插件！

### 简单修改Zotero插件

Zotero插件主要有两种格式：

- `.xpi`格式，几乎所有Zotero插件都是这种格式。
- `.zoteroplugin`格式，比较少见的Zotero插件格式，新版ZoteroQuickLook插件就是这种格式。

今天，我们主要介绍`.xpi`格式Zotero插件的修改。

`.xpi`其实一种压缩文件格式，就如同我们常用的`.zip`等压缩格式一样。

既然是压缩文件格式，那么自然想到从压缩软件入手。

很多小白，首先想到的是把Zotero插件的`.xpi`后缀改为`.zip`格式，在`.zip`格式内修改插件之后，再把后缀改为`.xpi`。

***可是，这样做的结果就是Zotero无法识别该格式。***

那么，正确的做法是：

> 找到一个可以直接打开`.xpi`文件的压缩软件（注意：不是直接解压），然后在压缩软件内修改插件内容，修改完后，存储更改到压缩包即可。

下面，分别以Mac系统和Windows系统，进行详细介绍。

#### Mac

在Mac上，**鼎鼎大名**的压缩软件BetterZip可以直接打开`.xpi`格式。

（不幸的是，**臭名昭著**的思杰马克丁代理了BetterZip）

这里，我以修改**mdnotes.xpi**插件进行演示。

启动BetterZip，按下`CMD+O`或者点击菜单栏`文件-->打开`，然后选择mdnotes.xpi。

![BetterZip](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210217204657.png)

或者，更快的方法是，把mdnotes.xpi插件拖到Dock栏的BetterZip应用图标上。

打开mdnotes.xpi后的界面如下。👇


![用BetterZip打开mdnotes.xpi](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210217205440.png)

一般来说，一款Zotero插件的核心代码都在content文件夹下，比如mdnotes插件的核心代码就是content文件夹下的mdnotes.js。👇


![插件核心代码](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210217205209.png)

假如你想修改mdnotes.js，直接双击即可，一般会自动以默认的文本编辑器打开。

（推荐大家使用Sublime Text，[这里下载](https://mp.weixin.qq.com/s/eVKIuTIzkqEZsQxGcjZRSQ)）

Sublime Text打开mdnotes.js后，就可以修改自己想改的部分了。

![修改代码](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210217210307.png)



很多代码，看看也就大概懂了。而且，往往你想改的地方，都很容易看懂。


修改完成后，按`CMD+S`保存修改。

此时，Dock栏的BetterZip应用图标开始跳动，并提示：**文件mdnotes.js已经被更改，您希望将更改存储回压缩文件吗？**


![更新文件](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210217210601.png)

点击**更新文件**，然后关闭BetterZip窗口，或者按下`CMD+W`。

继续提示：**您想存储您对文件mdnotes.xpi所做的修改吗？如果不存储，您的改动将会丢失。**

![存储修改](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210217211022.png)

点击**存储**。

继续提示：**警告：存储过程不可逆，您确定要替换原压缩文件吗？**


![替换原压缩文件](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210217211237.png)

再次点击**存储**。

最后的最后，提示如下。👇不重要，任选其一皆可。

![任选其一](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210217211507.png)

到此，就彻底完成了mdnotes插件的修改！在Zotero中也能正常安装。

#### Windows

Windows上，压缩软件**快压**可以直接打开直接打开`.xpi`格式。

（`青柠学术`公众号后台回复`快压`下载。）

启动**快压**，点击左上角的`打开`，然后选择想要修改的插件，比如mdnotes.xpi。打开后如下。👇

![快压内打开Zotero插件](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210217211932.png)

其余操作和上述BetterZip类似，这里不再赘述。


以上就是本文的全部，希望能够帮助到你！