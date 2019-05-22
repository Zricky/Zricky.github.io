---
title: 利用git博客备份（换电脑等）
subtitle: 创建分支保存博客 
description: 博客备份 以及换电脑编辑 博文
tags:
  - git
  - hexo
categories:
  - git
  - blog
date: 2019-05-17 14:10:01
updated: 2019-05-17 14:10:01
summary_img: https://avatars0.githubusercontent.com/u/29839337
keywords:
author:
---
<!--more-->
# 1 建立分支hexo
* 1 克隆到本地 
> git clone git@github.com:yourname/yourname.github.io.git
* 2 删除yourname.github.io目录下.git之外的所有文件
* 3 把blog下.git之外的所有文件复制到yourname.github.io目录下
* 4 删除主题目录下通过git clone的目录下.git目录
* 5 创建分支 hexo
> git checkout -b hexo
* 6 添加所有文件到暂存区
> git add --all
* 7 进行提交
> git commit -m "博客备份"
* 8 推送hexo分支的文件到github仓库
> git push --set-upstream origin hexo

# 2 博客更新
~~~sh
    git add . #添加所有文件到暂存区
    git commit -m "提交一篇博客"  #提交
    git push origin hexo 推送hexo分支到github
~~~

> git remote add origin git@github.com:yourname/yourname.github.io.git

# 3 新电脑写blog
~~~
    git clone -b hexo git@github.com:yourname/yourname.github.io.git
    cd yourname.github.io
    npm install
~~~
