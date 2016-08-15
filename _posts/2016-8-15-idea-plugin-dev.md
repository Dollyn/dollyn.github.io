---
title: 2016-8-15-idea-plugin-dev
tags: IDEA,Plugin,小书匠
grammar_cjkRuby: true
---


# 0. 准备工作

## 下载Intellij IDEA 社区版
idea社区版是一个开源免费的版本，相对于商业版，少了对JEE等特性的支持，但对于普通的Java开发是够用的。我们做插件开发就使用这个版本，可以到这里下载: 
https://www.jetbrains.com/idea/download/#section=windows

## 安装
没有什么特别的，不再赘述。 装都装不上的话，这篇文章可以暂时不要看了...

## Checkout 源码（可选）
下载源码可以让你方便地参考（抄袭）IDEA平台自带插件的实现方式（源码），推荐下载下来，并和SDK绑定，需要的时候可以直接看源码。
下载地址：
git clone --depth 1 git://git.jetbrains.org/idea/community.git idea

或者使用github上的镜像地址：https://github.com/JetBrains/intellij-community
（由于Idea现在自带反编译插件，所以没有源码也可以凑合着用，大家自行决定，毕竟这个源码库还是有点大，又在国外，没有好的代理下不下来也是很正常的...）


# 1. 新建一个插件项目

File --> New --> Project
打开新建项目向导，选择Intellij Platform Plugin：

![New Project](images/posts/2016-08-15-idea-plugin-dev/new_project_1.png)
 
初次运行的话，这里的SDK列表是空的，所以需要手动新建一个。 点击右侧的New...按钮：


选择IDEA的安装目录， 然后会弹出要求你选择一个JDK，

最后，如果前面从git中下载了源码， 在这里添加上源码的路径：
 


 然后进入下一步，输入项目的名字和路径：

 