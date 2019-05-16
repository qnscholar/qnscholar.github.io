---
title: C盘空间不够了怎么办？这就教你如何扩容！
date: 2019-05-17 00:00:00
categories:
- 超赞工具
tags:
- C盘扩容
- PE系统
typora-root-url: ../../iseex.github.io
---

当你看到下图，什么感受？

![](/assets/images/posts/Tools/c-red.jpg)

此时，相信你一定为C盘空间不够而烦恼！

随着电脑使用时间越来越长，软件安装得越来越多，C盘会逐渐变得臃肿，刚刚安装系统时以为留100G给C盘足够了，后来发现还是太天真了！

就在今天我的C盘也红了，甚至部分软件提示无法工作了！所以我不得不想办法为C盘扩容了。

可是，如果不采用合适的方法，对磁盘进行分区调整可能出现数据丢失问题。因此今天介绍个快速且安全的方法。

常见的磁盘扩容方法有两种。第一种是进入**计算机管理**的**磁盘管理工具**，

![](/assets/images/posts/Tools/disk-management.jpg)

不过用这种方法扩容C盘，需要把C盘旁边的盘给格式化，因此不推荐。这里介绍我才用的方法。

# 利用PE系统分区助手为C盘扩容

很早的时候，我介绍过如何用U盘制作PE系统，请[点击这里](https://mp.weixin.qq.com/s/YWPzYmUy7EMPdomcQw5NlA)阅读文章。不过这篇文章中提供的WePE软件的下载链接已经过期，这里重新分享下。

>WePE下载链接：
>
>链接: https://pan.baidu.com/s/10Z1jKW0t8WlSdK38l9Lsxg 提取码: 6gqv 

为了进行下一步的分区操作，需要首先制作PE系统。

PE系统制作好后，将U盘插入电脑，并进入PE系统，在桌面上找到**分区助手（无损）**软件并打开，如下图所示。

![](/assets/images/posts/Tools/PE-disk-helper.jpg)

打开分区助手后，选择你一个想要分配多余空间给C盘的磁盘，因为我这里F盘剩余空间较多，因此选择F盘。点击F盘，在左侧面板选择“分配自由空间”，如下图所示。

![](/assets/images/posts/Tools/PE-disk-select.jpg)

出现下图界面，输入想要分配给C盘的空间，点击确定。

![](/assets/images/posts/Tools/PE-cut-disk.jpg)

点击确定后，还没完，还需点击左上角的**提交**（确认后提交按钮变绿），如下图所示。

![](/assets/images/posts/Tools/PE-confirm-cut.jpg)

之后，会有个进度条显示磁盘分配进程，等待数十分钟即可完成。完成后，退出PE系统，重启电脑即可发现C盘已经扩大了很多。下图便是我扩容了50G后的C盘。

![](/assets/images/posts/Tools/disk-extension-finished.jpg)

到此C盘扩容大功告成，再也不同担心C盘不够用了~