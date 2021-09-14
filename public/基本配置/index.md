# vuepress基本配置

<!--more-->
# 基本配置

## 配置文件

1. `docs`文件夹下创建 `.vuepress` 文件夹
```
cd docs
mkdir .vuepress
```
2. 在`.vuepress` 文件夹内创建 `config.js`文件
```
cd .vuepress
touch config.js
```
3. `config.js`是核心配置文件，所有菜单、栏目相关的配置均配置在该文件中
```
module.exports = {
  title: 'Hello VuePress',
  description: 'Just playing around'
}
```
4. 参考`默认主题配置`、`自定义主题配置`，对`config.js`文件进行编辑
[配置](https://vuepress.vuejs.org/zh/config/) 来查看所有可配置的选项。
```
module.exports = {
  title: 'CCJEE Journal',
  description: '关注学习过程 关注分享',
  head: [
    ['link', { rel: 'icon', href: '/logo.webp' }]
  ],
	themeConfig: {
    nav: [
      { text: '首页', link: '/' },
      { text: '关于', link: '/about.html' },
      { text: 'Windows', link: '/software.html' },
      {
        text: '项目',
        items: [
            {
              text: '数据分析',
              items: [
                {text: '数据化管理（1）', link: '/project/data/day1.html'},
                {text: '数据化管理（2）', link: '/project/data/day2.html'},
                {text: '自学数据分析', link: '/project/data/guide.html'}
              ]
            },
            {
              text: '读书笔记',
              items: [
                {text: '美团的成长与进化逻辑', link: '/project/read/meituan.html'}
              ]
            },
            {
              text: 'Obsidian笔记',
              items: [
                {text: '我的Obsidian使用方法', link: '/project/obsidian/obsidian.html'},
                {text: 'Markdown语法', link: '/project/obsidian/markdown.html'},
                {text: 'Obsidian个人知识管理', link: '/project/obsidian/个人知识管理.html'}
              ]
            },
            {    
              text: '生活',
              items: [
                  {text: '记录锅具选择、使用', link: '/project/life/锅具.html'}
              ]
            }
        ]
      }
    ]
  },
  plugins: [
    [
      '@vuepress/plugin-search',
      {
        placeholder: '搜索',
      },
    ],
    ['@vuepress/back-to-top'],
    ['@vuepress/plugin-pwa'],
  ],
}
```
## 主题配置
[默认主题配置](https://vuepress.vuejs.org/zh/theme/default-theme-config.html) 
[自定义配置](https://vuepress.vuejs.org/zh/theme/)
参考Vuepress官网[配置教程](https://vuepress.vuejs.org/zh/config/)
## 静态资源配置
vuepress程序默认的图片目录是`/docs/.vuepress/public`
```
cd .vuepress
mkdir public
```
## 本地运行blog
