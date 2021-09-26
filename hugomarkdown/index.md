# Hugo Markdown

<!--more-->
---
# Hugo Markdown

## 说明文档
[Hugo中文文档](https://www.gohugo.org/doc)

### 本地服务预览

```
hugo server
```

## Front Matter
[官方文档Front Matter](https://www.gohugo.org/doc/content/front-matter/)

### Front Matter范例

```yaml
---
weight: 1  #权重排序
title: "文章标题"  #标题
date: 2021-09-11T21:57:40+08:00  #日期
lastmod: 2021-09-14T16:45:40+08:00 #更新日期
draft: false #表示是否是草稿，编辑完成后请将其改为 false
author: "ccjee" #作者
authorLink: "https://dillonzq.com" #作者链接
description: "内容描述" #内容描述
resources:
- name: "featured-image"
  src: "featured-image.png"
tags: ["Markdown","blog","hugo","GitHub Pages","Github Actions"] #标签
categories: ["编程"] #分类
keywords: #关键词
- 关键词
showless: true  #设置部分内容可访问
mermaid: true #为true时通过脑图渲染节点
lightgallery: true #支持触屏滑动的响应式相册
toc: #目录导航
  auto: false
---
```
### 自定义支持脑图mindmap

自定义属性，文章支持脑图/思维导图

```
mindmap: true #为true时通过脑图渲染节点
```

文章中如何写脑图节点：[自定义mind脑图shortcodes](#%E8%87%AA%E5%AE%9A%E4%B9%89mind%E8%84%91%E5%9B%BEshortcodes)

### 自定义支持绘图mermaid

采用mermaid的绘图方案，官方文档：[mermaid绘图帮助文档](https://mermaid-js.github.io/mermaid/)

```
---
mermaid: true #为true时支持mermaid绘图展示
---
```
参考：官方帮助文档：[mermaid绘图帮助文档](https://mermaid-js.github.io/mermaid/#/flowchart)
