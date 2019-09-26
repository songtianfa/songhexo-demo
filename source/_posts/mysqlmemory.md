---
title: MySQL存储引擎的介绍
date: 2019-09-10 15:14:23
categories:
- 数据库
tags:
- mysql
- 数据库
---
　　　数据库存储引擎是数据库底层软件组件，数据库管理系统使用数据引擎进行创建、查询、更新和删除数据操作。不同的存储引擎提供不同的存储机制、索引技巧、锁定水平等功能，使用不同的存储引擎还可以获得特定的功能。

　　现在许多数据库管理系统都支持多种不同的存储引擎。MySQL 的核心就是存储引擎。

　　如创建一个InnoDB类型的表：

　　CREATE TABLE `yingqing` (

　　`goods_id` int(11) NOT NULL AUTO_INCREMENT,

　　`goods_name` varchar(30) NOT NULL DEFAULT '0',

　　`goods_number` int(11) NOT NULL DEFAULT '0',

　　`shop_price` varchar(30) NOT NULL DEFAULT '0',

　　`market_price` varchar(30) NOT NULL DEFAULT '0',

　　`click_count` bigint(20) NOT NULL DEFAULT '0',

　　PRIMARY KEY (`goods_id`)

　　)

　　ENGINE=InnoDB DEFAULT CHARSET=utf8;

　　下面为大家介绍一下mysql常用的存储引擎：

　　MyISAM：MySQL 5.0 之前的默认数据库引擎，最为常用。拥有较高的插入，查询速度，但不支持事务

　　InnoDB：事务型数据库的首选引擎，支持ACID事务，支持行级锁定, MySQL 5.5 起成为默认数据库引擎

　　BDB：源自 Berkeley DB，事务型数据库的另一种选择，支持Commit 和Rollback 等其他事务特性

　　Memory：所有数据置于内存的存储引擎，拥有极高的插入，更新和查询效率。但是会占用和数据量成正比的内存空间。并且其内容会在 MySQL 重新启动时丢失

　　Merge：将一定数量的 MyISAM 表联合而成一个整体，在超大规模数据存储时很有用

　　Archive：非常适合存储大量的独立的，作为历史记录的数据。因为它们不经常被读取。Archive 拥有高效的插入速度，但其对查询的支持相对较差

　　Federated：将不同的 MySQL 服务器联合起来，逻辑上组成一个完整的数据库。非常适合分布式应用

　　Cluster/NDB：高冗余的存储引擎，用多台数据机器联合提供服务以提高整体性能和安全性。适合数据量大，安全和性能要求高的应用

　　CSV： 逻辑上由逗号分割数据的存储引擎。它会在数据库子目录里为每个数据表创建一个 .csv 文件。这是一种普通文本文件，每个数据行占用一个文本行。CSV 存储引擎不支持索引。

　　BlackHole：黑洞引擎，写入的任何数据都会消失，一般用于记录 binlog 做复制的中继

　　EXAMPLE ：存储引擎是一个不做任何事情的存根引擎。它的目的是作为 MySQL 源代码中的一个例子，用来演示如何开始编写一个新存储引擎。同样，它的主要兴趣是对开发者。EXAMPLE 存储引擎不支持编索引。

　　同一个数据库也可以使用多种存储引擎的表。如果一个表要求比较高的事务处理，可以选择InnoDB。这个数据库中可以将查询要求比较高的表选择MyISAM存储。如果该数据库需要一个用于查询的临时表，可以选择MEMORY存储引擎。