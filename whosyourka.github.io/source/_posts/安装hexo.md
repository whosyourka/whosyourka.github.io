---
title: 安装hexo
date: 2019-01-17 16:48:32
tags:
---

# 本文为快速部署，详细问题请参考[官方文档](https://hexo.io/zh-cn/docs/)   

# 安装插件：

## linux: 

安装git nodejs npm：

```
sudo apt install git
sudo apt install nodejs
sudo apt install npm
```

直接安装hexo：

```
npm install -g hexo-cli
npm install hexo-deployer-git --save（hexo的git插件，后续需要用）
```

## windows：

nodejs和npm：https://nodejs.org/en/

git：https://git-scm.com/download/win

配置完环境变量后直接安装hexo：

```
npm install -g hexo-cli
npm install hexo-deployer-git --save（hexo的git插件，后续需要用）
```

# hexo 初始化

```
hexo init xxxxxxxxxxx（github名称）.github.io     //如果要传到github
cd xxxxxxxxxxx（github名称）.github.io
npm install
hexo g
hexo s 
```

本地效果：locolhost:4000

# 上传git

github新建一个项目，名称：用户名.github.io

然后在本地目录里面配置_config.yml:

```
deploy:
	type: git
	repository: https://github.com/xxxxx/xxxxx.github.io.git
	branch: master
```

生成至public目录： 

```
hexo g
```

然后上传命令：

```
hexo d   
```

# 多台电脑共用

首先把源代码(xxxxxxxxxxx（github名称）.github.io)保存到远程仓库（github都可以），然后每次hexo d发布后，再提交到远程仓库。

其他电脑使用：先安装git nodejs npm hexo，然后获取到源代码，就（xxxxxxxxxxx（github名称）.github.io目录下）可以直接用hexo g和hexo s本地生成了 ，想用hexo d，还是要安装（npm install hexo-deployer-git --save）

# 其他功能

## 个人主要功能

**评论功能：**http://theme-next.iissnan.com/third-party-services.html

**归档，分类，标签，索引功能：已默认安装**

**搜索功能：**

**主题：**[最新主题](https://github.com/iissnan/hexo-theme-next) 下载完放theme文件目录，并修改_config.yml里面的theme标签



## 其他可能用到的插件命令(已经安装查看package.json)

- 本地搜索: `npm install hexo-generator-search --save`
- 置顶功能：`npm install hexo-helper-post-top --save`
- Latex语法支持： `npm install hexo-math --save`