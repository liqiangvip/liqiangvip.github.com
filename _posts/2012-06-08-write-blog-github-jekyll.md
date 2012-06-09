---
layout: post
title: "随笔：技术流可以这样写博客"
description: ""
category: 
tags: [blog, github, jekyll]
---
{% include JB/setup %}

在知道Git之后，对它了解越多就越觉得它功能强大。

今天又发现了一件有趣的玩具，就是用GitHub+Jekyll来搭建博客站点，这绝对是我这种技术宅男的最爱，my type :)

##技术路线
1. 使用[Markdown](http://en.wikipedia.org/wiki/Markdown)来写博文。Markdown是一种轻量级的标记语言，可以直接生成HTML，很多人都使用它来写博文，也得到wordpress之类的支持。
2. 使用Jekyll搭建博客站点。Jekyll是一个Blog生成工具，通常被用来生成静态网页，并且借助GitHub的托管功能，就成为一个免费的博客站点了哈。
3. 使用GitHub来存储所有的数据。这点就不必多说了，数据放在上面也不怕丢了，同时广大免费的代码仓库也提供了大量优秀的博客站点及主题模板等资源。

##具体步骤
本实验环境为：windows上搭建Jekyll测试平台，为了方便，使用[pizn](https://github.com/pizn/pizn.github.com)的仓库代码

1. 先注册申请一个[GitHub](https://github.com/)账号
2. 按照[官方教程](https://help.github.com/articles/set-up-git)在本地配置好Git环境下载安装Git工具。其实就是以下几步:
> a. 在[此处](http://git-scm.com/downloads)下载安装最新版本的Git。国内如果访问有困难，可以去[google code](http://code.google.com/p/gitextensions/downloads/list)下载。  
> b. 使用`git config --global user.name "Your Name Here"`设置用来标识你身份的提交用户名  
> c. 使用`git config --global user.email "your_email@youremail.com"`设置用来标识你的地址信息（此处并不需要是真实的邮件地址）

3. Windows平台的用户，可以此处下载安装[GitHub](http://windows.github.com/)的客户端，用它可以很方便的管理你的代码仓库。为了更方便的使用GitHub，它还会要求你去下载一个微软的PowerShell程序。
4. 下面我们先使用piz的blog仓库，打开[页面](https://github.com/liqiangvip/pizn.github.com "pizn.github.com")，点击右上角的"Fork"按钮，就会在你的仓库那生成一条支线仓库，然后你的仓库中就多了一个pizn.github.com的仓库，点击其页面上的Clone in Windows按钮，就会调用你之前安装好的GitHub客户端，将该仓库的代码下载到本地。默认位置是我的文档下的GitHub文件夹内。
5. 至此，我们已经拥有了一个作为博客站点的示例代码，下面就需要在本地搭建Jekyll测试平台。
6. 下载最新的[RubyInstaller](http://rubyforge.org/frs/?group_id=167)并安装，然后在命令行终端下输入`gem update --system`来升级gem
7. 下载最新的[DevKit](https://github.com/oneclick/rubyinstaller/downloads/)并双击运行解压到C:\DevKit。然后打开终端cmd，输入下列命令进行安装：  
	cd C:\DevKit  
	ruby dk.rb init  
	ruby dk.rb install
8. 然后就可以使用下列命令安装Jekyll了：  
	gem install jekyll  
并使用`jekyll --version`检验是否安装成功
9. 一般而言，还可以安装Rdiscount，这个用来解析Markdown标记的包，使用如下命令：  
	gem install rdiscount
10. 现在，所有的工作都完成了，让我们在本地测试看看下载得到的pizn博客站点是否可以成长运行。
11. 打开终端命令行，进入到你clone得到的pizn.github.com目录下，运行以下命令：  
	jekyll --server  
12. 打开浏览器，输入 http://127.0.0.1:4000 进行访问。
13. 如果出现问题的话，请参考[《Jekyll 本地调试之若干问题》](http://chxt6896.github.com/blog/2012/02/13/blog-jekyll-native.html)。比如本人就遇到过其中的Problem3.