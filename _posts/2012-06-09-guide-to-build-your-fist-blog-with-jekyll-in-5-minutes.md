---
layout: post
title: "Guide to build your fist Blog with Jekyll in 5 minutes"
description: ""
category: 
tags: [blog, jekyll, guide]
---
{% include JB/setup %}

上次介绍了技术流可以怎样利用GitHub以及Jekyll来搭建博客，过程看着有点长了，囧~

今天给大家带来快速搭建方法，主要原理是借助[Jekyll-Bootstrap](http://jekyllbootstrap.com/)直接clone一个给自己，然后就可以用了:)
可以打开上面那个链接，按照它的详细讲解步骤，就可以搭建好了。下面我也简单的总结下吧：

1. 你首先需要有一个GitHub账号（假设你的ID为USERNAME），然后新建一个名为“user_name.github.com”的repo
2. 本地需要已经装好Git或者GitHub的程序，然后在终端下输入下列代码安装Jekyll-Boostrap:  
`git clone https://github.com/plusjade/jekyll-bootstrap.git USERNAME.github.com`  
`cd USERNAME.github.com`  
`git remote set-url origin git@github.com:USERNAME/USERNAME.github.com.git`  
`git push origin master`
3. 到此为止，不必惊讶，你已经拥有了一个博客站点，就在 http://USERNAME.github.com （由于后台生成页面需要点时间，可以稍等会儿哈）

##关于本地测试运行
为了本地查看，你需要另行安装jekyll（详情请前一篇博文），你可以打开终端，进入到你clone的这个repo目录下，然后运行`jekyll --server`，然后打开浏览器访问 http://127.0.0.1:4000 查看页面。

接下来可以使用命令创建博文，还有其他一些快速上手教程，可以参看[此文](http://jekyllbootstrap.com/usage/jekyll-quick-start.html)

##关于主题的使用
上面使用的repo自带了一个twitter主题，你也可以切换使用Jekyll-Bootstrap设计的几个主题，请看[教程](http://jekyllbootstrap.com/usage/jekyll-theming.html)
