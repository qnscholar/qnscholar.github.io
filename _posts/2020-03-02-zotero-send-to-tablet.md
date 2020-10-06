---
layout: post
title: 重磅｜Zotero + Tablet，跨平台文献同步的新姿势！
date: 2020-03-02 12:37:00
tags: 
- Zotero
published: true
---

之前一直向大家主推【Zotero+坚果云+PaperShip】组合来实现跨平台文献同步，青柠的读者们也基本采用的这种方式。

确实，这个强大组合让我们能够随时在不同设备上阅读和批注Zotero中的文献，并做到实时同步。

不过，什么东西做到完美都很难。

【Zotero+坚果云+PaperShip】这个组合也不例外，有它的一些不足或者局限性，比如：

- PaperShip只有iPad和iPhone版，因此安卓用户无法使用。尽管安卓平台也有个别能同步Zotero文献的App，但是说实在的质量太差了，而且据我所知没有批注功能。
- PaperShip的批注功能内购价格为68元，也不算便宜。当然如果你只想同步和阅读，不需要批注，这68元也就不用花。如果你想要批注功能却又不想花这份钱，不妨加入青柠学术VIP，[我已经为大家买好了](https://mp.weixin.qq.com/s/lSLGRv7jS05SuJJejagzeQ)，并且近100位用户已经享用了。
- 【Zotero+坚果云+PaperShip】这个组合需要一些和WebDAV相关的配置步骤，虽然说有了我的教程保证你配置成功，但是应该会有人不想费这个劲。

因此，今天我给大家带来实现Zotero文献跨平台同步的另一种方式：通过Tablet功能，实现Zotero文献与PDF Expert等PDF阅读软件的文献同步。

下面听我一一道来。

### 什么是Tablet功能？

Tablet（或者说平板）并不是什么新鲜功能，只是之前我一直没和大家提过，因此估计很多人很陌生。

准确来说，Tablet功能并不是Zotero自带的，而是由Zotfile插件带来的。

顺便夸赞一句Zotfile，可以说Zotfile是Zotero平台最强大最重要的一款插件了，有了它我们可以用自定义格式重命名（rename）文献PDF，可以通过链接文件方式实现Zotero文献的网盘同步（以后介绍），以及今天这个Tablet功能。

打开Zotero，点击菜单栏Tools-->Zotfile Preferences，在下方窗口中点击`Tablet Settings`，即可对Tablet功能进行设置。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgmqed8ivj30k60lv40j.jpg)

那么Tablet的究竟能做些什么？上图中的一段文字就是对Tablet功能的描述，我来解释下。

通过Zotfile插件的Tablet功能，你可以将想要阅读和批注的文献发送到Tablet（平板）上，比如iPad或者安卓平板。

需要认识到的是，不仅仅是iPad或者安卓平板，其实iPhone、安卓手机或者其他任何有网盘同步能力的设备都可以。因此可以认为这是`广义`上的Tablet，只是因为这个功能主要用在平板上，所以就叫做Tablet了。

那么，Tablet功能的具体原理是啥呢？

首先你需要在网盘中建立一个文件夹，用于Zotero与平板端PDF阅读软件间的文献同步。

为什么必须是网盘文件夹呢，因此该文件夹需要和平板PDF阅读软件的云同步功能绑定起来。

那么，什么类型的网盘可以呢？这个和你在平板上使用的PDF阅读软件有关系，因为不同App具有的云存储类型有所区别，比如PDF Expert可以与iCloud、Dropbox、谷歌云、Box、OneDrive等进行文件的同步。

比如我喜欢iCloud（苹果原生，同步速度快），那么我就将iCloud和PDF Expertj进行绑定。（其实默认就是绑定的，这就是iCloud的生态优势）

这里提一个注意事项：请确认，你所选择的PDF阅读App的云同步功能是直接与网盘同步，而不是将网盘中的文件导入到App中，因为导入后就和网盘没有关系了，因此便无法实现无缝同步（除非你手动再导出到网盘）。

一旦你建立好网盘文件夹后，就需要在上图中设置该文件夹的路径。

设定好后，通过Send to Tablet功能，Zotfile会将想要在平板上阅读的文献PDF复制到该文件夹。此时平板上的PDF阅读软件便能通过云同步功能立即查看到这些文献。

因此我们就可以在平板上阅读或者批注这些文献了。

一旦你对某篇文献进行了批注，就相当于对该PDF进行了修改，此时电脑端的Zotfile会自动识别到Tablet文件夹中的PDF发生了变化，此时我们通过Get from Tablet便能够将Tablet文件夹内的PDF（即平板上批注的文献）取回到该文献的原始位置（即storage文件夹内），且保留所作的批注。同时可能会自动提取批注存放在单独的Notes附件中（和阅读软件有关系）。

下面我将以PDF Expert为例，详细介绍Tablet的配置步骤。

### 同步示例：Zotero+Tablet+PDF Expert

在平板上下载PDF Expert（我身边没有iPad，就用iPhone演示）。

默认情况下，PDF Expert就是与iCloud同步的，而且会自动生成一个`PDF Expert`文件夹，因此我们可以省去手动建立同步文件夹的这一步。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgnyycw24j30u0122q6i.jpg)

我们回到电脑端的iCloud，可以看到同样存在一个`PDF Expert`文件夹。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgqho3uauj30oi0f8myf.jpg)

接着我们在下图的`Location of Files on Tablet`设置为电脑上iCloud中`PDF Expert`的路径。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgo41av7jj30k60lv40l.jpg)

上图还有一个`Subfolers`功能，可用于按照指定格式将文献进行分类，方便在平板上查看，这个大家根据需要自行设定，这里不多介绍。

接着，我们在Zotero中，选中想要在平板上阅读的文献，然后右键选择Manage Attachments-->Send to Tablet。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgoacwxpyj31740q7af3.jpg)

此时Zotero左侧会自动生成`Tablet Files`和`Tablet Files (modified)`文件夹（准确来说叫做`搜索集`）。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgqsc62u1j31740q741h.jpg)

其中`Tablet Files`存放的便是刚刚选中的几篇文献。

此时，我们可以顺便看下电脑本地iCloud PDF Expert文件夹中是否有刚刚发送的文献。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgogkmd33j30oi0f8jsa.jpg)

选中3篇文献，成功发送3篇文献，没毛病。

接着，切换到移动端（iPad等设备）的PDF Expert中，并打开PDF Expert文件夹。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgokspexhj30u0122zmx.jpg)

可以看到这3篇文献秒速同步过来了，非常的迅速。

假如此时想在iPad上阅读文献了，那我们就用PDF Expert打开PDF进行阅读和批注即可。

比如我做了一些高亮、删除线、文字注释。👇

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgosn63jyj30u012279h.jpg)

批注完，返回，可以看到PDF Expert会立即向iCloud同步对该文献所作的修改，并以进度条显示。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgqkgsxpvj30u0122ju5.jpg)

待同步完毕后，我们回到电脑端Zotero。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgowbev8tj31740q740z.jpg)

可以看到，Zotfile几乎同时识别到了我们对文献的修改，并自动将被修改的文献分类到`Tablet Files (modified)`文件夹中。而还未批注的文献依然保存在`Tablet Files`文件夹内。

假如我们以后还要继续阅读和批注刚刚那篇文献，那么该文献会一直保存在`Tablet Files (modified)`中。

假如已经阅读和批注完毕，此时我们右键该文献，选择Manage Attachments-->Get from Tablet，即可将该文献移动到原始位置进行覆盖。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgp1ud7ytj31740q7q7h.jpg)

此时我们打开该文献，可以看到所作的批注全部同步过来了，且`Tablet Files (modified)`中的文献条目被移除了。

![](https://tva1.sinaimg.cn/large/00831rSTly1gcgp71pqzuj30xc0p478b.jpg)

怎么样，还是很完美的吧！

所以我们可以假定一个生活中的出差场景：

在办公室打开Zotero-->选中想要阅读的文献，Send To Tablet-->带上iPad，准备出门-->在高铁上拿出iPad，用PDF Expert阅读和批注文献-->出差回到办公室-->在Zotero中Get from Tablet-->一切搞定

### 总结

除了【Zotero+坚果云+PaperShip】，【Zotero+Tablet】的组合是又一种实现跨平台文献同步的方式。

而且我认为未来这种方式会更加流行，主要基于以下几点考虑：

- 该方式操作简单，没有复杂的配置步骤，且一步到位，不存在配置失败的情况。
- 突破设备限制，理论上该方式可以实现Zotero与所有常用终端的文献同步，iPhone、iPad、安卓手机、安卓平板等等，毫无压力。
- PDF Expert、MarginNote、Notability、GoodNotes等阅读/批注软件越来越流行，文献阅读体验好，功能强大，且一般都有强大的云同步功能，因此和Tablet功能搭配起来将是一个趋势。
- 可以做到不花一分线实现【Zotero+Tablet】文献生态，虽然像MarginNote等App是收费的，但是免费又好用的PDF阅读/批注软件同样有很多选择（如PDF Expert、PDF Viewer等）。