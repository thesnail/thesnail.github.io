---
layout: post
title: "React Native IDE选型和配置"
date: 2017-04-03 
description: "React Native已经进化了很多版本，开发环境的配置也发生了一些改变，本文仅供参考，请按照官方指引配置，防止某些细节出入导致配置失败。官方英文版配置说明(转载[www.scott-cry.xin](www.scott-cry.xin)"
tag: React Native 
---   

　　React Native 的开发基本上是 Javascript ＋ 系统原生开发语言（Java，Objective-C，Swift），原生语言的开发所用的 IDE 没有多余的选择，Android 平台只能使用 Android Studio（不要告诉我你还在使用 Eclipse），iOS 平台只能使用 XCode，而开发 Javascript 的 IDE 选择就多了，从 FaceBook 官方推荐的 Atom＋Nuclide，到与 Android Studio 同系列的 Javascript IDE WebStorm，再到功能强大的 Sublime Text 3，以及微软推出的 Visual Studio Code 和 decosoftware 专门为 React Native 打造的开源 IDE Deco，甚至 Vim，NodePad++ 等等，都可以用来开发 React Native，唯一的前提能够支持识别 Javascript 语法，识别 JSX 和 React Native API 的智能提醒。接下来我们就来介绍最常用的五款 IDE 的配置和选型。

## React Native IDE

### 1、Atom + Nuclide
　　第一: [Atom](https://atom.io/)是由 Github 打造的下一代编程开发利器，支持 Windows、Mac OS X、Linux 三大桌面平台，免费且开源。[Atom](https://atom.io/)  支持各种编程语言的代码高亮，同时具备强大的代码补全功能，能够极大的提高编程效率，[Atom](https://atom.io/)  本质上是一个文本编辑器，而不是一个 IDE，因此在用来开发 React Native 时需要配合 Nuclide 一起使用。
<img src="/images/react/20170403/atom.io.png" height="460" width="800"> 

　　第二: [Atom](https://atom.io/)已经安装成功了，下面开始安装[Nuclide](https://github.com/facebook/nuclide)，直接打开Atom软件，点击Atom-> Preferences打开Setting，然后点击install，输入nuclide-installer搜索，进行下载即可
<img src="/images/react/20170403/nuclide.io.png" height="360" width="800"> 

### 2、WebStorm IDE介绍和安装
　　我相信做过Web前端的童鞋们，肯定对WebStorm IDE非常的熟悉WebStorm 是jetbrains公司旗下一款JavaScript开发工具。被广大中国JS开发者誉为“Web前端开发神器”、“最强大的HTML5编辑器”、“最智能的JavaScript IDE”等。与IntelliJ IDEA同源，继承了IntelliJ IDEA强大的JS部分的功能。该IDE官网地址:[https://www.jetbrains.com/webstorm/](https://www.jetbrains.com/webstorm/)。该新版本已经支持了React了，所以在现如今的开发阶段WebStrom已经算是支持性最好的IDE了，大家有兴趣可以下载使用以下哦~，不过该是收费的,相信你也会有[办法](https://www.baidu.com/s?ie=utf-8&f=3&rsv_bp=1&rsv_idx=1&tn=baidu&wd=webstorm%2010%20%E6%B3%A8%E5%86%8C%E7%A0%81&oq=webstorm&rsv_pq=8b460dd700068735&rsv_t=aaacEWo%2BiGh1ZpNk2F8Ye6bDjqd8KJbUPUn9nY22TI1NZAUaZjMI%2FdQCZzI&rqlang=cn&rsv_enter=1&rsv_sug3=7&rsv_sug1=6&rsv_sug7=100&rsv_sug2=1&prefixsug=webstorm&rsp=0&rsv_sug4=2224)的。

### 3、Sublime Text 3
　　Sublime Text 3 是一款广泛使用的代码编辑器，支持 Windows、Mac OS X、Linux 三大桌面平台，它是付费应用，但目前可以无限期的试用。它支持多种编程语言的语法高亮、拥有优秀的代码自动完成功能，还拥有代码片段（Snippet ）的功能，可以将常用的代码片段保存起来，在需要时随时调用，极大的提高编程效率。
　　一、简单的安装方法
　　使用Ctrl+`快捷键或者通过View->Show Console菜单打开命令行，粘贴如下代码：

```
import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

如果顺利的话，此时就可以在Preferences菜单下看到Package Settings和Package Control两个菜单了。
如有问题 参考:[https://packagecontrol.io/installation#st3](https://packagecontrol.io/installation#st3)

　　二、安装插件 babel-sublime
　　支持ES6， React.js, jsx代码高亮，对 JavaScript, jQuery 也有很好的扩展。
　　安装

　　PC上ctrl+shift+p（MacCmd+shift+p）打开面板
　　选择Install Package
　　输入babel安装

　　配置

　　打开.js, .jsx 后缀的文件;

　　打开菜单view，Syntax -> Open all with current extension as... -> Babel -> 　　JavaScript (Babel)，选择babel为默认 javascript 打开syntax

　　修改TAB缩进为空格

　　在sublime text中将TAB缩进直接转化为4个空格，可以按照如下方式操作：

　　菜单栏: Preferences -> Settings – More -> Syntax Specific – User

　　然后添加设置代码就可以了，文件保存在$Packages/User下

　　另：
　　font_face 设置字体
　　font_size 设置字体大小

    {
        "font_face": "SourceCodePro",
        "font_size": 14,
        "tab_size": 4,
        "translate_tabs_to_spaces": true
    }


### 3、VS Code
　　React Native智能开发工具，可代码提醒的IDE——VS Code。
　　安装VS Code方法非常简单，去github上下载插件，直接安装在电脑就可以了。
　　插件地址:[https://github.com/Microsoft/vscode-react-native](https://github.com/Microsoft/vscode-react-native)
　　它具有打开文件夹功能，定位到React Native项目的根目录直接使用文件夹打开功能就可以，这样就可以把整个项目目录放进去了