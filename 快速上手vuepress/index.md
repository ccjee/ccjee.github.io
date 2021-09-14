# 快速上手Vuepress

<!--more-->
# 快速上手Vuepress

## 前提条件

使用VuePress 需要安装 [Node.js](https://nodejs.org/en/)，版本号>= 8.6

## 阅读须知

- 本文会帮助你从头搭建一个简单的 VuePress 文档。
- 如果你想在一个现有项目中使用 VuePress 管理文档，从步骤 3 开始。

## 安装步骤

1. 安装Node.js后，打开Node.js command prompt，进入初始页面，如下：
```
Your environment has been set up for using Node.js 14.17.5 (x64) and npm.
C:\Users\CCJEE>
```
2. 输入`d:`(不区分大小写)，进入D盘
3. 在D盘，新建blog文件夹（建议：文件夹存放于非系统盘）
```
mkdir blog
```
4. 进入blog文件夹
```
cd blog
```
5. 使用npm或yarn包管理器进行初始化
```
yarn init 或 npm init
```
6. 安装VuePress
```
yarn add -D vuepress 或 npm install -D vuepress
```

> 安装过程中有报错情况时
1. 删除所有blog文件夹，重新操作
2. 使用yarn初始化、安装Vuepress报错时，换npm进行

7. 创建docs文件夹（在D盘blog文件夹下）
```
mkdir docs
```
8. 在docs文件夹内创建`inbox.md`首页文件，输入以下内容：
```
---
home: true
heroImage: /logo.jpg
actionText: 快速上手 →
actionLink: /zh/guide/
features:
- title: 简洁至上
  details: 以 Markdown 为中心的项目结构，以最少的配置帮助你专注于写作。
- title: Vue驱动
  details: 享受 Vue + webpack 的开发体验，在 Markdown 中使用 Vue 组件，同时可以使用 Vue 来开发自定义主题。
- title: 高性能
  details: VuePress 为每个页面预渲染生成静态的 HTML，同时在页面被加载的时候，将作为 SPA 运行。
footer: MIT Licensed | Copyright © 2018-present Evan You
---
```
参考页面[VuePress](https://vuepress.vuejs.org/zh/)
9. 在 package.json 中添加scripts代码
```
{
  "scripts": {
    "docs:dev": "vuepress dev docs",
    "docs:build": "vuepress build docs"
  }
}
```
10. 本地运行blog
```
yarn docs:dev 或 npm run docs:dev
```
11. 打开链接 http://localhost:8080 查看blog
> VuePress 会在 http://localhost:8080 启动一个热重载的开发服务器。
