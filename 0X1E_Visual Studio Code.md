# 0X1E Visual Studio Code

## 简介

Visual Studio Code（简称VSCode）是微软推出的一款免费开源跨平台的纯文本编辑器（Plain Text Editor）。除了拥有界面舒适，操作方便（对于习惯了Windows和Word的人来说），运行流畅，稳定可靠等过硬的基本素质。还拥有非常强的可拓展性和可自定义性。并且给Visual Studio Code安装插件就像给iOS手机装商店里的应用一样方便。顺便提一句，VSCode还内置了对Git的支持（需要安装Git，并不是VSCode内置了Git本身）。用了VSCode之后我已经很少在命令行里输Git命令了。

VSCode经过设置还能直接在其窗口内启动调试程序和shell。所以你可以把VSCode当作一款轻量级的IDE来使用。但是毕竟VSCode和Visual Studio是两款侧重不同的软件。Visual Studio旨在提供一个功能完备的开发环境。而VSCode仅仅提供一个好用，可拓展的文本编辑器。至于VSCode的其他功能需要靠插件，配置以及你的想象力来补完。

## 和其他编辑器的相互替换

作为一个依赖于图形界面的编辑器。VSCode和VI/VIM根本形不成竞争。你甚至可以把VSCode设置成VIM键位的。

VSCode的主要对手是Atom，Sublime之类的编辑器。一定程度上也可以拉拢部分不坚定的emacs党。

其他编辑器不好评价，但是就我使用Atom和VSCode的经历来说，Atom在速度上比VSCode差很多。而且由于微软一贯的不折磨用户的产品风格。VSCode不会一上来就把你扔进配置海里。就算你什么都不配置，VSCode也是一款挺好用，内置了不少实用工具的，开箱即用的编辑器。

## 获取

上官网下载符合你系统的安装包安装就好了。微软出品的东西不会在安装阶段太折磨人的。目前提供了适用于Windows，Mac和几个主流Linux发行版的安装包。

官网地址：<https://code.visualstudio.com/>

## 基本使用

就像记事本那样用。

如果你要让常用的20%命令更快捷，就去背一背快捷键表：<https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf>

如果你想把剩下80%的功能也用到，按Ctrl+p打开命令栏输入命令就行（带自动补全哦）。

官网上还有非常详细的文档和教程：<https://code.visualstudio.com/docs>

## 信息总结

* 功能定位：可拓展的纯文本编辑器
* 平台支持：Windows, Linux, Mac
* 开源（MIT协议）：<https://github.com/Microsoft/vscode/>
* 拓展性：支持插件拓展
* 费用：免费
* 网址：<https://code.visualstudio.com/>
* 意见：通用的主力代码查看器，轻量级代码编辑器（或者IDE窗口）。微软出品，不是精品也差不多了。况且这还是微软拥抱开源之后的一个产品。

## 插件推荐

可能是为了保持程序本体的轻量。微软把很多功能做成了拓展插件，而非直接打包在本体里。另外还有很多热情的社区贡献者为VSCode编写的插件。根据需求装几个插件可以让你的使用体验更好。就我自己的使用经验在这里简单介绍几个插件：

### Chinese (Simplified) Language Pack for Visual Studio Code

<https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-zh-hans>

VSCode的简中本地化文件。不装这个，VSCode中的菜单栏什么的默认是英文。启用这个拓展后变成中文。

### Markdown+Math

<https://marketplace.visualstudio.com/items?itemName=goessner.mdmath>

增加Markdown中增加对$\KaTeX$风格的数学公式的支持。

### markdownlint

<https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint>

一款适用于Markdown的lint工具。帮助你写出代码风格规范的Markdown文档。

### Python

<https://marketplace.visualstudio.com/items?itemName=ms-python.python>

微软官方出品的Python支持插件。安装后可以在VSCode中使用Pylint，Python调试等功能。

### Excel Viewer

<https://marketplace.visualstudio.com/items?itemName=GrapeCity.gc-excelviewer>

电子表格渲染查看工具。让你不用再对着一堆逗号头号头疼。

而且除了支持CSV还支持TSV和Excel。