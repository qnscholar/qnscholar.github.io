---
title: GitHub Pages域名绑定及https支持的配置步骤
date: 2018-08-21 08-30-59
categories:
- 网站搭建
tags:
- 域名绑定
- https支持
typora-root-url: ../../iseex.github.io
---

补充说明：由于在微信端访问没有备案的域名受限，会弹出⚠️，非常影响体验。最新的政策规定域名备案需要实名制，而我的国外域名iseex.me很难在国内备案，因此我取消了域名绑定，还是用域名iseex.github.io访问博客，下方iseex.me的链接已无法访问，不过这不影响对本文的理解。另，我的github用户名从以前的iseexuhs换成了iseex，因此不要觉得截图有误。

--------------



GitHub pages提供绑定域名的功能（custom domain），在仓库的setting中可以设置，GitHub也提供了[帮助页面](https://help.github.com/articles/using-a-custom-domain-with-github-pages/)说明相关步骤和注意事项。一旦成功绑定自己的域名，就可以使用该域名来访问博客了，比如我绑定的域名是iseex.me，那么在浏览器中输入iseex.me就可以了。当然，输入GitHub Pages的原地址（username.github.io）会自动跳转到iseex.me。



虽然GitHub以及网上都有很多域名绑定的操作教程，但是自己操作起来发现还是会遇到一些问题，特别是https支持的配置。这也就是我写这篇博客原因，我希望我写的博客能解决你在网上难以查到答案的问题。

废话不多说，按照以下几个步骤来介绍。

- 域名申请
- DNS设置
- GitHub Pages域名绑定及https支持配置

### 域名申请

首先得申请个自己喜欢的域名，不建议在国内申请域名，因为要需要备案。在国际知名的域名供应商[Godaddy](https://www.godaddy.com/)上申请是个不错的选择，GoDaddy支持用支付宝付款，这点对中国用户比较友好。需要提一下，GitHub大法有个[GitHub Education](https://education.github.com/
)，对学生有教育优惠，如果申请成功，GitHub会送你一个教育礼包（pack），包括一年的namecheap（域名供应商）免费域名、Atom编辑器、Digital Ocean（主机）供应商的优惠券等福利。

![](/assets/images/posts/GitHub-Pages/github-education.jpg)

我这次就是申请的教育优惠，因此用的就是一年免费的namecheap域名，不过需要注意的是namecheap免费域名只限定为.me的域名，不含.com以及.io等，比如我的域名iseex.me一年免费，一年之后需要续费。申请教育优惠和namecheap域名不是今天要讲的内容，具体步骤可参考文章[我的 Github 个人博客是怎样炼成的](https://www.jianshu.com/p/4fd3cb0a11da)。

### DNS设置

DNS用于域名解析，即将主机空间和域名建立定向关系，是搭建网站非常重要的一个环节。一般来说，主机空间价格较贵，域名比较便宜（除非是那些非常好的域名）。之所以GitHub Pages这么受欢迎，原因之一便是GitHub Pages提供免费的主机空间。

DNSPod是主流的域名解析平台，不过这里用的是namecheap自带的域名解析服务。登陆namecheap，进入控制台，点击Domain List，可以查看到自己的域名，再点击 Manage，如下图。

![](/assets/images/posts/GitHub-Pages/namecheap-1.jpg)

进入下图，点击Advanced DNS，可以看到namecheap控制台已经自动为你添加了记录。其中两条A记录指向的ip地址是GitHub Pages提供的ip，www指定的记录是你在GitHub注册的仓库。

![](/assets/images/posts/GitHub-Pages/namecheap-2.jpg)

需要注意的是，为了https配置，上图中的ip是我修改过的。默认情况下namecheap指向的ip是：

- 192.30.252.153
- 192.30.252.154

虽然利用上述两个ip也能正常进行域名解析，网站也能正常打开，但是不支持https。https更加安全，越来越多的网站也加持了https，在Chrome中用http而非https的网站会提示不安全。

我在配置过程中，GitHub Pages的settings中就提示绑定的两个ip比较老，现在不能支持https，因此根据GitHub提供的[帮助文档](https://help.github.com/articles/troubleshooting-custom-domains/#https-errors)中的信息：

![](/assets/images/posts/GitHub-Pages/ip.jpg)

可以知道，支持https的ip地址必须指向以下ip其中一个。

- 185.199.108.153
- 185.199.109.153
- 185.199.110.153
- 185.199.111.153

如上图所示，我在namecheap控制台配置的就是其中两个。到此DNS的设置就完成了，如果是用DNSPod进行域名解析可以参考资料[如何搭建一个独立博客——简明Github Pages与Hexo教程](https://www.jianshu.com/p/141abf1700da)。

### GitHub Pages域名绑定及https支持配置

下面进行GitHub的设置，打开GitHub仓库的settings，在custom domain 中填上刚申请的域名（如果是用namecheap的域名，GitHub Pages会自动填充域名），勾选enforce https，使能https支持，如下图所示。

![](/assets/images/posts/GitHub-Pages/enforce-https.jpg)

按照GitHub Pages的[帮助文档](https://help.github.com/articles/using-a-custom-domain-with-github-pages/)，绑定域名需要在仓库中新建一个CNAME的文件，文件内容为绑定的域名（比如iseex.me），如下图所示。

![](/assets/images/posts/GitHub-Pages/cname.jpg)



不过第一次GitHub Pages也会自动建立好CNAME文件，不需要我们操作什么。

接下来很重要的一步，由于前面我们更新了ip地址，根据GitHub 提供的[帮助文档](https://help.github.com/articles/troubleshooting-custom-domains/)，我们需要删除CNAME并重新添加，以触发https支持，如下图所示。

![](/assets/images/posts/GitHub-Pages/cname-readd.jpg)

到这里看似该完成的都完成了，可是打开settings，发现还是有警告⚠️。接着，我根据GitHub Pages的[Help页面](https://help.github.com/articles/securing-your-github-pages-site-with-https/)提供的帮助，如下图。

![](/assets/images/posts/GitHub-Pages/url-setting.jpg)

大致意思是让html中的链接（src）都使用https的形式，因此我想到的解决办法是在Jekyll或者Hexo的配置文件.config.yml的url项写上带https的域名，如下所示。

![](/assets/images/posts/GitHub-Pages/url.jpg)

修改完push一下，再次到仓库的settings一看发现一切正常，如下图所示。

![](/assets/images/posts/GitHub-Pages/finish.jpg)

在Chrome中打开网站[iseex.me](https://iseex.me)，也显示安全，如下图。

![](/assets/images/posts/GitHub-Pages/site-https.jpg)

> 大功告成，如果有疑问🤔️欢迎在下方留言。