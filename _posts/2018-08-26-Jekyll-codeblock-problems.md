---
title: 解决Jekyll插入Liquid代码块编译出错问题
date: 2018-08-26 10:27:00
categories:
- 网站搭建
tags:
- Jekyll
typora-root-url: /Users/iseexuhs/Documents/GitHub/iseex.github.io
---

> 终于解决了困扰昨天一晚上的问题，先表达一下自己的开心😄！

昨晚在写博客[《在Jekyll NexT主题中部署wildfire评论系统》](https://iseex.github.io/2018-08/Jekyll-NexT-wildfire/)的时候遇到一个问题，就是我在博客中用markdown命令` ``` `插入代码的时候发现，总是编译出错，具体错误信息如下：

![](/assets/images/posts/GitHub-Pages/codeblock-liquid-tags.jpg)

意思是在我的博客中出现了GitHub无法识别的liquid tag `elsif`，我就坚持了下自己的博客，部分代码块是没有问题的，出问题的是包含liquid tag（不懂可以搜索jekyll liquid tag）的代码块。比如下面代码就无法编译通过：

{% highlight html linenos%}
{% raw %}
```
{% include _third-party/comments/wildfire.html %}
```
{% endraw %}
{% endhighlight %}

其实昨天在写一篇关于$LaTeX$公式的博客时页出现了一个代码块无法编译的问题，错误信息如下：

![](/assets/images/posts/GitHub-Pages/codeblock-errors-latex.jpg)

当时很郁闷，不过没有去深究，删除了那部分才编译通过。而且那个代码中不含liquid 由此可见GitHub不能识别的不仅仅是liquid tag。

通过在谷歌和百度上搜索，终于找到了答案，[见这里](https://blog.csdn.net/jireren/article/details/52197045)。

所以解决方案是，用：

```
{% highlight liquid linenos%}
{% raw %}
```

代码所在处....
```
{% endraw %}
{% endhighlight %}
```

