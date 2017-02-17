---
title: MacOS 配置 Docker 加速器
date: 2017-02-16 16:27:04
tags: docker, docker pull, docker hub, daocloud
category: docker
toc: true
---

使用 Docker 的时候，需要经常从官方获取镜像，但是由于显而易见的网络原因，拉取镜像的过程非常耗时，严重影响使用 Docker 的体验。DaoCloud 推出了加速器工具解决这个难题，通过智能路由和缓存机制，极大提升了国内网络访问 Docker Hub 的速度，目前已经拥有了广泛的用户群体，并得到了 Docker 官方的大力推荐。如果您是在国内的网络环境使用 Docker，那么 Docker 加速器一定能帮助到您。

# 加速器配置过程

1. 登录 [https://www.daocloud.io/](https://www.daocloud.io/)，注册一个账号
2. 进入控制台，选择加速器，复制 *http://xxx.m.daocloud.io*，注意 xxx 为自己注册之后 daocloud 给你分配的
3. 右键点击桌面顶栏的 docker 图标，选择 Preferences，选择 Daemon tab 下的 Basic，在 Insecure registries 中点击+号把 *http://xxx.m.daocloud.io* 贴进去
4. 点击 Apply & Restart 按钮使设置生效


# 我的 docker 环境


```
$ docker version
Client:
 Version:      1.13.1
 API version:  1.26
 Go version:   go1.7.5
 Git commit:   092cba3
 Built:        Wed Feb  8 08:47:51 2017
 OS/Arch:      darwin/amd64

Server:
 Version:      1.13.1
 API version:  1.26 (minimum version 1.12)
 Go version:   go1.7.5
 Git commit:   092cba3
 Built:        Wed Feb  8 08:47:51 2017
 OS/Arch:      linux/amd64
 Experimental: true
```