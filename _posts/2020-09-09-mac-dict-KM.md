---
layout: post
title: Mac词典打磨，第二弹！
date: 2020-09-06 22:36:00
tags: 
- Mac生产力
- 文献阅读与翻译
published: true
---

之前在下面这篇推文中，全面而详细地介绍了如何打磨Mac词典，创造极致查词体验！

[Mac词典打磨，创造极致查词体验！](https://mp.weixin.qq.com/s/fyck4PpL6dmi7IhEmx12Xw)

其中一项内容是为查词操作设置快捷键，我设置的是`CMD+Shift+2`，并用一张动图演示了在PDF Expert中的查词效果。

不过，相信有些读者已经发现了，该快捷键对Mac自带的**预览App**并不奏效。

但是，Mac预览又实实在在提供了`在词典中查询`这样一个服务菜单。

![Mac预览](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200907164442.png)

所以，不知道是bug，还是苹果屏蔽了该服务。

Anyway，那干脆另辟蹊径，寻找一种更好的方案。

也就是本文要说的。👇

#### Keyboard Maestro + Mac词典

Keyboard Maestro (KM)，Mac上的workflow神器，第一次向大家介绍是在我的第一支剪辑视频中。👇

[又一个超级实用的文献翻译技巧！get起来！](https://mp.weixin.qq.com/s/bPC0seicGvVPRh-P9JzqIQ)

今天，要再次利用KM实现更强大的Mac词典快捷查词。

如果将Mac词典词典快捷查词操作拆解一下，是这样的：

1. 拷贝选中的单词至剪贴板。
2. 启动Mac词典。
3. 在Mac词典的搜索框粘贴第一步拷贝的单词，自动出现查词结果。

可以看到，拆解之后，整个查词工作流简单明了。

为此，我们便可以在Keyboard Maestro中设置以下工作流：👇

![在KM内设置Mac查词工作流](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200907170139.png)

放大一下。

![工作流设置放大图](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200907170253.png)

**分析如下：**

触发条件设置为快捷键`CMD+Shift+2`。

![触发条件](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200907170444.png)


一旦你按下了快捷键`CMD+Shift+2`，KM会自动执行下面三个步骤。

![执行步骤](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200907170540.png)

1. Copy。（即复制选中的单词）
2. Activate 词典。（启动词典）
3. Simulate keystroke CMD+V。（模拟按下CMD+V，即粘贴单词）

**通过该工作流，即可脱离Mac的`在词典中查询`服务，实现在任意应用内的快捷查词。**

不管是PDF Expert，Mac预览，还是浏览器等等，选中单词，按下`CMD+Shift+2`即可放心查词了。

![Mac词典](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200907173349.png)

这套查词的玩法，主要是为了利用系统原生应用Mac词典的极速启动，以及经过打磨后Mac词典精致的外观和排版。

当然，双屏下查词体验更加，无需切换窗口。

#### 注意事项

如果你使用本文介绍的`Keyboard Maestro + Mac词典`组合，请取消勾选Mac设置中的`在词典中查询`快捷键，防止与KM的快捷键冲突。

![取消勾选`在词典中查询`快捷键](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200907172452.png)

另外，建议将Keyboard Maestro设置为开机启动。

![Keyboard Maestro - 开机启动](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200907172717.png)

#### 下载

**Keyboard Maestro下载**：`青柠学术`公众号后台回复`KM`获取下载链接。


如果本文对你有所帮助，欢迎**三连走起**！

