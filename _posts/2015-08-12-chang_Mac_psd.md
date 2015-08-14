---
layout: post
title: Mac如何修改开机密码
description: "其他"
categories: 其他
tags: [工具]
imagefeature: pic-2014-09-08.jpg
comments: true
mathjax: null
featured: true
published: true
---

###Mac的开机密码忘了咋办？

	1.打开你的Mac，一直按住 command + S 进入你的终端界面
	2.输入 /sbin/mount -uaw /  
	3.输入 rm /var/db/.AppleSetupDone    (删除)
	4.reboot                          (重新启动)

---

####中间的空格别忘了输入

接下来就是重新配置你的Mac电脑了，时间、Apple账号、新密码等
