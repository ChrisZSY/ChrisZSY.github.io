---
title: hexo搭建教程
date: 2021-02-08 22:05:11
categories: blog
author: ChrisZSY
tags:
	- github
	- hexo
---

### Hexo简介  

Hexo是一款基于Node.js的静态博客框架，依赖少易于安装使用，可以方便的生成静态网页托管在GitHub和Coding上，是搭建博客的首选框架。大家可以进入 [hexo官网](https://hexo.io/zh-cn/) 进行详细查看，因为Hexo的创建者是台湾人，对中文的支持很友好，可以选择中文进行查看。
<!--more-->
教程分三个部分  
* 第一部分：hexo的初级搭建还有部署到github page上，以及个人域名的绑定。
* 第二部分：hexo的基本配置，更换主题，实现多终端工作，以及在coding page部署实现国内外分流。
* 第三部分：hexo添加各种功能，包括搜索的SEO，阅读量统计，访问量统计和评论系统等。

### 第一部分  
   hexo的初级搭建还有部署到github page上，以及个人域名的绑定。

#### Hexo简介

Hexo是一款基于Node.js的静态博客框架，依赖少易于安装使用，可以方便的生成静态网页托管在GitHub和Coding上，是搭建博客的首选框架。大家可以进入hexo官网进行详细查看，因为Hexo的创建者是台湾人，对中文的支持很友好，可以选择中文进行查看。

#### Hexo搭建步骤

* 安装Git
* 安装Node.js
* 安装Hexo
* GitHub创建个人仓库
* 生成SSH添加到GitHub
* 将hexo部署到GitHub
* 设置个人域名
* 发布文章

#### 1. 安装Git

Git是目前世界上最先进的分布式版本控制系统，可以有效、高速的处理从很小到非常大的项目版本管理。也就是用来管理你的hexo博客文章，上传到GitHub的工具。Git非常强大，我觉得建议每个人都去了解一下。廖雪峰老师的Git教程写的非常好，大家可以了解一下。[Git教程](https://www.liaoxuefeng.com/wiki/896043488029600)  
windows：到git官网上下载,Download git,下载后会有一个Git Bash的命令行工具，以后就用这个工具来使用git。

linux：对linux来说实在是太简单了，因为最早的git就是在linux上编写的，只需要一行代码  

```bash
sudo apt-get install git
```
安装好后，用`git --version` 来查看一下版本

#### 2. 安装nodejs

Hexo是基于nodeJS编写的，所以需要安装一下nodeJs和里面的npm工具。

windows：nodejs选择LTS版本就行了。

linux：
```bash
sudo apt-get install nodejs
sudo apt-get install npm
```

```bash
node -v
npm -v
```

检查一下有没有安装成功

顺便说一下，windows在git安装完后，就可以直接使用git bash来敲命令行了，不用自带的cmd，cmd有点难用。
#### 3. 安装hexo

前面git和nodejs安装好后，就可以安装hexo了，你可以先创建一个文件夹blog，然后cd到这个文件夹下（或者在这个文件夹下直接右键git bash打开）。

输入命令  
```bash
npm install -g hexo-cli
```

依旧用`hexo -v`查看一下版本

至此就全部安装完了。

接下来初始化一下hexo  
```bash
hexo init myblog
```
这个myblog可以自己取什么名字都行，然后  
```bash
cd myblog //进入这个myblog文件夹
npm install
```

新建完成后，指定文件夹目录下有：

* node_modules: 依赖包
* public：存放生成的页面
* scaffolds：生成文章的一些模板
* source：用来存放你的文章
* themes：主题
* ** _config.yml: 博客的配置文件**  

打开hexo的服务，在浏览器输入localhost:4000就可以看到你生成的博客了。

大概长这样：  
```bash
$ hexo g
INFO  Validating config
[camaro] worker_threads is not available, expect performance drop. Try using Node version >= 12.
INFO  Start processing
INFO  Files loaded in 624 ms
INFO  Generated: 2021/02/08/hexo搭建教程/index.html
INFO  Generated: search.xml
INFO  2 files generated in 421 ms
$ hexo server
INFO  Validating config
[camaro] worker_threads is not available, expect performance drop. Try using Node version >= 12.
INFO  Start processing
INFO  Hexo is running at http://localhost:4000 . Press Ctrl+C to stop.
```





使用ctrl+c可以把服务关掉。  
