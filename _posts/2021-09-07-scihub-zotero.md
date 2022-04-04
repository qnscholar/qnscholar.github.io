---
layout: post
title: SciHub 复活后，Zotero + SciHub 玩法大汇总！
date: 2021-09-07 22:36:00
tags: 
- Zotero
published: true
---



昨天通过一个简单的测试，确认了回归后的SciHub已经能够下载一个月前的论文了。

[SciHub归来！问题来了：一个月前的论文能下载不？](https://mp.weixin.qq.com/s/bywFy1xCso7bFexoe6Dmmw)

早期的时候，**青柠学术介绍过一些Zotero + SciHub的搭配玩法。**

那么，随着SciHub的复活，这些玩法可以重新捡起来了。

下面来回顾下（有更新）。

#### Find Available PDF（下载PDF）

之前，在下文中介绍了将SciHub配置为Zotero的PDF解析器，来实现文献PDF的下载。

[Zotero搭配Sci-Hub，真香！](https://mp.weixin.qq.com/s/QMSG24tgn4z8ShfE9pVYMg)

特别提到了**SciHub的配置代码**：
```
{
    "name":"Sci-Hub",
    "method":"GET",
    "url":"https://sci-hub.ee/{doi}",
    "mode":"html",
    "selector":"#pdf",
    "attribute":"src",
    "automatic":true
}
```

根据最新的可用网址，上述url的内容可以为：

- https://sci-hub.ee
- https://sci-hub.se
- https://sci-hub.ru
- https://sci-hub.st
- https://sci-hub.ren

为了挖掘Zotero + SciHub的应用场景，之前还介绍了`WOS检索文献-->导出文献题录-->导入文献至Zotero-->文献泛读/SciHub下载PDF`的工作流。

[Zotero + Web of Science，如何做文献泛读？](https://mp.weixin.qq.com/s/1KM2rySbNcUZaW7RuLRiSQ)

其中最后一步「SciHub下载PDF」，即是下图的**Find Available PDFs**。👇

![Find Available PDFs](https://gitee.com/qnscholar/figurebed/raw/master/img/20210907214109.png)

#### ZotFile + SciHub 搜索引擎

如果觉得上述的SciHub解析器方式下载文献比较慢，而且你不需要处理大量文献，那么推荐使用下面的方法下载PDF。👇

[ZotFile + Sci-Hub，巧妙玩转PDF下载！](https://mp.weixin.qq.com/s/je9hPNN37xhtAjRFSZQGIQ)

> **简单来说**：选中不含PDF附件的文献题录，然后一键点击「 **Zotero SciHub搜索引擎**」，跳转到浏览器手动下载该PDF，最后通过ZotFile插件的Attach New File功能实现PDF附件的绑定。

一张动图演示下关键步骤：

![Zotero SciHub搜索引擎 - 演示](https://raw.githubusercontent.com/iseex/iseex.github.io/master/images/Kapture%202021-09-07%20at%2021.59.26.gif)

最后，呈上更新版「Zotero SciHub搜索引擎」的下载方式。👇

**Zotero SciHub搜索引擎下载**：`青柠学术`公众号后台回复`SciHub引擎`下载。

其中，搜索引擎配置方法可参考[本教程](https://mp.weixin.qq.com/s/6pV4aDKL-EOoV9dgvxK9ew)。

当然，如果你想获取青柠学术全部搜索引擎，可以[在此加入会员](https://mp.weixin.qq.com/s/cxjGBasxldUKGcJR3vzUFA)（当作一种支持咯🤭）～