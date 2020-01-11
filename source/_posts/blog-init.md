---
title: DigitalOcean+Hexo+Nginx+Namecheap搭建个人博客
date: 2019-12-10 23:57:14
tags: [VPS,hexo,hginx,网站]
cover: /asset/create.jpg
---
强烈推荐[Github学生包](https://education.github.com/pack)，内含大量对学生的免费福利，包括不限于Jetbrain全家桶，AWS，Azure，DigitalOcean，Namecheap，name等。本文基于Github学生包里的DigitalOcean $50和Namecheap一年个人域名搭建个人博客。

## 技术架构

- VPS：[DigitalOcean](https://cloud.digitalocean.com/)
- 域名注册：[NameCheap](https://www.namecheap.com/)
- 博客框架：[Hexo](https://hexo.io/zh-cn/)
- 自动部署：[githook](https://git-scm.com/)
<!--more-->
## 前期准备

- 学生，或者有一个.edu后缀的邮箱
- 可以给国外付款的visa卡，或者PayPal（可使用银联的借记卡）
- $5用来激活账户

## Github学生认证

这一步网络上有大量教程，本文不再赘述。

参见：

- [注册Github并进行学生认证](https://blog.csdn.net/qq_40176716/article/details/84679999)
- [Github教程 学生认证](https://blog.csdn.net/qq_36667170/article/details/79084166)

## 注册Paypal

亲测中国银行借记卡(有union标志)可用。

参见：

- [注册申请PayPal支付账户](https://blog.csdn.net/love_bb/article/details/76064080)
- [PayPal注册绑卡使用教程](https://blog.csdn.net/PecoVio/article/details/82708048)

## 注册DigitalOcean

这一步也很简单，参见网上教程，只是最近注册完之后增加了一步verify，需要实名认证。processing的过程有点慢，我的认证13个小时才给我成功，如果卡在processing不用急，睡一觉就好了。

参见：

- [在GitHub Students Developer Pack申请DigitalOcean的50刀优惠码](https://blog.csdn.net/hunzhangzui9837/article/details/84974624)
- [从领取Github教育礼包到DigitalOcean购买服务器](https://www.jianshu.com/p/c5e7721d886c?tdsourcetag=s_pctim_aiomsg)

## 申请一个服务器

新建一个实例（droplets）,系统选择ubuntu（centos也可），standard（标准型，我们用来搭建个人博客足够了）：

![create-droplets](/asset/create-droplets.png)

价格选择最便宜的，这样可以用接近一年

![prize](/asset/prize.png)

重点来了！！！

服务器既然在国外，那速度肯定是首要考虑的。所以在选择服务器所在地区的时候，首先我们可以在官网测一下到达每个地方的速度，选择最快的地方搭建我们的服务器。在这里我选择了Frankfurt：

![region](/asset/region.png)

下面是一些常规选项，IPV6看个人需求可要可不要，其他有些是付费的，没需求就不用改

![others](/asset/others.png)

最后点击create droplet等待30s即创建好第一个服务器，随后服务器IP，Root，密码会发到你的邮箱里。

![final](/asset/final.png)

## 本地配置hexo

怎么安装，怎么使用，怎么用markdown写作，怎么部署到远程VPS服务器，在[下一篇博客](http://peizhengyijiaqin.me/2019/12/11/writing/)会讲。

## 部署Hexo到远程VPS服务器

putty输入服务器IP和密码远程连接，在第一次登录时由于DigitalOcean的安全策略会让你修改自己的登录密码。

具体过程参见：
[简书-VPS部署Hexo网站](https://www.jianshu.com/p/5cf20649f328)

现在，在浏览器输入 http://[yourIP] 就可以看到你的个人网站了！下一步我们通过设置域名来访问。

## 注册域名/域名解析

从Github学生包界面进入namecheap，挑选没有被别人占用的域名，确认后设置域名解析：
[Namecheap域名如何绑定IP](https://blog.csdn.net/SweetTool/article/details/87900507)

等待几分钟后，就可以通过你的.me域名进入网站了！