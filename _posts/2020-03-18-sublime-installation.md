---
layout: post
title: 玩转Sublime Text 3｜软件安装与汉化（附下载链接）
date: 2020-03-19 09:30:00
tags: 
- 效率工具
published: true
---

**Sublime Text 3，一款流行的的代码/文本编辑神器。简洁美观，功能强大。**

我在平时写博客、编辑文本时，习惯用Sublime Text 3，慢慢已经离不开它了！

今天就以macOS系统为例，和大家聊聊Sublime Text 3的安装与汉化。

当然，未来可能会深度介绍Sublime Text 3的使用技巧。

###   Sublime Text 3安装

**Sublime Text 3 for Mac安装包下载方式：**「青柠学术」公众号后台回复`Sublime Text`获取下载链接。

这里分享的安装包为：`Sublime+Text+Build+3208.dmg`，且安装即破解。

下载完成后，双击安装包。弹出下面窗口，拖动Sublime Text到Applications文件夹。

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyrhbai9j30oi0f874i.jpg)

接着，在应用程序内找到Sublime Text并双击。

此时，如果你的系统为macOS Catalina，可能会弹出**“Sublime Text”已损坏，无法打开。您应该将它移到废纸篓。”**

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyr7c6rkj30n20dsq3q.jpg)

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyrgkgccj30es07ft9u.jpg)

这里的解决办法是，打开终端，粘贴下方命令。

```
sudo xattr -r -d com.apple.quarantine
```

**紧接着，在上面命令后面按一下空格（切记不要忘了！！）**，接着将Sublime Text从应用程序内拖动到终端窗口，此时会自动填充路径，然后回车。

提示需要输入密码，**输入电脑密码并按回车**（输入时密码处于隐藏状态），如下。👇👇

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyrib6tcj30iy0d9gm6.jpg)

此时，再回到应用程序，双击Sublime Text，发现可以成功打开软件，界面如下。

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyrd681pj30qg0iomxf.jpg)

为了验证是否为破解版，可以点击菜单栏Sublime Text-->About Sublime Text，破解信息如下。

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyrekjmhj30c507sdgq.jpg)

###   Package Control安装

Package Control可以用来为Sublime Text安装丰富的插件，因此Package Control的安装是个必备环节。

这里介绍两种安装Package Control的方式（任选其一即可）。

#### 用Python代码安装

点击Sublime Text的菜单栏View-->Show Console，调出Console，如下。

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyra0f55j30qg0iojs3.jpg)

然后，将下方代码粘贴进去并按回车。

**Sublime Text 3（这里我们选择此代码）：**

```
import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

**Sublime Text 2：**

```
import urllib2,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')
```

不出意外会安装成功。

**判断是否成功安装Package Control的方式为：**

点击菜单栏Sublime Text-->Preferences，如果能找到下图所示的Package Control表示成功安装。

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyr94cgrj307k07saap.jpg) 

#### **手动安装**

点击Sublime Text 3菜单栏Sublime Text-->Preferences-->Browse Packages，会自动打开下面目录。

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyrf5fraj30oi0f8jrx.jpg)

这里我们进入该目录的上级目录，并进入Installed Packages文件夹。如下👇👇

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyrdnikyj30oi0f8t9i.jpg)

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyrc859wj30oi0f8gm8.jpg)

然后，用下面提供的链接下载**Package Control.sublime-package**，并拷贝到上述Installed Packages文件夹。

https://sublime.wbond.net/Package%20Control.sublime-package

重启Sublime Text，即可成功安装Package Control。

###   汉化

Sublime Text支持多种语言，目前支持的语言包括：

简体中文 繁体中文 日本語 Chinese Japanese German Russian Spanish Armenian Swedish and French

详情可访问：

https://github.com/rexdf/ChineseLocalization

下面就介绍下如何将Sublime Text汉化。👇

Sublime Text的汉化有很多方式，这里介绍一个最简单也最不容易出错的方式：通过Package Control安装汉化插件。

（这也是为什么我首先在前面介绍了如何安装Package Control）

按下快捷键`CMD+Shift+P`（或者点击菜单栏Tools-->Command Palette），然后输入install，选中`Package Control: Install package`并回车，如下。👇👇

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyr8fdcoj30qg0iodge.jpg)

然后，输入chinese，选择`ChineseLocalizations`并回车，如下。👇

![img](https://tva1.sinaimg.cn/large/00831rSTly1gcyyrae2rjj30qg0iot9p.jpg)

到此汉化就成功了，这时会自动弹出一个关于ChineseLocalizations汉化插件的使用说明。

**如果想要更改其他语言，点击菜单栏Help-->Language，即可选择需要的语言。**

汉化前后Sublime Text的界面对比如下。👇

![汉化前](https://tva1.sinaimg.cn/large/00831rSTly1gcyz2ohgspj30u00irwg0.jpg)

![汉化后](https://tva1.sinaimg.cn/large/00831rSTly1gcyz37yn83j30u00irmym.jpg)

