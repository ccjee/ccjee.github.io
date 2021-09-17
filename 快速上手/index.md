# hugo搭建blog基本配置

<!--more-->

## 快速上手Hugo

### 前提条件

- 安装[Hugo](https://github.com/gohugoio/hugo/releases)
- 安装 [Git](https://git-scm.com/)

### 安装Hugo

- windows
	- 下载及解压
		- 解压后将hugo.exe文件放到新建的`\Hugo\bin`下，例如：`D:\Hugo\bin`
	- 添加环境变量
		- 添加方法可参考[如何添加环境变量](https://jingyan.baidu.com/article/8ebacdf02d3c2949f65cd5d0.html)。
	- 查看hugo版本信息
		- Git Bash 中输入 `hugo version`
		- `hugo static site generator`信息表示安装完成。

### 安装主题

hugo没有自带主题，需要先安装主题

#### 安装方式

- 安装方式
	- CMD中`git clone`安装
	- 下载主题文件[Hugo官网主题库](https://themes.gohugo.io/)
		- 解压文件到`themes`文件夹(详细步骤参照对应主题的使用说明文档)
			- 进入 **blog/themes/even/exampleSite** 文件夹，将 **config.tom** 文件拷贝到项目根目录下，同时将 **blog/themes/even/exampleSite/content** 文件夹覆盖掉根目录下的 **content** 。

#### 安装[hugo-theme-bootstrap主题](https://github.com/razonyang/hugo-theme-bootstrap)
```
cd hugo-blog #进入文件夹
git init #初始化
git submodule add https://github.com/razonyang/hugo-theme-bootstrap themes/hugo-theme-bootstrap #下载主题
xcopy .\themes\hugo-theme-bootstrap\exampleSite /E  #移动文件
hugo server #本地运行
```
详情参考[hugo-theme-bootstrap说明文档](https://github.com/razonyang/hugo-theme-bootstrap/blob/master/README.zh-CN.md)


