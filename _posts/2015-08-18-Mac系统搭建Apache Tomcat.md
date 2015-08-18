---
layout: post
title: "Mac系统搭建Apache Tomcat"
description: "SVN"
category: SVN
tags: [SVN]
imagefeature: pic-2014-09-08.jpg
comments: true
mathjax: null
featured: true
published: true
---



###1.下载Eclipse

###2.下载Tomcat  [http://tomcat.apache.org/download-70.cgi](http://tomcat.apache.org/download-70.cgi)


![2](http://www.himigame.com/wp-content/uploads/2012/05/11.png)
<br/>
下载Core:(zip.pgp,md5)

###3.shift+commond+G进入 /usr/local/ 文件夹下将刚才解压后的tomcat文件夹整个放到整个目录

###4.打开终端输入pico .bash_profile  

###5.添加一个路径 export PATH=$PATH:/usr/local/apache-tomcat-7.0.63/bin

![1](http://www.himigame.com/wp-content/uploads/2012/05/3.png)
编辑完后，control+x   （保存）    继续 ：y   （同意）     回车；
###6.启动tamcat
1)如果你配置了（便捷）这一步，你可以直接在终端输入    ./startup.sh

2) 如果你没有配置（便捷）这一步，首先  cd  xxxx   (xxx表示你tomcat放至的路径例：cd /usr/local/apache-tomcat-7.0.32/bin)，回车找到路径后，

然后再输入  ./startup.sh

![3](http://img.my.csdn.net/uploads/201210/15/1350274550_4856.png)
如果当 startup.sh后出现类似 “Permission denied” 字样，那么需要你对此目录进行权限设置：

启动终端：输入   sudo chmod 755 xxx/bin/*.sh     (xxx表示你tomcat放至的路径) 回车；

OK，再次在终端输入 startup.sh 进行启动tomcat；

![4](http://img.my.csdn.net/uploads/201210/15/1350274642_7160.png)

如果出现

Neither the JAVA_HOME nor the JRE_HOME environment variable is defined
At least one of these environment variable is needed to run this program

的错误提示

请查看jdk是否安装了，在finder里面进入你的应用安装－》实用工具然后双击下面图表安装
![5](http://img.my.csdn.net/uploads/201210/15/1350274776_9235.png)


###7.打开你的  safari  ，然后网址输入  [http://localhost:8080/](http://localhost:8080/)
![6](http://www.himigame.com/wp-content/uploads/2012/05/22222.png)

---

##[Mac下eclipse安装SVN插件](http://www.cnblogs.com/yinxiangpei/articles/3859057.html)


---

