---
layout: post
title: "Gradle笔记"
date: 2024-03-14 19:55:06
tags: Gradle, Build
description: 
toc: true
---

## 目录结构

### buildSrc
在比较复杂的构建中，为了更好的组织和复用构建代码，可以引入buildSrc目录，它是一个Java/Kotlin模块项目的形式。这个目录被自动测试和构建，然后添加到项目的构建classpath，项目中的build.gradle.kts可以引用buildSrc中的逻辑。
相比于直接在build.gradle.kts中写构建脚本，buildSr则使用java/kotlin开发，且可以分成多个文件，更加有利于管理和逻辑清晰。
多项目（模块）的情况下，buildSrc只能有一个，并且必须放在项目的根目录下。