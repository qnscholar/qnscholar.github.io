---
layout: post
title: wolai 近期新特性盘点！有何亮点？
date: 2021-10-16 22:36:00
tags: 
- wolai
- 笔记生态
published: true
---



好久没介绍wolai了，最近wolai有啥新动向呢？

本文就简单盘点一下。

#### 粘贴图片识别

早在8月初，wolai就提供了数学公式OCR识别功能，可谓加强了wolai的「学术属性」。

[wolai 支持公式识别、飞行模式，学生党的福音来了！](https://mp.weixin.qq.com/s/N7on2FjuHfYZZS_4jJNGjg)

今天，wolai进一步完善了公式识别的使用体验。

现在，**你可以通过粘贴图片，实现数学公式的快速识别了。**

以下两种图片粘贴方式均有效：

1. 粘贴本地的图片
2. 粘贴网络图片

以粘贴网络图片为例，比如我在知乎看到如下所示的**麦克斯韦方程组**。👇

![公式 - 网络图片](https://gitee.com/qnscholar/figurebed/raw/master/img/20211015223951.png)

首先，我们右键图片，选择**拷贝图像**。

切换到wolai，键入公式输入命令`/sxgs`。

![键入公式输入命令](https://gitee.com/qnscholar/figurebed/raw/master/img/20211015224149.png)

然后，在下面的输入框中按下`CMD + V`键（以Mac为例）。


![粘贴图片](https://gitee.com/qnscholar/figurebed/raw/master/img/20211015224239.png)

识别中...

![识别中](https://gitee.com/qnscholar/figurebed/raw/master/img/20211015224542.png)

1～2s后，识别成功。顺便得到了相应的$\LaTeX$代码。👇

![识别成功](https://gitee.com/qnscholar/figurebed/raw/master/img/20211015224612.png)

对比原公式发现，wolai识别出的公式没有任何差错，准确度非常高！

#### 块历史

现在，wolai的每一个块都可以查看/播放/恢复历史版本！（历史快照从2021年6月上旬开始自动保存）。

<img style="border-radius:10px 10px 10px 10px;
  text-align:center;
  display:block;
  margin:0px auto;
  width:280px;
  height:100%;box-shadow: 0px 4px 20px -5px #84A1A8;
  object-fit:contain;" src="https://gitee.com/qnscholar/figurebed/raw/master/img/20211015224928.png" alt="往期精彩">

该功能算是对用户数据安全提供的又一保障！点赞👍

#### 访客

wolai在团队协作上又更进了一步：增加「**访客**」功能。



<blockquote data-tool="科技兽" style="border-top: none;border-right: none;border-bottom: none;font-size: 0.9em;background: url(https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210519013028.png) 10px 10px / 40px no-repeat rgb(31,79,137);overflow: auto;color: inherit;border-left: 0px;padding: 1.2em 2em;margin-bottom: 2em;margin-top: 2em;text-align: center;border-radius: 10px;"><p style="font-family: Optima-Regular, Optima, PingFangSC-light, PingFangTC-light, &quot;PingFang SC&quot;, Cambria, Cochin, Georgia, Times, &quot;Times New Roman&quot;, serif;text-align: justify;line-height: 26px;margin-top: 1em;margin-bottom: 0.3em;font-size: 14px;color: rgb(255, 255, 38);"><strong style="color: #fc8705;">wolai 访客</strong><br  />您可以邀请公司或团队外的伙伴加入您的页面成为访客，通过为他们设置不同的页面权限与您共同协作。访客仅能看到被邀请协作的页面。</p></blockquote>

wolai官方的[帮助中心](https://www.wolai.com/wolai/8XtDuVgByhv7SDKAykmJDj )详细介绍了「访客」功能的使用方法，感兴趣可以自行查看。

![「访客」功能的使用方法](https://gitee.com/qnscholar/figurebed/raw/master/img/20211015230527.png)

不过，你还记得我之前写的下面的文章吗？

[如果 wolai 团队空间向 Zotero 群组看齐，会如何？](https://mp.weixin.qq.com/s/kxZ_VjN1q5G3p1b89aGRPQ)

我期待的wolai团队空间更像是Zotero群组那样的。

或者，在保留现有团队空间类型的基础上，提供一种Zotero群组那样的就好了。🌝