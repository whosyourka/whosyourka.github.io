---
title: 安装hexo
date: 2019-01-17 16:48:32
categories:
- hexo
tags: 
- hexo


---

# 本文为本博客的快速部署方案，详细问题请参考[官方文档](https://hexo.io/zh-cn/docs/)   

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

# 主题Next功能（下面功能都可以再[官网](https://theme-next.iissnan.com/)获取）

首先先集成主题：[最新主题](https://github.com/iissnan/hexo-theme-next) 下载完放theme文件目录，并修改\_config.yml里面的theme标签，接下来就可以开心的集成其他功能了。ps：下面的\_config.yml为主题目录下的,跟前面的不一样

## 主题设定

设置RSS，tags，categories，去掉动画，google分析，百度统计，[阅读量统计](http://www.jeyzhang.com/hexo-next-add-post-views.html)，自动截断

本地字数统计修改：修改themes/(主题名) 的_config.yml文件，找到post_wordcount下面的wordcount为true

后续集成：[社交](https://github.com/revir/need-more-share2)，打赏，订阅微信公众号  

## 第三方服务集成[请参考官方NexT](http://theme-next.iissnan.com/third-party-services.html)

**搜索功能：**我用的是local search，安装`npm install hexo-generator-search --save`，修改themes/(主题名) 的_config.yml文件,改成true

``` local_search:
local_search:
  enable: true
```

**[评论功能](https://chad-it.github.io/2018/06/14/Hexo%E9%9B%86%E6%88%90Gitment%E8%AF%84%E8%AE%BA%E7%B3%BB%E7%BB%9F/)：**

1.使用gitment，修改themes/(主题名) 的_config.yml文件，找到gitment标签，修改下面对应的数据（先注册个[OAuth](https://github.com/settings/applications/new)）

```
gitment:
  enable: true
  github_user: # MUST HAVE, Your Github ID
  github_repo: # MUST HAVE, The repo you use to store Gitment comments
  client_id: # MUST HAVE, Github client id for the Gitment
  client_secret: # EITHER this or proxy_gateway, Github access secret
```

2.使用valine，修改themes/(主题名) 的_config.yml文件，修改enable，appid，appkey即可（appid和appkey需要申请leancloud），这种不需要登录可评论