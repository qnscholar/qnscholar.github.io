---
layout: post
title: 【PicGo + gitee】图床打造，最详细攻略！
date: 2021-07-29 22:36:00
tags: 
- 效率工具
published: true
---

之前在下面的推文中向大家介绍了【PicGo + 阿里云OSS】的图床方案。

1. [PicGo + 阿里云OSS，最详细的图床配置教程！](https://mp.weixin.qq.com/s/Mry9_HdLbXz8w4_874_7eQ)
2. [PicGO图床详细教程，及其妙用揭晓？](https://mp.weixin.qq.com/s/vGblYphDIx23uyozoAqUiw)

尽管阿里云OSS的存储空间年费并不高，但是流量费用还是有些小贵的，特别是对于经常使用图床的用户，可能无法承受。

GitHub图床是另一个方案，但是GitHub在国内访问速度感人，做图床简直没法用。

为此，今天将利用国内的**gitee**（相当于中国版“GitHub”），并结合PicGo，打造免费又快速的图床。

  <span style="line-height:1;padding:0px 20px;font-size:12px;display:block;text-align:center;color:gray;">（又可以省下一笔开支）</span>


### gitee + Picgo 图床

首先，进入PicGo的`设置-->插件设置`，搜索`gietee`。👇

![插件设置](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729182539.png)

这里我们选择第三个**gitee-uploader 1.1.2**进行安装。

此时会弹出需要先安装**node.js**的提示，而且会自动跳转到下面的[网页](https://nodejs.org/en/)。

![gitee-uploader 1.1.2](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729183000.png)

以Mac为例，这里我下载安装左边的`14.17.3 LTS`。

接着，重新打开PicGo，再次搜索**gitee-uploader 1.1.2**，即可顺利安装。👇

![](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729183109.png)

接下来，我们进行gitee图床仓库的创建。


#### 创建gitee图床仓库

首先，到[gitee官网](https://gitee.com )注册一个账号。

![gitee官网](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729183836.png)

登录后，在右上角的+号处，点击**新建仓库**。

![新建仓库](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729184342.png)

按照下图所示，设置仓库信息。


![设置仓库信息](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729184750.png)

包括：

1. 随意起个`仓库名称`，比如叫做figurebed。
2. 选择`开源`。
3. 勾选`设置模板-->Readme文件`。
4. 勾选`选择分支模型-->单分支模型（只创建master分支）`。

点击**创建**，进入下一步。

#### 获取token（私人令牌）

在你的gitee头像处，进入**设置**。

![设置](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729185449.png)

如下图，点击左侧的**私人令牌**。

![私人令牌](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729185628.png)

点击**生成新令牌**。

![生成新令牌](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729185721.png)

如下图，先取消全选，再勾选**projects**，然后提交。

![](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729185825.png)

提示要输入gitee账户密码，输入即可。

![输入gitee账户密码](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729190028.png)

**到此便获得了私人令牌**，点击**复制**，并保存好。因为该窗口关闭后，将无法再查看该私人令牌。

![复制 私人令牌](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729190154.png)

#### 在PicGo中配置gitee图床

进入PicGo设置界面，在左边找到gitee。

按照下图进行gitee图床的配置。

![](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729190608.png)

其中：

1. **repo**处填写`gitee账户名/仓库名`。
2. **branch**处填写`master`。
3. **token**处填写上一步获取的`私人令牌`。
4. **path**处填写`img`。
5. 其他的保持默认，不用管。

顺便提一下，`gitee账户名/仓库名`可以在你的gitee仓库的网页地址中复制。👇

![](https://gitee.com/qnscholar/figurebed/raw/master/img/20210729191249.png)

填写完毕后，点击**确定**，并**设置为默认图床**。

到此，便完成了「gitee + Picgo 图床」的所有设置，接着即可使用了，新手可阅读这个[教程](https://mp.weixin.qq.com/s/vGblYphDIx23uyozoAqUiw)。

总之，有了图床后，就可以在诸如Typora、Obsidian等Markdown编辑器中用上了。

#### 下载

本文涉及的PicGo和node.js的Mac/Win版安装包我已经备好了。

1. PicGo
2. node.js

**下载**：`青柠学术`公众号后台回复`图床`获取安装包。

#### gitee图床的局限性

试想一下，如果大家都这么免费无节制的使用gitee的存储，它的服务器怎么承受得住？

所以，**gitee图床也是有一定局限性的**：如果上传大于1MB的图片，图片插入到markdown编辑器后，是无法显示出来的。

这里推荐两种节约成本的方案：

1. **免费方案**：利用图片压缩工具将图片压缩到小于1MB，然后再用Picgo上传到gitee。（我用的是Mac上的[Image Optimizer](https://mp.weixin.qq.com/s/BgWqDjEW2Z5M9LPsbOo4NA)图片压缩工具，非常棒）
2. **低成本方案**：大于1MB的图片采用阿里云OSS图床，小于1MB的图片采用gitee图床。


本文就介绍到这里，希望对你有所帮助！