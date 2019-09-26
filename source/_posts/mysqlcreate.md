---
title: mysql建表常用命令
date: 2019-09-10 14:51:38
categories:
- 数据库
tags:
- mysql
---
<p>　　MySQL是一个关系型数据库管理系统，由瑞典MySQL AB 公司开发，目前属于 Oracle 旗下产品。MySQL 是最流行的关系型数据库管理系统之一，在 WEB 应用方面，MySQL是最好的 RDBMS (Relational Database Management System，关系数据库管理系统) 应用软件之一。</p>
<p>　　MySQL是一种关系数据库管理系统，关系数据库将数据保存在不同的表中，而不是将所有数据放在一个大仓库内，这样就增加了速度并提高了灵活性。</p>
<p>　　这里为大家介绍一下mysql在建表过程中经常用到的命令：</p>
<p>　　修改表名：rename table 原表名 to 现表名;</p>
<p>　　增加表的一列：alter table 表名 add 列名 列名类型;</p>
<p>　　修改表的一列：alter table 表名 change 原列名 现列名 类型</p>
<p>　　修改表的字符集 alter table 表名 character set utf8</p>
<p>　　修改表的一个字段类型 alter table 表名 MODIFY age int;</p>
<p>　　查看表的创建细节：show create table 表名</p>
<p>　　删除一列：alter table 表名 drop 字段</p>
<p>　　删除表：drop table 表名</p>
<p>　　创建数据表：</p>
<p>　　先进入一个数据库，然后创建表：</p>
<p>　　create table (表名)(</p>
<p>　　列名1 列类型 [约束],</p>
<p>　　列名2 列类型 [约束],</p>
<p>　　...</p>
<p>　　列名n 列类型 [约束]</p>
<p>　　);</p>
<p>　　如：</p>
<p>　　create table song(</p>
<p>　　id bigint，</p>
<p>　　name varchar(20),</p>
<p>　　age int</p>
<p>　　);</p>
<p>　　代码例子：</p>
<div class="cnblogs_code">
<pre><span style="color: #008080;"> 1</span> <span style="color: #008000;">/*</span><span style="color: #008000;">创建表</span><span style="color: #008000;">*/</span>
<span style="color: #008080;"> 2</span> <span style="color: #000000;">create table stu(</span>
<span style="color: #008080;"> 4</span>     id  int unsigned NOT <span style="color: #0000ff;">NULL</span> PRIMARY <span style="color: #008080;">KEY</span>,
<span style="color: #008080;"> 5</span>     name VARCHAR(20) NOT <span style="color: #0000ff;">NULL</span> <span style="color: #0000ff;">DEFAULT</span> '0',
<span style="color: #008080;"> 6</span>     age int unsigned NOT <span style="color: #0000ff;">NULL</span> <span style="color: #0000ff;">DEFAULT</span> '0'
<span style="color: #008080;"> 7</span> <span style="color: #000000;">);
</span><span style="color: #008080;"> 8</span> 
<span style="color: #008080;">10</span> <span style="color: #008000;">/*</span><span style="color: #008000;">查看表的结构</span><span style="color: #008000;">*/</span>
<span style="color: #008080;">11</span> <span style="color: #000000;">desc stu;
</span><span style="color: #008080;">12</span> 
<span style="color: #008080;">13</span> <span style="color: #008000;">/*</span><span style="color: #008000;">修改表名</span><span style="color: #008000;">*/</span>
<span style="color: #008080;">14</span> <span style="color: #008080;">rename</span><span style="color: #000000;"> table stu to xuesheng;
</span><span style="color: #008080;">15</span> 
<span style="color: #008080;">16</span> <span style="color: #008000;">/*</span><span style="color: #008000;">添加一列</span><span style="color: #008000;">*/</span>
<span style="color: #008080;">17</span> alter table xuesheng add sex varchar(20<span style="color: #000000;">)
</span><span style="color: #008080;">18</span> 
<span style="color: #008080;">19</span> <span style="color: #008000;">/*</span><span style="color: #008000;">修改表的列名</span><span style="color: #008000;">*/</span>
<span style="color: #008080;">20</span> alter table xuesheng change sex  sexual VARCHAR(20<span style="color: #000000;">)
</span><span style="color: #008080;">21</span> 
<span style="color: #008080;">22</span> <span style="color: #008000;">/*</span><span style="color: #008000;">修改表的一个字段类型</span><span style="color: #008000;">*/</span>
<span style="color: #008080;">23</span> <span style="color: #000000;">alter table xuesheng MODIFY age int;
</span><span style="color: #008080;">24</span> 
<span style="color: #008080;">25</span> <span style="color: #008000;">/*</span><span style="color: #008000;">修改表的字符集为utf8</span><span style="color: #008000;">*/</span>
<span style="color: #008080;">26</span> <span style="color: #000000;">alter table xuesheng character set utf8
</span><span style="color: #008080;">27</span> 
<span style="color: #008080;">28</span> <span style="color: #000000;">create table zhujian1 (
</span><span style="color: #008080;">29</span>   uid int PRIMARY <span style="color: #008080;">KEY</span>, <span style="color: #008000;">/*</span><span style="color: #008000;"> 设置主键 </span><span style="color: #008000;">*/</span>
<span style="color: #008080;">30</span>   xingming  varchar(20) not <span style="color: #0000ff;">null</span> <span style="color: #0000ff;">DEFAULT</span> '',  <span style="color: #008000;">/*</span><span style="color: #008000;"> 不为null </span><span style="color: #008000;">*/</span>
<span style="color: #008080;">31</span>    age varchar(20) not <span style="color: #0000ff;">null</span> <span style="color: #0000ff;">default</span> '' <span style="color: #008000;">/*</span><span style="color: #008000;"> 不为null </span><span style="color: #008000;">*/</span>
<span style="color: #008080;">32</span> <span style="color: #000000;">);
</span><span style="color: #008080;">33</span> 
<span style="color: #008080;">34</span> 
<span style="color: #008080;">35</span> <span style="color: #008000;">/*</span><span style="color: #008000;">创建表</span><span style="color: #008000;">*/</span>
<span style="color: #008080;">36</span> <span style="color: #000000;">create table zhujian3 (
</span><span style="color: #008080;">37</span>   uid int PRIMARY <span style="color: #008080;">KEY</span>  AUTO_INCREMENT,  <span style="color: #008000;">/*</span><span style="color: #008000;"> 设置主键，自增 </span><span style="color: #008000;">*/</span>
<span style="color: #008080;">38</span>   xingming  varchar(20) not <span style="color: #0000ff;">null</span> <span style="color: #0000ff;">DEFAULT</span> '',  <span style="color: #008000;">/*</span><span style="color: #008000;"> 不为null </span><span style="color: #008000;">*/</span>
<span style="color: #008080;">39</span>    age varchar(20) not <span style="color: #0000ff;">null</span> <span style="color: #0000ff;">default</span> ''   <span style="color: #008000;">/*</span><span style="color: #008000;"> 不为null </span><span style="color: #008000;">*/</span>
<span style="color: #008080;">40</span> <span style="color: #000000;">)
</span><span style="color: #008080;">41</span> 
<span style="color: #008080;">42</span> ENGINE=InnoDB <span style="color: #0000ff;">DEFAULT</span> CHARSET=<span style="color: #000000;">utf8;
</span><span style="color: #008080;">43</span> 
<span style="color: #008080;">44</span> 
<span style="color: #008080;">45</span> <span style="color: #000000;">create table good1s (
</span><span style="color: #008080;">46</span>    goods_id int PRIMARY <span style="color: #008080;">KEY</span> AUTO_INCREMENT,
<span style="color: #008080;">47</span>    goods_name varchar(30) not <span style="color: #0000ff;">null</span> <span style="color: #0000ff;">DEFAULT</span> '0',
<span style="color: #008080;">48</span>    goods_number int not <span style="color: #0000ff;">null</span> <span style="color: #0000ff;">DEFAULT</span> '0',
<span style="color: #008080;">49</span>    shop_price varchar(30) not <span style="color: #0000ff;">null</span> <span style="color: #0000ff;">DEFAULT</span> '0',
<span style="color: #008080;">50</span>    market_price varchar(30) not <span style="color: #0000ff;">null</span> <span style="color: #0000ff;">DEFAULT</span> '0',
<span style="color: #008080;">51</span>    click_count bigint  not <span style="color: #0000ff;">null</span> <span style="color: #0000ff;">DEFAULT</span> '0'
<span style="color: #008080;">52</span> <span style="color: #000000;">)
</span><span style="color: #008080;">53</span> ENGINE=InnoDB <span style="color: #0000ff;">DEFAULT</span> CHARSET=utf8;</pre>
</div>
<p>　　MySQL所使用的 SQL 语言是用于访问数据库的最常用标准化语言。MySQL 软件采用了双授权政策，分为社区版和商业版，由于其体积小、速度快、总体拥有成本低，尤其是开放源码这一特点，一般中小型网站的开发都选择 MySQL 作为网站数据库。</p>