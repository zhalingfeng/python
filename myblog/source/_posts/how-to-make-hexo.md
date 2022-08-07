---
title: how to make hexo
date: 2022-07-15 21:52:57
tags:
---
## 1 安装git
### 到git官网下载
[官网](https://git-scm.com/)       
## 2 安装node.js
### 到 node.js下载
[官网](https://nodejs.org/en/)
## 3 安装hexo
### 1.可以先创建一个文件夹，然后右键这个文件夹 （点击git bash)
### 2.输入指令 `npm install -g hexo-cli`
### 3.初始化一下hexo （`hexo init myblog`）这个myblog输什么名字都可以
### 4.然后`cd myblog` 进入这个myblog文件夹npm install
### 5.输入`hexo g` 和 `hexo server`，浏览器输入localhost:4000就可以看到你的博客了
## 4 创建GitHub 个人仓库  
### 首先先创建一个属与你的GitHub账户，然后注册完登录后，在http://GitHub.com中看到一个New repository，创建一个和你用户名相同的仓库，后面加 .http://github.io   
## 5 把ssh加入到GitHub 
### 1.回到git bash, 输入 (`git config --global user.name "yourname"`）和（`git config --global user.email "youremail"`）
yourname 代表你GitHub的用户名
youremail代表你GitHub注册时输入的邮箱 （可以输入以下两条检查是否输对） 
### `git config user.name`
### `git config user.email`
### 2.然后创建SSH.输入（`ssh-keygen -t rsa -C "youremail"`） 在你的电脑中找到这个文件夹   
## 6 将hexo部署到GitHub
### 1.打开文件 _config.yml，翻到最后，修改为 YourgithubName就是你的GitHub账户
deploy:

type: git

repo: https://github.com/YourgithubName/YourgithubName.github.io.git

branch: master
### 2.然后输入以下三条
`hexo clean`

`hexo generate`

`hexo deploy`   
### 3.点开[网址](http://yourname.github.io)后就可以看到你的博客了

