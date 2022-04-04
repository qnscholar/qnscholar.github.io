---
layout: post
title: zotero-save-with-tag 插件「进阶使用」
date: 2021-11-10 22:36:00
tags: 
- Zotero
published: true
---



前日向大家介绍了一个非常实用的插件**zotero-save-with-tag**。👇


[绝了！这个 Zotero 新插件简直刚需！](https://mp.weixin.qq.com/s/SY6JqFOkC7tKplVrvN8tBA)

<blockquote data-tool="科技兽" style="border-top: none;border-right: none;border-bottom: none;font-size: 0.9em;background: url(https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210519013028.png) 10px 10px / 40px no-repeat rgb(91,79,137);overflow: auto;color: inherit;border-left: 0px;padding: 1.2em 2em;margin-bottom: 2em;margin-top: 2em;text-align: center;border-radius: 10px;"><p style="font-family: Optima-Regular, Optima, PingFangSC-light, PingFangTC-light, &quot;PingFang SC&quot;, Cambria, Cochin, Georgia, Times, &quot;Times New Roman&quot;, serif;text-align: justify;line-height: 26px;margin-top: 1em;margin-bottom: 0.3em;font-size: 14px;color: rgb(255, 255, 38);"><strong style="color: #fc8705;">zotero-save-with-tag</strong><br  />当你通过Zotero Connector将网页端的文献保存至Zotero，或者拖动PDF到Zotero，该插件会自动为新导入的文献添加一个「To-Read」标签（意味着待读）。</p></blockquote>

今天继续介绍「zotero-save-with-tag」插件的**进阶使用**。

#### 完成阅读后

「zotero-save-with-tag」插件的作用是给待读的文献添加一个**To-Read**标签，**那么当我们完成阅读该文献后，自然要取消该标签**。

为了快速取消该标签，最有效的途径是利用[颜色标签](https://mp.weixin.qq.com/s/vrNMC-OYMVtcEeNtxVzJ6A)功能。

为此，首先从标签面板找到To-Read标签，然后
右键选择**Assign Color**。

![Assign Color](https://gitee.com/qnscholar/figurebed/raw/master/img/20211110184550.png)

比如我设置了如下颜色，且快捷键为`6`。

![颜色标签设置](https://gitee.com/qnscholar/figurebed/raw/master/img/20211110185231.png)

那么，当我们完成阅读一篇文献后，按下键盘上的`6`便可以**取消To-Read标签**。

当然，同时你也可以设置一个以为「**完成阅读**」的颜色标签，并分配一个快捷键。

比如我的「完成阅读」标签为**Done**，快捷键为`1`。

![完成阅读标签及其快捷键](https://gitee.com/qnscholar/figurebed/raw/master/img/20211110185528.png)

也就是说，完成阅读一篇文献后，你可以先后按下键盘上的`6`和`1`。

如此一来，完成阅读的文献就可以通过标签**Done**归档。

#### To-Read文献的筛选

如果想从My Library中过滤出所有带To-Read标签的文献，是不是在标签面板中找到To-Read就行了呢？

***非也***。

这里的情况比较特殊：

细心一点可以发现，**zotero-save-with-tag**插件为新导入的文献添加标签时，**父级条目（Parent Item）及其PDF附件都会加上To-Read标签。** 👇

![](https://gitee.com/qnscholar/figurebed/raw/master/img/20211110190328.png)

可是，当我们完成一篇文献阅读，按下上述颜色标签`6`后，只有父级条目的To-Read标签会被取消，而其PDF附件的To-Read标签则不会。

这导致的后果是：**在To-Read标签的过滤结果中，已经完成阅读的文献依然在里面。**

下图进行了演示。

![演示](https://gitee.com/qnscholar/figurebed/raw/master/img/20211110191212.png)

那么，总不能完成一篇文献阅读后，对条目及其PDF分别按一次快捷键吧！？**这也太蠢太不高效了。**

***这里有更为巧妙的方法。*** 👇

是时候利用Zotero的Saved Search功能了。👇

[厉害了！Zotero的【Saved Search】功能竟有如此妙用！](https://mp.weixin.qq.com/s/Twpyd6emaDqrhpf6rANfdA)

我们右击My Library，选择**New Saved Search**。👇

![New Saved Search](https://gitee.com/qnscholar/figurebed/raw/master/img/20211110191753.png)

比如起个名字叫做To-Read，筛选条件设置为`Tag` `contains` `To-Read`。

![Saved Search - 筛选条件设置](https://gitee.com/qnscholar/figurebed/raw/master/img/20211110191957.png)

另外，**务必勾选**下方的**Show only top-level items**👆，即只显示父级条目。

***如此一来，便可以忽略PDF附件所包含的To-Read标签了。***

即，建立的**To-Read Saved Search**可以准确地过滤待读文献。

![「To-Read」 Saved Search](https://gitee.com/qnscholar/figurebed/raw/master/img/20211110192526.png)

也就是说，完成阅读并按下快捷键`6`的文献不会在这里显示。

所以，啥时候想读新文献了，进入**To-Read Saved Search**即可。

到此，就介绍完了**zotero-save-with-tag**插件进阶使用。

总结一下：

- 颜色标签To-Read仅仅用于生成一个快捷键，从而实现快速取消已读文献的To-Read标签。
- 通过建立Saved Search，实现对待读文献的准确筛选，快速抵达。