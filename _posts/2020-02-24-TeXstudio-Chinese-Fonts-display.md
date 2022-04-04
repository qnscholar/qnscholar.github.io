---
layout: post
title: “macOS Catalina下TeXstudio内置PDF阅读器无法正常显示中文”的解决办法！
date: 2020-02-24 20:00:00
tag: 
- LaTeX
---

关于“macOS Catalina下TeXstudio编译中文文档，内置PDF阅读器无法显示中文，而外部PDF阅读器能够正常显示”的解决办法[^1]。

 打开终端，输入以下命令：

```
ln -s /System/Library/Fonts/Supplemental/Songti.ttc /Library/Fonts 
```

执行命令，即可解决问题。👇

![](https://tva1.sinaimg.cn/large/0082zybply1gc7jqtojbkj30iy0d9t9d.jpg)

打开TeXstudio，运行一个ctexart文档试试效果。

![](https://tva1.sinaimg.cn/large/0082zybply1gc7jriys77j314c0o0dip.jpg)

当然以上只是临时解决方案，想要根本性解决问题还需等待CTEX宏集更新。

[^1]:  [[LaTeX使用]升级 macOS 10.15 后 ctex 文档不显示中文的临时方案](https://zhuanlan.zhihu.com/p/90404943)

