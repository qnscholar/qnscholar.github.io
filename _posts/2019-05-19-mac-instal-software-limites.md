---
title: MacOS Sierra 或 Mojave 如何打开未知来源应用？
date: 2019-05-19 01:00:00
categories:
- 超赞工具
tags:
- macOS
typora-root-url: ../../iseex.github.io
---

可能很多人和我一样，每次将mac系统升级到最新版本，就会遭遇一些第三方软件无法安装的情况，比如提醒"来自身份不明的开发者"或者"已损坏，移到废纸篓"。

![](/assets/images/posts/Tools/mac-software-problem1.jpeg)

在macOS Sierra之前的系统，只需要到"系统偏好设置-安全性与隐私-通用"里勾选"任意来源"即可打开第三方应用。可是在macOS Sierra系统，这样做却无济于事。

对于macOS Sierra系统，小编为您提供开启任意来源的解决办法：

- 打开应用程序-实用工具-终端。
- 在终端中输入代码`sudo spctl --master-disable`，回车并输入密码。
- 此时，再次到"安全性与隐私"中查看，发现"任意来源"可以勾选了，即可以放心安装第三方软件了。

macOS Sierra的问题解决了，新的问题又在macOS Mojave中出现了。

如果你的mac已经更新到Mojave系统，有时候你会发现，尽管采用了上述方法，安装第三方软件时依旧会提醒"打不开已损坏"。现在另一种解决方案来了，贴在下方供大家参考。下面以安装SketchUp软件为例：

- 打开终端，输入`sudo bash`并回车，这时需要输入电脑密码，输入密码后回车，则切换为root用户。
- 接着输入`xattr -cr /Applications/SketchUp/SketchUp.app`，再次回车。
- 此时回到`/Applications/SketchUp`目录，发现可以正常打开`SketchUp.app`了。

上面几步操作的大概意思就是：对`/Applications/SketchUp/SketchUp.app`路径的SketchUp软件添加信任，一旦系统信任该第三方软件，就可以正常安装了。

顺便提一下，这里的Applications就是Finder窗口左侧的"应用程序"。如果是其他软件，需要对代码`xattr -cr /Applications/SketchUp/SketchUp.app`进行变换，变换原则是路径要定位到`软件名.app`上。特别需要提醒的是，如果你的应用名中间有空格，比如是`SketchUp 2017`，此时建议将应用程序下的`SketchUp 2017`改为`SketchUp`（总之得删除空格），否则该代码会运行失败，即代码`xattr -cr /Applications/SketchUp 2017/SketchUp.app`是错误的。

为了更佳直观地掌握该方法，这里贴上我的操作截图。

首先是`/Applications/SketchUp`目录：

![](/assets/images/posts/Tools/applications-sketchup-filefolder.png)

单击SketchUp文件夹，进入下方目录，发现有`SketchUp.app`即对应了路径`/Applications/SketchUp/SketchUp.app`。

![](/assets/images/posts/Tools/applications-sketchup.png)

熟悉了上述路径后，打开终端，按照下图执行代码。

![](/assets/images/posts/Tools/shell-sketchup.png)

接着，回到目录`/Applications/SketchUp/SketchUp.app`，双击SketchUp，发现可以正常打开了，如下图。

![](/assets/images/posts/Tools/sketchup-open.png)

> 今天就介绍到这里，建议收藏本文，说不定哪天你也会遇到这个问题～

