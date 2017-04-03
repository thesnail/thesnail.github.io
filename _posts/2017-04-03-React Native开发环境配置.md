---
layout: post
title: "React Native搭建开发环境"
date: 2017-04-03 
description: "React Native已经进化了很多版本，开发环境的配置也发生了一些改变，本文仅供参考，请按照官方指引配置，防止某些细节出入导致配置失败。官方英文版配置说明(转载[www.scott-cry.xin](www.scott-cry.xin)"
tag: React Native 
---   

　　React Native的开发环境配置直接参考官方文档即可完成，不过对小白来说东西有点多，有些名词不是很好理解，这里就(官方的[安装文档](http://facebook.github.io/react-native/)稍微展开说一下。[http://reactnative.com/](http://reactnative.com/)

　　译注：如果`阅读完教程`后还碰到很多环境搭建的问题，我们建议你还可以再看看由[reactnative.cn](http://reactnative.cn/)提供的[环境搭建视频教程](http://v.youku.com/v_show/id_XMTQ4OTYyMjg4MA==.html)、[windows环境搭建文字教程](http://bbs.reactnative.cn/topic/10)、以及[常见问题](http://bbs.reactnative.cn/topic/130)。

## 安装

### 1、安装HomeBrew
第一: 通过命令行安装HomeBrew

    ruby -e “$(curl –insecure -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)”

第二: 查询HomeBrew的版本

    XXXXX-Mac:~ scottwang$ brew -v
    Homebrew 1.1.11
    Homebrew/homebrew-core (git revision 8663; last commit 2017-04-02)
    XXXXX-Mac:~ scottwang$

　　至此说明HomeBrew已经安装成功。

### 2、安装NodeJs
使用[Homebrew](http://brew.sh/)来安装[Node.js](https://nodejs.org/)
（对解析JS所需的环境node+安装之后你就可以用npm命令了）

    XXXXXX-Mac:~ scottwang$ brew install node
    ......
    XXXXXX-Mac:~ scottwang$ node -v
    v6.10.0


　　安装完node后建议设置[npm镜像](https://www.baidu.com/s?ie=UTF-8&wd=npm%E9%95%9C%E5%83%8F%E4%BB%A5%E5%8A%A0%E9%80%9F)以加速后面的过程（或使用[科学上网工具](https://www.baidu.com/s?ie=utf-8&f=8&rsv_bp=1&rsv_idx=1&tn=baidu&wd=%E7%A7%91%E5%AD%A6%E4%B8%8A%E7%BD%91&oq=npm%25E9%2595%259C%25E5%2583%258F%25E4%25BB%25A5%25E5%258A%25A0%25E9%2580%259F&rsv_pq=ac6ecffc000569a4&rsv_t=a6dfnk2LVwrQb%2BMub1C9r%2F5C4E2fs8%2F7LK8FpawDEhScyN4%2FQESXgaxOu0g&rqlang=cn&rsv_enter=0&rsv_sug3=2&rsv_sug1=1&rsv_sug7=000&inputT=795&rsv_sug4=1384&rsv_sug=1)),因为天朝的网络你懂得。

    npm config set registry https://registry.npm.taobao.org --global
    npm config set disturl https://npm.taobao.org/dist --global

### 3、React Native的命令行工具（react-native-cli）
React Native的命令行工具用于执行创建、初始化、更新项目、运行打包服务（packager）等任务。

    npm install -g react-native-cli

如果你看到EACCES: permission denied这样的权限报错，那么请参照上文的homebrew译注，修复/usr/local目录的所有权：

    sudo chown -R `whoami` /usr/local

### 4、Xcode
React Native目前需要Xcode 7.0 或更高版本。你可以通过App Store或是到[Apple开发者官网](https://developer.apple.com/xcode/downloads/)上下载。这一步骤会同时安装Xcode IDE和Xcode的命令行工具。

```
虽然一般来说命令行工具都是默认安装了，但你最好还是启动Xcode，并在Xcode | Preferences | Locations菜单中检查一下是否装有某个版本的Command Line Tools。Xcode的命令行工具中也包含一些必须的工具，比如git等。
```
### 5、测试安装

    react-native init reactIOS
    cd reactIOS
    react-native run-ios

### 6、React Native开发工具IDE
所谓工欲善其事必先利其器,做React Native开发也和其他应用开发一样，但是工具有很多种，可能每个公司用的也不一样。下节就给大家介绍几款比较好用的IDE:[sublime](http://www.sublimetext.com/3)、[webstorm](https://www.jetbrains.com/webstorm/)以及官网推荐的[Nuclide](https://atom.io/)、[VSCode](https://code.visualstudio.com/)-[中文](http://www.vscode.org/)

转载请注明原地址，LCry的博客：[http://scott-cry.win/](http://scott-cry.win/) 谢谢！