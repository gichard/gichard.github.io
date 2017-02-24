---
layout: post
title:  "博客搭建流程"
date:   2017-02-24 12:55:27 +0800
categories: log
---

一直以来都想建立一个博客，但一拖再拖，现在我终于用jekyll和GitHub Pages搭起了自己的博客。
现在对大概的流程做一个记录，虽然不太会有人来看...

搭建流程主要参考了[使用 Jekyll 和 Github Pages 搭建博客](http://helldwellercn.github.io/20150910/jekyll/)这篇文章

## 步骤一：安装Ruby
前往[Ruby的官网](http://rubyinstaller.org/downloads/)下载Ruby和Ruby DevKit安装包.
然后安装Ruby，记得 勾上“Add Ruby executables to your PATH” 以省去配置环境变量。然后
解压Ruby DevKit,在CMD中cd到该目录，执行
{% highlight ruby %}
ruby dk.rb init
ruby dk.rb install
{% endhighlight %}

## 步骤二：安装Jekyll
执行
{% highlight ruby %}
gem install jekyll
{% endhighlight %}
可能需要更换安装源，但我并没有遇到这样的问题
更换方式如下：
{% highlight ruby %}
gem sources --remove https://rubygems.org/
gem sources -a https://ruby.taobao.org/
gem sources -l
{% endhighlight %}
这样可以换成淘宝的源。

## 步骤三：用Jekyll建立博客
先在合适的位置建立一个文件夹，如My_Blog然后cd进入。执行
{% highlight ruby %}
jekyll new blog-name
{% endhighlight %}
blog-name是自己随意起的名字。执行后会出现一个blog-name的文件夹,cd进入后运行
{% highlight ruby %}
jekyll serve
{% endhighlight %}
现在就可以用浏览器打开 http://localhost:4000/ 以查看[自己的博客](http://localhost:4000/)

## 步骤四：将本地的博客上传到GitHub
这一步可以按照[GitHub Pages的官网](https://pages.github.com/)按照步骤操作。

## 后记
现在终于搭建好了博客，那么应该怎样修改网页或发文章呢？要改变网页的title和about等信息可以
修改blog-name下的_config.yml和about.md。发表的文章应当用markdown写，然后放在_posts目录下。
写好文章后最好先在本地确认好后，再提交到GitHub上。关于Git和GitHub的使用，可以参考Udacity的课程[如何使用Git和GitHub](https://cn.udacity.com/courses/all)
