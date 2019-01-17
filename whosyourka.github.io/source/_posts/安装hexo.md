---
title: 安装hexo
date: 2019-01-17 16:48:32
tags:
---

[TOC]

# 安装插件：

## linux: 

安装git nodejs npm：

```
sudo apt install git
sudo apt install nodejs
sudo apt install npm
```

安装最新的管理插件

```
npm install -g hexo-cli
npm install hexo-deployer-git --save（hexo的git插件，后续需要用）
```

## windows：

nodejs：https://nodejs.org/en/

git：https://git-scm.com/download/win

配置完环境变量后直接安装hexo：

```
npm install -g hexo-cli
npm install hexo-deployer-git --save（hexo的git插件，后续需要用）
```

# hexo 初始化

```
hexo init xxxxxxxxxxx（github名称）.github.io     //如果要传到github
hexo g
hexo s 
```

本地效果，命令查看hexo help



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



# 其他功能

## 主要功能

**评论功能：**http://theme-next.iissnan.com/third-party-services.html

**归档，分类，标签，索引功能：**

**搜索功能：**

**主题：**



## 其他插件命令

- 索引生成器：`npm install hexo-generator-index --save`

- 归档生成器：`npm install hexo-generator-archive --save`

- 分类生成器：`npm install hexo-generator-category --save`

- 标签生成器：`npm install hexo-generator-tag --save`

- 本地搜索: `npm install hexo-generator-search --save`

- 本地化服务：`npm install hexo-server --save`

- Git部署功能：`npm install hexo-deployer-git --save`

- 渲染器：`npm install hexo-renderer-marked --save`

- 渲染器：`npm install hexo-renderer-stylus --save`

- 置顶功能：`npm install hexo-helper-post-top --save`

- Latex语法支持： `npm install hexo-math --save`