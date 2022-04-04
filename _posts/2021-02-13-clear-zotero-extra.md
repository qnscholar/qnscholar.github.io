---
layout: post
title: 巨巨有用！如何清空Zotero其他（extra）字段的信息？
date: 2021-02-13 22:36:00
tags: 
- Zotero
published: true
---





之前在下面三篇推文中，介绍了Zotero文献引用量插件Zotero Scholar Citations和Zotero Citation Counts Manager。👇

- [引用量 \| 无限制版Zotero Scholar Citations插件来了！](https://mp.weixin.qq.com/s/hSJLfcjd_uErdXsQCKtCAQ)
- [Zotero \| 又一个超好用的文献引用量插件来了！](https://mp.weixin.qq.com/s/FkXcHWA3kvTQ5yFegKnsfw)
- [Zotero Scholar Citations插件，帮你显示Zotero文献引用量！](https://mp.weixin.qq.com/s/44ADU_pE5-9n2DxY3d_IEg)

之后，有很多粉丝留言道：**如何清除Zotero其他（extra）字段的内容？**

之所以有这样的需求，是因为**有的文献在导入Zotero时，其他（extra）字段就自带内容**，比如Publisher、PMID等等。

![其他（extra）字段](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210213154101.png)

这些自带的内容不仅没多大用，在更新文献引用量时，还特别占位置。

清除其他（extra）字段的方法有多种，下面就介绍一种比较彻底的[方法](https://forums.zotero.org/discussion/comment/373181#Comment_373181)（PS：感谢微信群的一位学员提供）。

### 清除Zotero其他（extra）字段信息

我以Mac虚拟机上的Windows版Zotero（我的小号）演示。

首先，可以看到，下面这些文献的其他（extra）字段原本是有内容的。

![其他（extra）字段的原本信息](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210213154915.png)

我们进入Zotero菜单栏`工具-->开发者-->Run Javascript`，如下。

![工具-->开发者-->Run Javascript](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210213155131.png)

弹出下面的窗口。

![Run Javascript](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210213155314.png)

将下面的代码粘贴到Code区域。

```javascript
var fieldName = "extra";
var newValue = "";

var fieldID = Zotero.ItemFields.getID(fieldName);
var s = new Zotero.Search();
s.libraryID = ZoteroPane.getSelectedLibraryID();
var ids = await s.search();
if (!ids.length) {
return "No items found";
}
await Zotero.DB.executeTransaction(async function () {
for (let id of ids) {
let item = await Zotero.Items.getAsync(id);
let mappedFieldID = Zotero.ItemFields.getFieldIDFromTypeAndBase(item.itemTypeID, fieldName);
item.setField(mappedFieldID ? mappedFieldID : fieldID, newValue);
await item.save();
}
});
return ids.length + " item(s) updated";
```
也就是这个样子。👇

![粘贴代码到Code区域](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210213155514.png)

然后，按照下图，点击**Run**，快捷键为`Ctrl+R`或者`CMD+R`。

![点击Run](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210213155747.png)

接着，会在Return Value面板显示运行结果。



![运行结果](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210213155903.png)

比如我的结果是`24 item(s) updated`，即：更新了24个文献条目。

此时发现Zotero文献的其他（extra）字段的信息已经被清空了，搞定！

![其他（extra）字段的信息成功清空](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210213160213.png)

下面有注意事项，一定要看！👇

### 注意事项

不禁要问，为什么是更新了24个文献条目呢？

我们展开刚刚所在的AcousticDevices文件夹内的所有文献。

![展开所有文献](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210213160915.png)

可以看到正好是24个条目，其中包括了文献下面的PDF附件。

这下明白了！

通过Run Javascript清除其他（extra）字段的信息，仅仅对当前选中的文件夹内的文献有效。

比如我上面选中的是群组中的AcousticDevices文件夹。

那么，如果想要清除我的文库内所有文献的其他（extra）字段的信息：

***请先选中`我的文库`*** ，再按照前面介绍的方法操作即可。（安全起见，建议先备份文献）

![先选中我的文库，再Run Javascript](https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20210213161550.png)