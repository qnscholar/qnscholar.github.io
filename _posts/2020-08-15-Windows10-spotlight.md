---
layout: post
title: 超实用！如何获取Windows 10锁屏壁纸？
date: 2020-08-13 22:36:00
tags: 
- Windows生产力
published: true
---



有一天，当我来到办公室，坐上座位上，轻触鼠标，当PC屏幕亮起来的那一刻，呈现在我眼前的是下面这张锁屏壁纸！👇

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:100%;
  height:100%;
  object-fit:contain;" src="https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200815131942.jpg" alt="往期精彩">

顿时就被这张照片吸引了！自认为这张照片拍摄得非常棒，取景也很独特！

于是我在思考，怎么能获取这张Spotlight锁屏壁纸的原图呢？

摸索了一番，总算找到了方法，因此也就有了本文。


#### 获取Windows 10锁屏壁纸

按下`Win+R`键，打开下面的**运行**窗口。
![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200815200724.png)

输入下面的代码，并确定。

```
%localappdata%\Packages\Microsoft.Windows.ContentDeliveryManager_cw5n1h2txyewy\LocalState\Assets
```

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200815200800.png)

自动打开下图路径。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200815200932.png)

Windows锁屏壁纸便保存在这个路径内，不过默认情况下并不是图片的格式，需要进行转换。👇

为了不对系统造成破坏，我们将该路径内的所有文件复制到电脑其他地方（比如桌面），并放在的一个文件夹内（比如起名为`Spotlight`）。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200815202752.png)

右键单击文件夹内的任何一个文件，点击属性菜单。

如下图所示，拷贝其路径，比如为`C:\Users\iseexuhs\Desktop\Spotlight`

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200815203020.png)

再次`Win+R`，输入`cmd`打开命令行窗口。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200815203357.png)

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200815203519.png)

输入命令 `cd "上一步复制的路径"`。

比如，此处为`cd "C:\Users\iseexuhs\Desktop\Spotlight" `，如下图所示。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200815203926.png)

按下Enter。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200815204008.png)

然后输入命令`Ren *.* *.jpg`，并运行。👇

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200815204145.png)

此时，便会发现Spotlight文件夹内的文件全部变为图片格式（`.jpg`）了。

![](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20200815204429.png)

看到本文开头的锁屏壁纸了吗？

更可以发现，**除了PC分辨率的图片，还有移动端的图片。**

到此，全部步骤就介绍完了，你get了吗？