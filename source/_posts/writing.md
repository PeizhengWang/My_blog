---
title: Hexo+markdown开始博客写作
date: 2019-12-11 22:17:30
tags: [hexo,markdown,写作,网站]
---
## 目录

- Hexo安装
- Hexo使用
- Markdown写作
<!--more-->

## Hexo安装

引用[Hexo官方文档](https://hexo.io/zh-cn/docs/)：

> **什么是 Hexo?**
Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

> **安装** 
安装 Hexo 只需几分钟时间，若您在安装过程中遇到问题或无法找到解决方式，请提交问题，我们会尽力解决您的问题。

> **安装前提**
安装 Hexo 相当简单，只需要先安装下列应用程序即可：
Node.js (Node.js 版本需不低于 8.10，建议使用 Node.js 10.0 及以上版本)
Git
>
>如果您的电脑中已经安装上述必备程序，那么恭喜您！你可以直接前往 安装 Hexo 步骤。
如果您的电脑中尚未安装所需要的程序，请根据以下安装指示完成安装。

> **安装 Git**
>- Windows：下载并安装 git.
>- Mac：使用 Homebrew, MacPorts 或者下载 安装程序。
>- Linux (Ubuntu, Debian)：sudo apt-get install git-core
>- Linux (Fedora, Red Hat, CentOS)：sudo yum install git-core

> **安装 Node.js**
Node.js 为大多数平台提供了官方的 [安装程序](https://nodejs.org/en/download/)。对于中国大陆地区用户，可以前往 [淘宝 Node.js 镜像](https://npm.taobao.org/mirrors/node) 下载。
>
>其它的安装方法：
>
>- Windows：通过 nvs（推荐）或者nvm 安装。
>- Mac：使用 Homebrew 或 MacPorts 安装。
>- Linux（DEB/RPM-based）：从 NodeSource 安装。
>
>其它：使用相应的软件包管理器进行安装，可以参考由 Node.js 提供的 指导
对于 Mac 和 Linux 同样建议使用 nvs 或者 nvm，以避免可能会出现的权限问题。

这里需要用到刚才安装的git，在git bush里进行如下操作：
> **安装 Hexo**
所有必备的应用程序安装完成后，即可使用 npm 安装 Hexo。
>
>$ npm install -g hexo-cli

这样，Hexo就成功安装好了，下一步就可以着手在本地搭建自己的博客了。

## Hexo使用

**如果你已经有了一个建好的网站**，并且已经上传到了github，可将网站代码克隆到本地。

在选定的文件夹下：

```
$ git clone git@github.com:heros979/My_blog.git
```
clone后面是你的github代码库的地址，示例是我的，你们要改成你们自己的。

**如果你是第一次建立自己的网站**，在你想要的（随意哪个都行）文件夹里右键进入git bush，输入：
```
$ hexo init <folder>
$ cd <folder>
$ npm install
```
其中folder是你存放代码的文件夹名字

好了，我们的文件夹里有了很多新的文件,如下：
```
.
├── _config.yml
├── package.json
├── scaffolds
├── source
|   ├── _drafts
|   └── _posts
└── themes
```

其中 _config.yml 是网站的[配置](https://hexo.io/zh-cn/docs/configuration)信息，您可以在此配置大部分的参数。  
如果是第一次建立的话，要在deploy处加入自己的github地址。例如我的：

![deploy](/asset/deploy.png)

我们要写的博客就放在 _post 文件夹里。在根目录可以使用如下方式新建post
```
hexo new <post-name>
```

我们在写完post后在根目录输入：
```
hexo clean
hexo g
hexo d
```

即可将我们的网站部署到VPS服务器和我们的github上。

## Markdown写作

打开我们刚才建立的post-name.md文件，我们要用markdown的语法来写这个页面，markdown是一个很简单的写作工具，也很好看，很实用。

例子1：
```
*开辟鸿蒙，谁为情种？*                  #这是斜体
**都只为风月情浓。**                    #这是加粗
***奈何天，伤怀日，***                  #这是斜体加粗
<font size=4>寂寥时，试遣愚衷。</font>  #自定义字体大小
~~因此上，演出这~~                      #这是删除线
> 怀金悼玉的《红楼梦》。                 # 这是引用
```

*开辟鸿蒙，谁为情种？*
**都只为风月情浓。**
***奈何天，伤怀日，***
<font size=4>寂寥时，试遣愚衷。</font> 
~~因此上，演出这~~
> 怀金悼玉的《红楼梦》。

例子2：

```
## CALLED BACK  #这是标题，几个#就是几级标题

<font face="微软雅黑" size=6 color=#FF0000 >Just lost when I was saved!</font>  #修改字体字号颜色
<table><tr><td bgcolor=orange>Just felt the world go by!</td></tr></table>     #修改背景色
Just girt me for the onset with eternity,
When breath blew back,
And on the other side
I heard recede the disappointed tide!

Therefore, as one returned, I feel,
Odd secrets of the line to tell!
Some sailor, skirting foreign shores,
Some pale reporter from the awful doors 
Before the seal!

Next time, to stay!
Next time, the things to see
By ear unheard,
Unscrutinized by eye.

Next time, to tarry,
While the ages steal,—
Slow tramp the centuries,
And the cycles wheel.
```

# CALLED BACK

<font face="微软雅黑" size=6 color=#FF0000 >Just lost when I was saved!</font>
<table><tr><td bgcolor=orange>Just felt the world go by!</td></tr></table>
Just girt me for the onset with eternity,
When breath blew back,
And on the other side
I heard recede the disappointed tide!

Therefore, as one returned, I feel,
Odd secrets of the line to tell!
Some sailor, skirting foreign shores,
Some pale reporter from the awful doors 
Before the seal!

Next time, to stay!
Next time, the things to see
By ear unheard,
Unscrutinized by eye.

Next time, to tarry,
While the ages steal,—
Slow tramp the centuries,
And the cycles wheel.

更多语法，比如标题、换行、注释、分割线、引用、代码块、列表、链接、表格、图片、流程图、LaTeX。

参见：[Markdown快速入门](https://sspai.com/post/45816)，[Markdown语法(字体,样式,公式,背景,图表等)](https://blog.csdn.net/woswod/article/details/82753451)