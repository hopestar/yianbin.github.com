---
layout: post
title: 像黑客一样写博客
---

我一直在寻求一种写博客的最佳体验，就在一个月前，我了解到如何在Github上建博客，便打算使用Jekyll来重新设计我的博客。而今天，这个博客终于可以问世了。

## 创建Github项目 ##

首先，我创建了一个名字如下的项目，并初始化：

    ~ mkdir yianbin.github.com
    ~ git init

## 安装Jekyll ##

我是在Cygwin上安装的，首先确定Cygwin环境中有Ruby，然后执行下面的代码：

    gem sources -a http://ruby.taobao.org/
    gem install jekyll
    gem install rdiscount

## 编写Blog模版代码 ##

Jekyll要求的站点目录应该是下面的样子：

    .
    |-- _config.yml
    |-- _layouts
    |   |-- default.html
    |   `-- post.html
    |-- _posts
    |   `--2012-09-14-blogging-like-a-hacker.md
    |-- _site
    `-- index.html

在Github项目中创建像上面一样的站点目录，然后通过下面命令，就可以在本地预览Blog了。

    jekyll --server


## 发布 ##

    git add --all
    git commit -m "The First Commit"
    git remote add origin git@github.com:yianbin/yianbin.github.com
    git push origin master

稍等片刻，就可以查看到Blog了。
