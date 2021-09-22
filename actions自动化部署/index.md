# Hugo + GitHubPages + Github Actions

本地添加文章，提交到Github，自动触发Github Actions发布到Github Pages进行托管。
<!--more-->

## 步骤1：准备工作

- 新建blog源码仓库：ccjee.github.io.source
	- 源码仓库设置为 Private（不公开）
	- 存放blog源码（blog站点文件夹）
- 新建public文件夹仓库：ccjee.github.io
	- 存放静态文件（站点文件夹下执行`hugo`代码，生成的public文件夹） 

## 步骤2：将 ccjee.github.io.source  与 ccjee.github.io 进行绑定 SSH Key
1. 生成ssh key
2. 将id_rsa.pub添加到 ccjee.github.io 仓库
3. 将id_rsa添加到 ccjee.github.io.source 仓库（Secrets 变量名为：ACTIONSDEPLOYKEY）
> 实现效果
通过Git提交源码至 ccjee.github.io.source 后，Github Actions编译生成静态文件，并Git Push到 ccjee.github.io
## 步骤3：将 ccjee.github.io.source 仓库克隆到本地
```
# 选取目录（建议非系统盘）
d:

# 创建存放github克隆到本地文件的文件夹
mkdir ccjee_source

# 进入ccjee_source文件夹
cd ccjee_source

# 克隆 ccjee.github.io.source 仓库
git clone git@github.com:ccjee/ccjee.github.io.source.git

# 进入仓库
cd ccjee.github.io.source/ 
```
## 步骤4：生成 Hugo 源码并进行配置
```
# 在ccjee.github.io.source目录下生成 Hugo 源码
hugo new site . 

# 本地运行预览
hugo serve
```
## 步骤5：推送 Github 仓库(即ccjee.github.io.source)
```
git add .
git commit -m "first commit"
git push -u origin main
```
## 步骤6：配置 ccjee.github.io.source 仓库的 Github Actions
复制以下内容覆盖原内容,修改远程仓库、分支名称即可
```
name: Deploy Hugo Site to Github Pages on Master Branch

on:
  push:
    branches:
      - main

jobs:
  build-deploy:
    runs-on: ubuntu-18.04
    steps:
      - uses: actions/checkout@v1  # v2 does not have submodules option now
       # with:
       #   submodules: true

      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v2
        with:
          hugo-version: '0.62.2'
          # extended: true

      - name: Build
        run: hugo --minify

      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          deploy_key: ${{ secrets.ACTIONS_DEPLOY_KEY }} 
          external_repository: ccjee/ccjee.github.io
          publish_dir: ""
          keep_files: false # remove existing files
          publish_branch: main  # deploying branch
          commit_message: ${{ github.event.head_commit.message }}
```

## 步骤7：检查 Github Actions 自动部署
手动开始动作 或 本地重新 commit 后，查看日志

## 步骤8：访问 https://ccjee.github.io/ 查看效果

## 写`blog`或`修改文件`后常用命令
```
# 生成静态文件
hugo

# 添加所有修改过的文件
git add .

# 说明这次提交记录
git commit -m "Add a new post"  

# 将本地的更新，推送到github
git push -u origin main
```
