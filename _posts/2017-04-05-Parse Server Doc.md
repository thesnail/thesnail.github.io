---
layout: post
title: "Parse Server Doc"
date: 2017-04-05 
description: "Parse Server is open server"
tag: Parse Server 
---   

　　从去年开始公司的一个项目的app后端使用的是Parse Server，但是在前几天我开发IOS版本时发现DOC不见了,心里想是不是被黑了,最后在[stackoverflow](www.stackoverflow.com),我发现它说了这句话

```
As of April 5, 2017, Parse, LLC has transferred this code to the parse-community organization, and will no longer be contributing to or distributing this code. 
```

    只是我一直没发现,也就不瞎扯了,下面就说说它的发展史和他的文档是怎么搭建的
 
### Parse Server 发展史
　　Parse开始是一个以服务平台的形式作为移动后端,就像做app不需要再做服务器，我们可以直接使用它,但是在2013年的时候被Facebook收购了,可能是因为一直没有盈利，或者其他原因，2016年1月，Parse公司宣称他们将在2017年1月关闭服务。2017年5月Parse有限责任公司已将此代码转移给解析社区组织，不再为此代码做出贡献或分发。也就是把它托管在[github](www.github.com),感觉就像放弃了一样.虽然他们不再更新，但是它们里面的代码值得我们学习.

　　为了让用户将他们的应用从Parse服务器搬到他们自己的服务器，Parse公司已经发布了它的后端的一个开源版本，叫做[Parse Server](https://github.com/ParsePlatform/)

### [Parse Server Doc](https://github.com/parse-community/docs)搭建

1. 你需要Ruby, [Bundler](http://bundler.io/), and [npm](https://www.npmjs.com/).
　　
2. 安装Ruby,Bundler,npm,nodejs 等

3. 下载［Parse Server Doc]()到本地
　　
然后cd 到下载的目录下面

4. 安装库

```
bundle install
npm install
```

5. 然后运行webpack and Jekyll:

```
npm start
```
6. 最后在浏览器中打开:[http://localhost:4000/](http://localhost:4000/);