---
layout: post
title: "Android Studio配置Kotlin开发环境的最简单方式"
date: 2017-05-20
description: "Android Kotlin开发环境的最简单构建方式"
tag: Android 
---   

　　一觉醒来发现Google正式把Kotlin纳入Android程序官方的一级开发语言，这可能也在大家的意料之中,因为Google和oracle的官司
    废话不多说，首选了解一下Kotlin
    Kotlin[http://kotlinlang.org/](http://kotlinlang.org/) 主要由俄罗斯团队 JetBrains 开发，能与 Java 互通，但拥有 Java 不支持的功能。官方是这样描述的:Statically typed programming language
for modern multiplatform applications,100% interoperable with Java™ and Android™ ,[https://blog.jetbrains.com/kotlin/2017/05/kotlin-on-android-now-official/](https://blog.jetbrains.com/kotlin/2017/05/kotlin-on-android-now-official/), 这就是它的大致说明。
    如果你已经使用了Android Studio 3.0预览版, 他将会自动支持Kotlin， 同时还可以将你的Java 代码转换成Kotlin
    如果你使用的是Android Studio 3.0以下，请做以下配置

    第一步:下载插件
    [图片](images/posts/kotlin/1.png)
    第二步:快速配置Android Studio
    [图片](images/posts/kotlin/2)
    第三步:点击“OK”之后，Kotlin插件会自动开始配置。配置完成之后，同步一下工程（Sync Project）即可。
    更多的用法，请见：http://kotlinlang.org/docs/tutorials/android-plugin.html