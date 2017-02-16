---
title: 在github上使用hexo搭建博客
date: 2017-02-04
category: hexo
toc: true
---

Hexo是一个简单地、轻量地、基于Node的一个静态博客框架，可以方便的生成静态网页托管在github和Heroku上。引用Hexo作者 @tommy351 的话：

快速、简单且功能强大的Node.js博客框架。A fast, simple & powerful blog framework, powered by Node.js.

要使用Hexo，需要在你的系统中支持Nodejs和Git。


## 安装git客户端

根据自己的系统选择合适的git客户端进行安装。
官网：[https://git-scm.com/](https://git-scm.com/)

## 安装Nodejs
官网：[https://nodejs.org/en/](https://nodejs.org/en/)

## 使用Hexo
官网：[https://nodejs.org/en/](https://nodejs.org/en/)

### 安装hexo

```
mkdir hexo
cd hexo
npm install hexo-cli -g
```

### 初始化hexo

```
hexo init
```

### 安装依赖

```
npm install
```

### 启动hexo

```
hexo server
```

启动之后，打开浏览器，在地址栏输入：http://localhost:4000，你会看到Hexo的示例页面。

## Hexo命令

```
hexo new <title>
// 新建文章 此时在source_posts文件夹中便会多出一个文档"title.md".
// 如果要删除，直接在此文件夹下删除对应的文件即可

hexo generate  // 生成静态页面，生成的静态内容在public文件夹内。
hexo clean     // 清除生成内容，执行此操作会删除public文件夹中的内容。 
hexo deploy    // 该操作会将hexo生成的静态内容部署到配置的仓库中
hexo server    // 启动hexo

npm install hexo-deployer-git --save  // 安装git插件，如果没有安装git插件，会有错误提示，安装后重新部署就可以了。

//  hexo命令缩写
hexo g：hexo generate
hexo c：hexo clean
hexo s：hexo server
hexo d：hexo deploy

//  hexo命令组合
hexo clean && hexo g -s，就是清除、生成、启动
hexo clean && hexo g -d，就是清除、生成、部署
```

## 参考文档

1. [手把手教从零开始在GitHub上使用Hexo搭建博客教程(一)-附GitHub注册及配置](http://www.jianshu.com/p/f4cc5866946b)
2. [手把手教你使用Hexo + Github Pages搭建个人独立博客](http://jiji262.github.io/2016/04/15/2016-04-15-hexo-github-pages-blog/)


