---
title: GitHub Pages域名绑定及https支持的配置步骤
date: 2018-08-21 08-30-59
categories:
- 网站搭建
tags:
- 域名绑定
- https支持
typora-root-url: ../../iseexuhs.github.io
---

GitHub pages提供绑定域名的功能（custom domain），在仓库的setting中可以设置，GitHub也提供了[帮助页面](https://help.github.com/articles/using-a-custom-domain-with-github-pages/)说明相关步骤和注意事项。一旦成功绑定自己的域名，就可以使用该域名来访问博客了，比如我绑定的域名是iseex.me，那么在浏览器中输入iseex.me就可以了。当然，输入GitHub pages的原地址（username.github.io）会自动跳转到iseex.me。



虽然GitHub以及网上都有很多域名绑定的操作教程，但是自己操作起来发现还是会遇到一些问题，特别是https支持的配置。这也就是我写这篇博客原因，我希望我写的博客能解决你在网上难以查到答案的问题。

废话不多说，按照以下几个步骤来介绍。

- 域名申请
- DNS设置
- GitHub Pages域名绑定及https支持配置

### 域名申请

首先得申请个自己喜欢的域名，在知名的国际域名供应商[Godaddy](https://www.godaddy.com/)上申请是个不错的选择，GoDaddy支持用支付宝付款，这点对中国用户比较友好。不过GitHub大法有个[GitHub Education](https://education.github.com/
)，对学生有教育优惠，如果申请成功，GitHub会送你一个教育礼包（pack），包括一年的CNAME（域名供应商）免费域名、Atom编辑器、Digital Ocean（主机）供应商的优惠券等福利。

![github-education](/assets/images/posts/GitHub-Pages/github-education.jpg)

我这次就是申请的教育优惠，因此用的就是一年的CNAME域名，不过需要注意的是CNAME免费域名只包含.me，不含.com以及.io等，比如我的域名iseex.me。申请教育优惠和CNAME域名不是今天的内容，具体步骤可参考文章[我的 Github 个人博客是怎样炼成的](https://www.jianshu.com/p/4fd3cb0a11da)。



