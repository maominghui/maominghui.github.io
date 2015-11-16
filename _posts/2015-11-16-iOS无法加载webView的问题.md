---
layout: post
title: iOS无法加载webView的问题
description: "iOS"
category: iOS
tags: [iOS]
imagefeature: pic-2014-09-08.jpg
comments: true
mathjax: null
featured: true
published: true
---


>加载webView时报错

* 在plist文件中增加一个Key，`App Transport Security Settings`，值为Dictionary，在其下面增加一个`Allow Arbitrary Loads`,Type值为Boolean，Value值为YES。