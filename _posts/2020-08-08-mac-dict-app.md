---
layout: post
title: Mac词典打磨，创造极致查词体验！
date: 2020-08-08 22:39:00
tags: 
- Mac生产力
published: true
---





之前，我向大家介绍了如何使用**沙拉查词 + Alfred**，在Mac上打造最佳文献翻译体验！👇

[沙拉查词 + Alfred，打造最佳文献翻译体验！](https://mp.weixin.qq.com/s/1D1I1WpiPS2diDZtfJT9Hg)

今天，本文将目光转向Mac自带的词典App，来探讨下如何将Mac词典打磨得更好用，甚至打造出极致的查词体验！

**实现方法**：将自己喜欢的第三方词库导入Mac词典，以扩充词库，并实现更养眼更精致的查词界面；为查词动作配置多种快捷操作（快捷键），让查词更高效！

此外，本文将 **Mac词典打造的极致查词体验** 与 **「沙拉查词 + Alfred」打造的最佳文献翻译体验** 进行比较，探讨两者的应用场景与优劣势。

#### 直接看结果

在详细介绍Mac词典的打磨前，我们先亮结果。👇

![Mac词典查词界面](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808104918.png)


![Mac词典 - 三指屏幕取词](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200809171344.gif)



![Mac词典 - 快捷键查词](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808162332.gif)



![【沙拉查词 + PDF Expert】文献翻译- 作为比较](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808105413.gif)



亮完主要结果，下面详细道来。

### 导入第三方词库

为什么要导入第三方词库？

**主要有两个原因**：第一，Mac自带的英汉汉英词典在外观上过于简陋，想换个UI更好看的词典；第二，自带的词中没有符合自己需要的词典，比如各种外语或者专业词汇。

准备好待导入的第三方词库（`.dictionary`格式）。

打开Mac词典App，点击菜单栏`文件-->打开词典文件夹`，弹出下图所示的**Dictionaries**文件夹。

![词库文件夹 Dictionaries](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808110936.png)

将`.dictionary`格式的第三方词库拷贝到**Dictionaries**文件夹。（本文以导入**牛津9英汉词典**为例）

接着，切换到Mac词典App，并点击菜单栏`词典-->偏好设置`。

如下图所示，勾选☑️自己导入的第三方词库。也可以同时打开多个词典，长按词典拖动可以调整词典的显示顺序。

![勾选词库](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808112054.png)

至此，第三方词库就导入完成，可以放心使用了！

### 更美观、更强大的第三方词库

输入一个单词，即可进行查词。在下图所示箭头处，可以切换词典。👇

![【牛津9英汉词典】查词界面 - 深色模式](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808112429.png)

![【牛津9英汉词典】查词界面 - 浅色模式](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808112849.png)

可以看到第三方词库【牛津9英汉词典】的查词界面非常的好看，无论是在深色模式下还是浅色模式下，都显得非常精致。

总结一下【牛津9英汉词典】的特点，主要有以下几点：
- 排版精致，各种高亮颜色运用得当，区分度好，非常养眼。
- 支持读音，不论是单词还是例句都有美式和英式发音，而且发音非常的好听标准，是练习发音的好工具。
- 支持示意图。很多实物对应的单词都有美观的配图，比如Apple（苹果🍎），Cup（杯子🍷），Pencil（铅笔✏️）等等。
- 释义丰富。覆盖了单词含义、例句、拓展用法等方面的内容，总之释义上很到位，非常适合深入学习某个单词。
- 词库丰富，支持单复数的识别。
- 离线查词。因为有本地词库，Mac词典可以脱离网络使用。

### 查词快捷操作（快捷键）

一个功能有没有用，我们得找到它的应用场景。

Mac词典查词的其中一个应用场景便是**文献阅读时进行查词**。

下面介绍几种Mac词典查词的快捷操作。

#### 屏幕取词
得益于Mac词典的原生性，macOS系统为快捷查词设计了很多实用操作。

最为经典的便是 ***三指屏幕取词***，演示如下。👇



![三指屏幕取词](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200809171344.gif)

除了三指操作，屏幕取词还有一个系统内置的快捷键`CMD+CTRL+D`。

将光标放在某个单词上，然后同时按下`CMD+CTRL+D`，即可弹出取词窗口。如果想取词其他单词，只需按住`CMD+CTRL`保持不动，松开`D`键再按下即可。

屏幕取词的以上两个快捷操作方式的特点如下：
- **三指屏幕取词**。优点：单手完成，与滚动文献共用一只手，从而释放另外一种手，文献阅读体验更轻松。
- **CMD+CTRL+D** 屏幕取词。缺点：需要用另外一只手按下快捷键，而且该快捷键不是很顺手。

值得注意的是，屏幕取词时，**在取词悬浮窗口中，是无法播放读音的**，只有词典App中才能播放。

而且，如果你的PDF阅读器有跟随系统的深色模式，取词窗口也会变为深色。

以Mac自带的**预览App**为例，在深色模式下，取词窗口是下面这个样子的。

![深色模式下的悬浮取词窗口](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808143755.png)

**屏幕取词的一个优势在于**：由于采用了悬浮弹窗设计，因此它不需要占用额外的屏幕空间来显示取词窗口，从而让文献阅读窗口铺满整个屏幕，阅读体验更好。

#### 在独立窗口中查词 - 快捷键

如果你有一个较大的屏幕，将Mac词典与文献阅读软件（以PDF Expert为例）全屏并列显示会是一个不错的选择。

![Mac词典与PDF Expert并列全屏显示](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808115619.png)

或者，**如果你有双屏，一个屏幕放Mac词典，一个屏幕放PDF阅读器，就更棒了！**

这样做的好处在于，你可以边阅读文献边查词。

***更为重要的是***：在Mac词典内，你可以得到最快的查词响应速度，享受最好看的外观，可以播放单词或者例句读音，还可以快速浏览所有查词结果。

那么，如何像**沙拉查词 + Alfred**一样，将待查的单词传递给Mac词典呢？

放心，Mac系统的设计者已经为我们考虑到了这点。

打开Mac的`设置-->键盘-->快捷键-->服务-->在词典中查询`，设置一个顺手的快捷键。👇

![为【在词典中查询】设置快捷键](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808144856.png)

我设置的快捷键是`CMD+Shift+2`。

***设置该键位的好处在于***：用左手非常容易触达，而且键位分布与**沙拉查词 + Alfred**中的`CMD+Shift+D`很接近，便于培养肌肉记忆，防止误触。

顺便提一下，该快捷键本质上触发的是右键菜单**服务**中的**在词典中查询**。👇

![服务-->在词典中查询](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808145541.png)

而且只有在支持**在词典中查询**服务的App中，该快捷键才能生效。（PDF Expert是支持的）

配置完快捷键后，只需要选中某个单词，或者左键双击某个单词，使该单词处于选中状态，然后按下快捷键`CMD+Shift+2`，即可自动在Mac词典内查词。

![【CMD+Shift+2】快捷查词](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808150558.gif)

此外，如下图所示，点击Mac词典左上角的`A`，可以调整查词结果的文字显示大小。

![调整查词结果文字大小](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808150848.png)

至此，关于Mac词典的快捷查词操作就介绍完了。

### 将查词结果打印成PDF

如果你觉得某个单词很重要，将查词结果打印出来学习也是个不错的选择。

在Mac词典查词界面，按下`CMD+P`（或者菜单栏`文件-->打印`），即可进行打印。


![打印查词结果](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808151801.png)

打印时，推荐在左下角选择**存储为PDF**，即可将查词结果输出为PDF，这样做得好处在于可以保持彩色不丢失。

输出的PDF如下。👇

![将查词结果输出为PDF](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808152041.png)

**怎么样？这完美的排版，漂亮的配色，还是很养眼的吧！**

毕竟，这么好看的词典排版，不发挥到极致总有些浪费！

那么，不妨想一想，将查词结果打印成PDF有哪些应用场景？

我个人觉得在**课堂教学、子女英语教育**方面都是一个不错的选择！

### Mac词典与【沙拉查词 + Alfred】对比

再次将Mac词典的`CMD+Shift+2`查词操作，与【沙拉查词 + Alfred】的`CMD+Shift+D`翻译操作进行对比。

![Mac词典【CMD+Shift+2】查词](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808150558.gif)

![【沙拉查词 + Alfred】的【CMD+Shift+D】查词翻译](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808105413.gif)

看起来，两者有些异曲同工之妙！

不过，本质上两者还是有很多差异的，总结如下：
- **Mac词典**：仅支持查词，不支持段落翻译；可查单词的数量和词库本身有关；无需联网即可查词；更适合外语学习和轻度查词场景。
- **沙拉查词 + Alfred**：支持查词与段落翻译；查词数量和生僻度无限制，翻译长度无限制；需联网，不支持离线工作；更适合深度文献翻译场景。


### 【Mac词典打磨】视频教程

如果您对本文介绍的部分内容不太明白，可以观看下方的视频教程（推荐在我的B站主页观看），介绍得更加详细，还包括一些本文没有提及的内容。

B站视频

### 第三方词库下载

能否将Mac词典打磨得精致，主要取决于你的词库是否够优质。

#### 网络公开版词库

这里分享四个来自互联网的公开词库资源：
- 朗道英汉词典
- 朗道汉英词典
- 麦克米伦（macmillan）英汉词典
- 牛津、朗文、剑桥、柯林斯四合一词典

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;
  object-fit:contain;box-shadow: rgb(210,210,210) 0em 0em 0.5em 0px;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808154747.png" alt="往期精彩">

***公开版词库下载方式***：青柠学术公众号后台回复`Mac词库`。

#### 会员专享版词库

本文中介绍的**牛津9英汉词典**是我花费几十元购买的，自己一直在用。由于存在版权，这里不方便公开分享。

***对于加入青柠学术会员的朋友，我会以朋友的名义赠送给大家。***

除了**牛津9英汉词典**，还有一份最新的**朗文英汉词典第5版**，价值约**50元**。



<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;
  object-fit:contain;box-shadow: rgb(210,210,210) 0em 0em 0.5em 0px;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200808160401.png" alt="往期精彩">



加入会员即可立即领取，现在加入还有**优惠券可领**。


后面会继续介绍iPad上的文献翻译教程，而且还有字典赠送！

本文就到这里了，如果有疑问欢迎**留言讨论**；如果本文对你有所帮助，欢迎**文末三连**走起！