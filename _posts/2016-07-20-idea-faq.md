---
layout: post
title: "Intellij IDEA使用说明"
date: 2016-07-20 16:25:06
tags: IDEA
description: 
toc: true
---

## 运行和调试

### 运行Maven工程中的Java类，找不到tests中资源的问题
是因为在src/java下面运行的时候，classpath里没有带上target/test-classess，解决方案就是在src/test下面转一次，再写个java类调用。 test下面的类运行的时候会自动带上tests下的资源。


