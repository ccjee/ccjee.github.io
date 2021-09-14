---
weight: 1
title: "GitHub部署"
date: 2019-12-01T21:57:40+08:00
lastmod: 2020-01-01T16:45:40+08:00
draft: false
author: "ccjee"
authorLink: "https://dillonzq.com"
description: ""
resources:
- name: "featured-image"
  src: "featured-image.png"
tags: ["Markdown","blog","vuepress",]
categories: ["编程"]

lightgallery: true

toc:
  auto: false
---
<!--more-->
# GitHub部署

## 前提条件

- 安装[Git](https://git-scm.com/)
- 文档放置在项目的 `docs` 目录中；
- 使用的是默认的构建输出位置；
- 发布到 `https://<USERNAME>.github.io/`

## Github配置

1. 创建Github 仓库
登陆 `GitHub`，创建`blog`仓库
2. 在`blog`文件夹中，创建 `deploy.sh` 文件
```
#!/usr/bin/env sh

# 确保脚本抛出遇到的错误
set -e

# 生成静态文件
npm run docs:build

# 进入生成的文件夹
cd docs/.vuepress/dist

# 如果是发布到自定义域名
# echo 'www.example.com' > CNAME

git init
git add -A
git commit -m 'deploy'

# 如果发布到 https://<USERNAME>.github.io
git push -f git@github.com:<USERNAME>/<USERNAME>.github.io.git master

# 如果发布到 https://<USERNAME>.github.io/<REPO>
# git push -f git@github.com:<USERNAME>/<REPO>.git master:gh-pages

cd -

```
3. 双击运行deploy.sh脚本
 查看github，生成的静态文件上传成功