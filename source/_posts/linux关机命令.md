---
title: linux关机命令
date: 2019-09-06 21:30:20
categories:
- 运维
tags:
---
　　我们在使用linux的时候，很多人经常会像window一样的关机，其实这样的关机方法对于linux是很不好的，这样不利于linux，还可能会导致有些文件的丢失，那么在命令中有哪些是关机的呢?

　　linux下常用的关机命令有：shutdown、halt等;重启命令一般使用：reboot。

　　重启命令　　reboot 重启

　　(以下几个一般是root用户)

　　shutdown -r now 立刻重启

　　shutdown -r 10 过10分钟自动重启

　　shutdown -r 22:22 在时间为22:22时候重启

　　shutdown -c 取消重启

　　关机命令　　halt 关机

　　poweroff 立刻关机

　　shutdown -h now 立刻关机

　　shutdown -h 5 5分钟后自动关机

　　我个人一般重启用reboot命令，关机一般用shutdown -h now，个人习惯，其实都可以，就是不要像window那样关机就好
