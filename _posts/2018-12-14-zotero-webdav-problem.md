---
title: 又来新问题！Zotero提示“请输入一个WebDAV地址”，这就告诉你怎么解决！
date: 2018-12-14 00:00:00
published: true
tags:
- Webdav
- Zotero
- 坚果云
categories:
- 文献管理
typora-root-url: ../../iseex.github.io
---

### 问题

大家都知道我个人非常喜欢使用Zotero来管理文献，于是偶尔我会推荐给实验室的同学使用。这几天实验室的一个同学说想要安装Zotero用用，于是我从Zotero官网下载了Zotero的最新版本，在进行配置时，我特意打开了我之前写过的好几篇关于Zotero配置的一些步骤和难点的博客，防止哪里操作出错。

在将坚果云作为WebDAV，配置成为Zotero的第三方存储时（可参考以前的一篇[推送](https://iseex.github.io/2018-08/zotero-webdav/)），我发现一个新的问题。就是当输入了WebDAV地址、坚果云账号和授权密码后，当我点击**Verify Server**，弹出“请输入一个WebDAV地址”，如果是英文版本Zotero，弹出的是“Please enter a WebDAV URL”。这个问题我还是第一次见，至少在我使用Zotero的时候还没遇到这个问题。

于是，我上网查了查，最后在Zotero的论坛里发现不少网友都在讨论这个bug（[点击这里](https://forums.zotero.org/discussion/67182/webdav-error-please-enter-a-webdav-url)），并给出了解决方案。这里就告诉大家如何解决。

### 解决方法

大家在将WebDAV地址，Zotero账号和密码输入完成后，不要点击**Verify Server**，而是输完密码后直接按Enter，即可完成验证，搞定！如下图所示，是不是很简单呢！

![](/assets/images/posts/zotero/webdav_problem.jpg)