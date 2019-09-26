---
title: ubuntu安装mysql数据库方法
date: 2019-09-09 08:54:50
categories:
- 数据库
tags:
- mysql
- 数据库
---
<p>　　ubuntu基于linux的免费开源桌面PC操作系统，十分契合英特尔的超极本定位，支持x86、64位和ppc架构。一个比较流行的Linux操作系统，不仅简单易用，而且和Windows相容性非常好。那么在ubuntu中如何安装mysql数据库呢?</p>
<p>　　在ubuntu安装mysql主要有以下两种方式：</p>
<p>　　1.打开Ubuntu Software Center，在右上角的搜索框查询mysql，然后选定MySQL Server，点击安装即可。</p>
<p>　　2.使用命令安装mysql,毕竟Ubuntu系统主要是以命令为主嘛。</p>
<p>　　打开ubuntu的终端执行：<span style="color: #ff0000;">sudo apt-get install mysql-server</span></p>
<p>　　然后可以看到一系列的执行过程，等待一会就安装完成了。</p>
<p>　　下面进入mysql,跟cmd一样，<span style="color: #ff0000;">mysql -h localhost - u root -p</span> 然后输入sudo的密码即可。</p>
<p>　　这样就进入ubuntu的数据库了，接着的操作就是数据库的常规操作了。</p>