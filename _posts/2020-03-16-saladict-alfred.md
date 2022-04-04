---
layout: post
title: 沙拉查词 + Alfred，打造最佳文献翻译体验！
date: 2020-03-17 09:30:00
tags: 
- Mac生产力
- 文献阅读与翻译
published: true
---

先上为敬！直接亮结果👇这么极速的文献翻译体验你心动了吗？



![单词翻译](https://tva1.sinaimg.cn/large/00831rSTly1gcw4id90s1g31400oe4qp.gif)



![一段文字翻译](https://tva1.sinaimg.cn/large/00831rSTly1gcw1gm3gyeg31400oex6q.gif)



### 前言

今天聊一聊很多人都非常感兴趣的一个话题：文献翻译。

关于文献翻译工具，很早之前我给大家介绍过一款：Copytranslator。👇

[文献翻译神器CopyTranslator，你的科研必备工具！](https://mp.weixin.qq.com/s/y3TH3zFBL_-zLg7wtm80LQ)

如果满分100人，我只能给Copytranslator打70分，因为它只能算是一款功能上还可以，体验上却还远远不足的翻译软件！

期间有粉丝希望我介绍更多的文献翻译软件，还有一些粉丝则向我推荐他们用过的翻译工具。

但是我迟迟没有发推文再次介绍文献翻译软件，主要原因有两点：

1. 我一直主张不应该过分依赖翻译软件。不依靠翻译工具就能快速阅读完一篇文献，是每个研究生都应该追求的目标。
2. 对于之前接触过的翻译软件，我对它们的体验都不是很满意。这让我觉得一款体验不好的翻译软件只能让阅读文献变得复杂，会破坏阅读文献的流畅性。

但是，今天我要打脸了，我决定再聊一聊文献翻译这个话题。（因为实在看到太多粉丝对这方面的内容感兴趣）

再加上我自己的一些好奇心，我就花了两三个小时小小研究了一款比较火的翻译工具：沙拉查词。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcv28tf87oj30jg07st90.jpg)

于是就有了今天这篇推文：**沙拉查词+Alfred，打造最佳文献翻译体验！**

这里特别强调了`体验`两个字，因为翻译工具有太多，体验很好的翻译工具却寥寥无几！

沙拉查词在Windows系统和macOS系统都要搭配相应的第三方工具才能实现**最佳体验**，今天介绍的`沙拉查词+Alfred`组合则是针对Mac电脑的。

（寒假在家，身边没有Windows电脑，因此关于Windows电脑上沙拉查词的用法，等开学了会发文介绍。不过其实无妨，两者的配置思路大致差不多，所以如果你是Windows用户，你完全可以继续往下看）👇

### 什么是沙拉查词？

沙拉查词，即Saladict，是一个非常良心的开源项目，它以浏览器（Chrome、Firefox等）插件的方式存在，可以实现高效的查词和翻译。

有很多开发者和网友为这个项目贡献了许多有趣的玩法！

想要详细了解，可以直接访问[官网](https://saladict.crimx.com/ "官网")。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcv29r9c2vj31740qaq6x.jpg)

官网列举了一些沙拉查词的特性，本文将重点关注下面几点：

- 丰富的词典支持。（谷歌翻译、百度翻译、必应词典、剑桥词典、柯林斯高阶等）
- 浏览器外划词翻译，即在Mac上搭配Alfred实现任意文献阅读软件内的极速翻译体验。
- 单词同步。绑定扇贝账号进行生词同步，实现生词云备份，还方便了在手机上复习生词。

### 【沙拉查词+Alfred】配置方式

在沙拉查词官网的[这个页面](https://saladict.crimx.com/manual.html#open-setting "使用教程")有完整的使用说明。不过该页面涉及的内容非常多，而且很多也不是必须了解的，因此下面我只介绍配置`沙拉查词+Alfred`的必要步骤。

#### 沙拉查词下载安装

首先到[GitHub](https://github.com/crimx/ext-saladict/releases "沙拉查词下载地址")上下载沙拉查词最新版浏览器插件。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcvvuchpx4j31740qawip.jpg)

可以看到沙拉查词在Chrome、Firefox和Edge浏览器上都有相应的插件，本文将以Chrome版为例进行介绍。

点击上图中的链接即可跳转到Chrome商店，如果你无法访问Chrome商店，我已经传了一份沙拉查词到百度网盘，公众号后台回复`沙拉查词`即可获取。

安装成功后，在Chrome的右上角可以看到沙拉查词图标。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gcvvzmnfchj31740q9tc5.jpg)

#### 浏览器外划词翻译

接下来详细介绍【浏览器外划词翻译】的配置步骤，浏览器内的就不介绍了（很基础，沙拉查词网站有详细介绍）。

本文的目标是实现在浏览器外的PDF阅读软件内实现划词翻译，浏览器外配置好后，其调用沙拉查词的方式同样适用于浏览器内，因此一劳永逸！

在沙拉查词的[下方网页](https://saladict.crimx.com/native.html#%E6%97%A0%E8%BE%85%E5%8A%A9%E6%9F%A5%E8%AF%8D "浏览器外划词")上，介绍了在不同系统上实现浏览器外划词的方式，包括Windows和macOS系统。（如果你是个Windows用户，该页面也可以提前了解下，当然我以后也会介绍）

![](https://tva1.sinaimg.cn/large/00831rSTgy1gcvwvyprm1j31740qa78l.jpg)

对于Mac用户，要想实现浏览器外划词翻译，需要搭配著名的Alfred软件。Windows用户则需要搭配Quicker。

如果你的Mac电脑上未安装Alfred软件，请在公众号后台回复`Alfred`下载并安装软件。

若你在安装软件过程中，遇到诸如**“XX损坏”、“XX意外退出”、“无法检查其是否包含恶意软件”、“不明来源应用”**等提示，请参考推文[macOS Catalina如何打开未知来源应用？](https://mp.weixin.qq.com/s/chTStRvCk8Apn66HSDsBgw )中的方法即可解决问题。

安装完Alfred，点击Powerpack，如果显示下面这个样子，代表是注册版，👇可以放心使用。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcvwfbdx3pj30yg0msaco.jpg)

接着，我们去[GitHub网页](https://github.com/crimx/ext-saladict/issues/509 "Alfred Workflows + Saladict配置方式")了解“Alfred Workflows 调用 Saladict 实现全局【文本翻译】”的配置步骤。

![](https://tva1.sinaimg.cn/large/00831rSTgy1gcvwz9d03gj31740qa0w6.jpg)

下面介绍具体操作步骤。👇

#### 设置沙拉查词全局快捷键

为了实现在浏览器外调用沙拉查词，需要在浏览器内为沙拉查词设置`全局快捷键`。

以Chrome浏览器为例，在地址栏输入`chrome://extensions/shortcuts`，进入下方的快捷键设置界面。

找到沙拉查词中的`在独立窗口中搜索剪贴板内容`，设置快捷键（建议设置为`CMD+Shift+L`），并选择`全局`。

![](https://tva1.sinaimg.cn/large/00831rSTgy1gcvxg67ranj31740q976x.jpg)

#### 配置Alfred workflow

为了实现沙拉查词和Afred的搭配使用，需要下载一个Alfred workflow脚本，[下载地址](https://github.com/crimx/ext-saladict/files/3711425/saladict.alfredworkflow.zip "saladict.alfredworkflow下载地址")，或者公众号后台回复`saladict`获取。

下载下来的是一个压缩包`saladict.alfredworkflow.zip`，解压后得到`saladict.alfredworkflow`，双击进行安装。

来到下方界面，点击`import`即可。

![](https://tva1.sinaimg.cn/large/00831rSTgy1gcvx8e9uxij30zw0o8dhu.jpg)

继续来到下方界面，双击下图所示的`Hotkey`录入快捷键。

![](https://tva1.sinaimg.cn/large/00831rSTgy1gcvxaqv720j30zw0o8q4p.jpg)

根据自己的习惯，在下图所示处设置一个快捷键（我设置的是`CMD+Shift+D`），点击`Save`进行保存。

![](https://tva1.sinaimg.cn/large/00831rSTgy1gcvxlu9n8rj30zw0o8aca.jpg)

接下来，双击下图所示的`Run NSAppleScript`。



![](https://tva1.sinaimg.cn/large/00831rSTgy1gcvxqdyu0vj30zw0o8tai.jpg)

默认代码如下，即通过快捷键`CMD+Ctrl+L`调用沙拉查词。由于我们前面在Chrome上设置的全局快捷键为`CMD+Shift+L`，和这个不符，因此需要进行修改。

![](https://tva1.sinaimg.cn/large/00831rSTgy1gcvxqagzopj30zw0o8gno.jpg)

使用`shift`替换上图中的`control`即可；或者也可以拷贝下方代码，覆盖上图中的全部代码。

```
on alfred_script(q)
  tell application "System Events"
	# 快捷键打开沙拉词典
	key code 37 using {shift down, command down}
  end tell
end alfred_script
```

也就是修改为下面这个样子，点击`Save`。（如果你在Chrome中设置的不是`CMD+Shift+L`快捷键，那么你可以参考[链接](https://eastmanreference.com/complete-list-of-applescript-key-codes "自定义快捷键")，将你的快捷键设置在此处）

![](https://tva1.sinaimg.cn/large/00831rSTgy1gcvxv3rba2j30zw0o8mz8.jpg)

#### 关于几个快捷键的说明

这里解释下上面涉及的几处快捷键：

我们共设置了三处快捷键，即沙拉查词`全局快捷键`、`Hotkey`、`Run NSAppleScript快捷键`。其中`全局快捷键`必须和`Run NSAppleScript快捷键`保持一致，`Hotkey`理论上可以自己随意设置，唯一的准则就是不能和你使用的PDF阅读软件中的已有快捷键重合，不然将无法调用沙拉查词。

三个快捷键的调用关系是`Hotkey`-->`Run NSAppleScript快捷键`=`全局快捷键`-->沙拉查词。

也就是说，当你在PDF阅读器中选中文字，按下`Hotkey`时，会触发Alfred的`Run NSAppleScript快捷键`，由于`Run NSAppleScript快捷键`和`全局快捷键`一致，因此便能够调用沙拉查词实现划词翻译。表现形式是：会弹出单独的沙拉查词面板，显示查词结果。

在正式演示翻译效果之前，还得说明一个问题：

如果不搭配Alfred，其实沙拉查词也能实现浏览器外划词翻译，只需设置`全局快捷键`即可。但是这种方式需要首先将待翻译内容传递给剪贴板，然后将剪贴板内容传递给沙拉查词。也就是说，在PDF阅读软件中阅读文献时，需要选中一个单词或者一段文字，先按下`CMD+C`进行复制，再按下全局快捷键（比如`CMD+Shift+L`）才能调用沙拉查词实现翻译。显然这种方式太过繁琐，需要三步才能实现翻译，这绝对谈不上很好的体验。

那么，搭配Alfred后，拷贝文字（即按下`CMD+C`）这一动作，就由Alfred来完成。我们要做的就是选中文字，然后按下Hotkey（即前面设置的`CMD+Shift+D`），即可自动弹出沙拉查词翻译面板，也就说最多需要两步。

之所以说最多两步，是因为选择文字这一动作对于单词来说，其实通过**鼠标双击即可自动选中单词**（很重要！！），这是一个非常自然的动作，因此对于查单词来说，可以近似认为只有一步按下Hotkey的动作。一步动作，自然能带来极速的翻译体验了！

当然，如果是一段文字，还是需要首先拖动鼠标选中文字，再按下Hotkey（即`CMD+Shift+D`），即可弹出沙拉查词翻译面板。虽然多了一步选中操作，但还是非常方便的，依然能够称得上极速翻译。

### 翻译演示

为了能够正常使用沙拉查词功能，我们需要让Chrome浏览器和Alfred处于打开状态。

下面通过动图演示在PDF阅读软件中，实现文献的单词翻译和一段文字翻译。

![单词翻译](https://tva1.sinaimg.cn/large/00831rSTly1gcw4iyrcc1g31400oe4qp.gif)



![一段文字翻译](https://tva1.sinaimg.cn/large/00831rSTly1gcvz7ziis6g31400oex6q.gif)

怎么样，还是很完美的吧！

整个过程可以描述为：`选中文字-->按下CMD+Shift+D-->自动弹出查询结果`，非常的高效，而且弹窗动画的加入让整个操作很流畅很舒服！

可以看到，在弹出的沙拉查词面板中，会显示不同词典翻译的结果，比如谷歌翻译、百度翻译、必应词典等等。当然，可以设置显示哪些词典的翻译结果，稍后会说明。

### 一些推荐设置

下面介绍几个关于沙拉查词的推荐设置，通过这些设置，可以让沙拉词典变得更好用，或者说更符合你自己的使用习惯。

#### PDF阅读器和沙拉查词并列显示

如果你不喜欢沙拉查词的弹窗效果，想要一个安静又简洁的阅读环境，那么不妨将PDF阅读器和沙拉查词在一个全屏窗口中并列显示，如下所示👇。体验也是相当不错的！

![](https://tva1.sinaimg.cn/large/00831rSTly1gcw25t2x88j315n0qnqci.jpg)

#### 词典设置

在沙拉查词面板中，双击下图所示处，可以进入沙拉查词的设置界面。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcw2aw2lzhj30e60icgmh.jpg)

或者，通过右键Chrome上沙拉查词的图标，点击`选项`，同样可以进入沙拉查词的设置界面。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcw2cxcw85j31740q9425.jpg)

沙拉查词设置界面如下👇。在【词典设置】中，可以添加或者删除词典，这直接决定了在沙拉查词面板中有哪些词典的翻译结果会显示出来。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcw2fh929kj31740q941j.jpg)

这里，我添加的是有道词典(或必应词典)、谷歌翻译和百度翻译。其中有道词典(或必应词典)对于查单词体验非常好，查询结果很详细，服务器的响应速度也很快。谷歌翻译和百度翻译则用于段落翻译，还可以顺便对照着看看谷歌翻译和百度翻译的翻译精准度。

#### 黑暗模式

为了实现一个沉浸式的阅读环境，建议将查询面板设置为`黑暗模式`。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gcw2kagwc9j31740q941k.jpg)

下面是明亮模式和黑暗模式的对比效果。还是黑暗模式看着比较舒服啊！

![](https://tva1.sinaimg.cn/large/00831rSTly1gcw2qc3iugj30rp0ic0uu.jpg)

#### 生词同步

想不想将文献阅读过程中遇到的生词都备份到云端呢？

在【单词设置】中，可以通过WebDAV或者扇贝生词本同步生词，这里我选择的是扇贝，点击绑定扇贝账号即可。同时建议关闭“红心单词时弹出编辑面板”。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gcw2xw1zkwj31740q90vx.jpg)

同步设置完毕后，点击沙拉查词弹窗中的心形按钮，👇即可一键将查询的单词同步到扇贝。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcw42v96mdj30e60icmy2.jpg)

如此一来，平时阅读文献时积累的生词就全部同步到扇贝了，建议下载扇贝App到手机上，方便随时复习生词！

### 注意事项

如果你安装本文提供的Alfred后，或者以后使用了其他版本Alfred后，发现选中文本后按`Hotkey`（即`CMD+Shift+D`）无法调出沙拉查词面板，下面提供的解决办法可以供您参考：

打开Mac电脑的`设置-->安全性与隐私-->辅助功能`，首先点击左下角的小锁🔒图标，输入密码解锁，接着取消勾选Alfred 4，再重新勾选☑️Alfred 4。

此时，你应该会发现可以用`CMD+Shift+D`正常划词了！

![](https://tva1.sinaimg.cn/large/00831rSTly1gcyifn0narj30k80hlmyd.jpg)

### 总结

本文字数大概3860，虽然看起来似乎内容挺多，其实【沙拉查词+Alfred】这个组合的配置方式并不难，只是我写的比较详细！

我写得详细，你们才能少踩坑啊。

根据我的使用感受，可以给【沙拉查词+Alfred】所打造的文献翻译体验打95分！

这个组合还有一个巨大优势在于不受PDF阅读器限制，你在电脑上任何能划词的地方，都可实现快速翻译！当然你得保证你的浏览器和Alfred处于打开状态。（可以设置为开机启动）

虽然本文介绍的内容是针对Mac用户的，但是Windows上配置思路也差不多，只是把Alfred换成了Quicker！

等后面开学手边有了Windows电脑后，我会推出Windows上沙拉查词的配置方式！大家也可以自行琢磨起来！

