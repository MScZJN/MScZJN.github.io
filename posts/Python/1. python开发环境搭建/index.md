---
layout: page
title: Python开发环境搭建
image:
    feature: abstract.jpg
comments: true
modified: 2016-03-13
---

## 安装Homebrew
首先你需要知道Mac默认的python版本为2.7，但是在学习过程中很可能会需要使用其他版本的python。系统自带的2.7版本会影响很多软件的时候，所以保持这个版本的相对纯净比较重要。

**Homebrew**可以理解成类似“App Store”或者“Google Store”这类软件平台，区别是他安装的是各种源码而不是封装好的软件包。

打开终端输入下面的命令：

`ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"`

等待下载并安装完成即可。

常用命令：

> 安装软件：brew install + name  
> 卸载软件：brew uninstall + name  
> 已安装列表：brew list  
> 更新Homebrew：brew update      
<!-- more -->

## 安装pyenv
**pyenv**是python的版本管理器，有了他我们可以干净利落的在各个python版本间切换而不至于把系统搞得一团糟。

在终端输入下面的命令来安装pyenv：

`brew install pyenv`

为了使pyenv的命令生效我们需要更改pyenv的root path，具体做法：

1. `cd`到根目录下	
2. 输入`touch .bash_profile`创建 .bash_profile 文件
3. 输入`mvim .bash_profile`打开文件
4. 输入以下内容到 .bash_profile 内：     
`export PYENV_ROOT=/usr/local/opt/pyenv`  
`if which pyenv > /dev/null; then eval "$(pyenv init -)"; fi`
5. 输入`:wq`写入并退出
6. 输入`SHELL -l`，.bash_profile 文件会生效pyenv就配置好了

附上一些常见的pyenv命令供大家玩耍：

>查看所以可以安装的python版本：pyenv install --list    
>安装特定版本的python：pyenv install + version，例子：pyenv install 2.7.8    
>查看当前使用的python版本：pyenv version    
>查看所以安装的python版本：pyenv versions    
>设置全局python版本：pyenv global + version    
>注：每次运行完 pyenv install 后，需要运行 pyenv rehash 来刷新。    
<!-- more -->

到此玩耍python之前的准备工作就算做完了，**以上操作仅针对MAC系统**。

## 参考
* [**Homebrew**](http://brew.sh/) 官方教程
* [**pyenv**](https://github.com/yyuu/pyenv) GitHub


