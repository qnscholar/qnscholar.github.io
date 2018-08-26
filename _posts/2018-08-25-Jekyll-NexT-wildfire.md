---
title: 在Jekyll NexT主题中部署wildfire评论系统
date: 2018-08-25 18:53:00
categories:
- 网站搭建
tags:
- Jekyll
- NexT theme
- wildfire
typora-root-url: ../../iseex.github.io
---

最近在搭建博客的时候，一直在考虑评论系统用哪一个。由于很多知名的评论系统相继停止服务，如Disqus、duoshuo，尚存活的几个评论系统，要么需要ICP备案（如畅言），要么就是加载很慢（如来必言）。唯一两个比较稳定的就是Git家族的gitalk和gitment了，我的博客就是部署的gitalk。gitalk很稳定，加载快，评论和repository的issues是连接的，只是gitalk需要登陆GitHub 账号才能评论，所以面向的人群会窄点。通常，面向大众的评论系统用邮件或者微信、QQ等社交账号登陆，所以我一直在寻找这样一款适用于GitHub Pages的评论系统，于是上网搜索了好久。

后来，意外地发现一篇博客提到了wildfire评论系统，有中国人开发，目前负责的人叫做cheng-kang，我还star了wildfire的开源代码。了解wildfire，可以参考下面几个链接。

- [GitHub](https://github.com/cheng-kang/wildfire)源码。
- [英文官网](https://wildfire.js.org/)。
- [中文官网](https://wildfire.js.org/#/zh-cn/)。

wildfire是一款通过邮箱注册进行评论的系统，目前也支持匿名评论。GitHub上有个版块[我们正在使用wildfire野火评论系统](https://github.com/cheng-kang/wildfire/wiki/%E6%88%91%E4%BB%AC%E6%AD%A3%E5%9C%A8%E4%BD%BF%E7%94%A8-Wildfire-%E9%87%8E%E7%81%AB%E8%AF%84%E8%AE%BA%E7%B3%BB%E7%BB%9F%EF%BC%81)展示了一些已经接入wildfire的博客网站。

看起来挺满足我对一个好的评论系统的期待的，要是能部署在我的博客中就好了。可是，wildfire开发者提供的资料都是讲如何将wildfire部署在基于Hexo框架的博客中。我到谷歌搜索“Jekyll + wildfire”也没找到任何资料（很大可能是因为wildfire诞生还不久）。

眼看希望就要落空，只能自己先尝试了。因为之前为我的博客添加很多功能时，也是依照Hexo的教程进行移植的，基本都成功了。于是，我就照着wildfire在Hexo上部署的[教程](https://mrliao.cn/2017/12/25/%E5%9C%A8Hexo.NexT%E4%B8%BB%E9%A2%98%E4%B8%AD%E9%83%A8%E7%BD%B2Wildfire%E8%AF%84%E8%AE%BA%E7%B3%BB%E7%BB%9F/)，尝试进行移植。然而，试了好久都失败了，总是提醒编译不通过（emmm，主要是我个人缺乏前端设计的基础，看来程序员进阶之路还很漫长啊，哈哈哈）

绝望之时，我就尝试在wildfire的GitHub的issues版块提问（上面有很多问题，讨论的很热烈，我就猜测或许开发者能帮我解决这个问题），于是我提了如下问题。

![](/assets/images/posts/GitHub-Pages/Jekyll-wildfire.jpg)

本来没抱太大希望，不过没想到第二天我就收到了邮件，开发者cheng-kang回复issues的邮件，很是惊喜！

经过几次邮件的交流，最后我就表达了真心希望在Jekyll NexT主题中部署wildfire的想法。

更让人惊喜的是，第二天早上起来就收到一封来自cheng-kang的邮件，他帮助我将wildfire部署在Jekyll NexT中了，并给了我[源码](https://github.com/wildfirejs/jekyll-theme-next)以及他在Jekyll NexT上push 了希望将wildfire接入到发行版中的[request](https://github.com/Simpleyyt/jekyll-theme-next/pull/93)。

[这里](https://github.com/wildfirejs/jekyll-theme-next/commit/f304f30d95af9f9f115f4813d41824c934e15747)说明了该如何修改Jekyll NexT主题，分以下几个步骤：

在_config.yml中添加如下代码，具体参数需要自己注册firebase或者wilddog，并[配置好数据库](https://wildfire.js.org/#/zh-cn/usage)，获取参数。

```yaml
# <wildfire>
wildfire:
  enable: false
  # version - It's recommended to use the following versions.
  loaderVersion: 1.2.5 #https://www.npmjs.com/package/wildfire-comment
  useDev: true
  version: 0.5.6 
  # database config
  databaseProvider: firebase # or wilddog
  firebase: # your firebase config goes here ↓
    apiKey: 
    authDomain:
    databaseURL:
    projectId:
    storageBucket:
    messagingSenderId:
  wilddog: # your wilddog config goes here ↓
    siteId:
  # other configs
  theme: light # or dark
  locale: en # or other locales, e.g. zh-CN
  defaultAvatarURL: 
# Any question? 
# Raise an issue here: https://github.com/cheng-kang/wildfire/issues
# </wildfire>
```

进入`_includes/_macro/post.html`，在下面位置添加代码。



{% highlight html linenos%}
{% raw %}
                        data-disqus-identifier="{{ post.url }}" itemprop="commentCount"></span>
                 </a>
               </span>

此处添加代码

             {% elsif site.hypercomments_id %}
             <!--noindex-->
               <span class="post-comments-count">
{% endraw %}
{% endhighlight %}


添加代码后如下：

{% highlight html linenos%}
{% raw %}
                        data-disqus-identifier="{{ post.url }}" itemprop="commentCount"></span>
                 </a>
               </span>
             {% elsif site.wildfire.enable %}
               <span class="post-comments-count">
                 <span class="post-meta-divider">|</span>
                 <span class="post-meta-item-icon">
                   <i class="fa fa-comment-o"></i>
                 </span>
                 <a href="{{ post.url | relative_url }}#comments" itemprop="discussionUrl">
                   <span class="post-comments-count wf-count-unit" wf-page-url="{{ post.url | absolute_url }}" itemprop="commentCount"></span>
                 </a>
               </span>
             {% elsif site.hypercomments_id %}
             <!--noindex-->
               <span class="post-comments-count">
{% endraw %}
{% endhighlight %}


进入`_includes/_partials/comments.html`，添加wildfire使能判断，比如以下位置：


{% highlight html linenos%}
{% raw %}
      <div id="lv-container" data-id="city" data-uid="{{ site.livere_uid }}"></div>
     {% elsif site.changyan.appid and site.changyan.appkey %}
       <div id="SOHUCS"></div>
此处添加代码
     {% endif %}
   </div>
 {% endif %}
{% endraw %}
{% endhighlight %}


添加如下代码：


{% highlight html linenos%}
{% raw %}
      <div id="lv-container" data-id="city" data-uid="{{ site.livere_uid }}"></div>
     {% elsif site.changyan.appid and site.changyan.appkey %}
       <div id="SOHUCS"></div>
     {% elsif site.wildfire.enable %}
       <div class="wildfire_thread"></div>
     {% endif %}
   </div>
 {% endif %}
{% endraw %}
{% endhighlight %}


进入`_includes/third-party/comments/index.html`添加下面代码：

{% highlight html linenos%}
{% raw %}
{% include _third-party/comments/wildfire.html %}
{% endraw %}
{% endhighlight %}


新建文件`_includes/_third-party/comments/wildfire.html`，添加代码：



{% highlight html linenos%}
{% raw %}
{% if site.wildfire.enable %}

  <script type="text/javascript">
    var wildfireConfig = () => ({
      {% if site.wildfire.useDev %}
      useDev: {{site.wildfire.useDev}},
      {% endif %}
      {% if site.wildfire.version %}
      version: '{{site.wildfire.version}}',
      {% endif %}
      databaseProvider: '{{site.wildfire.databaseProvider}}',
      databaseConfig: {
        {% if site.wildfire.databaseProvider == 'firebase' %}
        apiKey: '{{site.wildfire.firebase.apiKey}}',
        authDomain: '{{site.wildfire.firebase.authDomain}}',
        databaseURL: '{{site.wildfire.firebase.databaseURL}}',
        projectId: '{{site.wildfire.firebase.projectId}}',
        storageBucket: '{{site.wildfire.firebase.storageBucket}}',
        messagingSenderId: '{{site.wildfire.firebase.messagingSenderId}}'
        {% else %}
        siteId: '{{site.wildfire.wilddog.siteId}}'
        {% endif %}
      },
      pageURL: '{{ page.url | absolute_url }}',
      pageTitle: '{{ page.title| replace: "'", "\\'" }}',
      {% if site.wildfire.theme %}
      theme: '{{site.wildfire.theme}}',
      {% endif %}
      {% if site.wildfire.locale %}
      locale: '{{site.wildfire.locale}}',
      {% endif %}
      {% if site.wildfire.defaultAvatarURL %}
      defaultAvatarURL: '{{site.wildfire.defaultAvatarURL}}'
      {% endif %}
    });
  </script>
  {% if page.comments %}
    {% if site.wildfire.loaderVersion %}
    <script src="https://unpkg.com/wildfire-comment@{{site.wildfire.loaderVersion}}"></script>
    {% else %}
    <script src="https://unpkg.com/wildfire-comment"></script>
    {% endif %}
  {% endif %}

  <script src="https://unpkg.com/wf-count"></script>
{% endif %}
{% endraw %}
{% endhighlight %}

所有步骤到这里就结束了。

------

惊喜之后又失望的是，支持wildfire的两个平台中的firebase（谷歌的）在国内基本不能用（除非开vpn全局），另外一个wilddog现在已经不支持注册了（不知道以后会不会再次开放），哭泣....

所以，我又用回了gitalk。也罢，就当学习了，wildfire是个好项目，期待继续办下去，也希望wilddog野狗能开放注册，照顾下国内用户！哈哈