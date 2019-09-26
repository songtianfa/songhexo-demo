---
title: bootstrap环境搭建
date: 2019-09-15 14:32:08
categories:
- 前端
tags:
- bootstrap
- 前端框架
---
<p>　　Bootstrap 是stwitter公司的两名前端设计师设计的<span style="color: #ff0000;">基于html css javascript的超强的前端框架。</span></p>
<p>　　Bootstrap 是一移动设备为优先，pc机，平板，手机皆适用的框架。</p>
<p>　　那么如何引入bootstrap呢?主要有两种方式(文档要求必须是 html5)：</p>
<p>　　<strong>一：引入bootstrap环境：</strong></p>
<div class="cnblogs_code">
<pre><span style="color: #008080;"> 1</span> <span style="color: #0000ff;">&lt;!</span><span style="color: #ff00ff;">DOCTYPE html</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;"> 2</span> <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">html </span><span style="color: #ff0000;">lang</span><span style="color: #0000ff;">="zh-cn"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;"> 3</span> <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;"> 4</span>     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">meta </span><span style="color: #ff0000;">charset</span><span style="color: #0000ff;">="UTF-8"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;"> 5</span>     <span style="color: #008000;">&lt;!--</span><span style="color: #008000;">屏幕和设备的屏幕一致，初始缩放为1:1，禁止用户缩放</span><span style="color: #008000;">--&gt;</span>
<span style="color: #008080;"> 6</span>     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">meta </span><span style="color: #ff0000;">name</span><span style="color: #0000ff;">="viewport"</span><span style="color: #ff0000;"> content</span><span style="color: #0000ff;">="width=device-width,initial-scale=1,user-scalable=no"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;"> 7</span>     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>bootstrap环境搭建<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;"> 8</span>     <span style="color: #008000;">&lt;!--</span><span style="color: #008000;">引入外部的bootstrap中的css文件</span><span style="color: #008000;">--&gt;</span>
<span style="color: #008080;"> 9</span>     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">link </span><span style="color: #ff0000;">rel</span><span style="color: #0000ff;">="stylesheet"</span><span style="color: #ff0000;"> href</span><span style="color: #0000ff;">="bootstrap/css/bootstrap.min.css"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;">10</span>     <span style="color: #008000;">&lt;!--</span><span style="color: #008000;"> jQuery文件。务必在bootstrap.min.js 之前引入 </span><span style="color: #008000;">--&gt;</span>
<span style="color: #008080;">11</span>     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script </span><span style="color: #ff0000;">src</span><span style="color: #0000ff;">="bootstrap/js/jquery.min.js"</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;">12</span>     <span style="color: #008000;">&lt;!--</span><span style="color: #008000;">再引入bootstrap.min.js文件</span><span style="color: #008000;">--&gt;</span>
<span style="color: #008080;">13</span>     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script </span><span style="color: #ff0000;">src</span><span style="color: #0000ff;">="bootstrap/js/bootstrap.min.js"</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;">14</span> <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;">15</span>      <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">body </span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;">16</span>        <span style="color: #008000;">&lt;!--</span><span style="color: #008000;">内容区</span><span style="color: #008000;">--&gt;</span>
<span style="color: #008080;">17</span>       <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">body</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;">18</span> <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">html</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p><strong>　　二：使用外部的bootstrap环境：</strong></p>
<div class="cnblogs_code">
<pre><span style="color: #008080;"> 1</span> <span style="color: #0000ff;">&lt;!</span><span style="color: #ff00ff;">DOCTYPE html</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;"> 2</span> <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">html </span><span style="color: #ff0000;">lang</span><span style="color: #0000ff;">="en"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;"> 3</span> <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;"> 4</span>     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">meta </span><span style="color: #ff0000;">charset</span><span style="color: #0000ff;">="UTF-8"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;"> 5</span>     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>Bootstrap环境搭建<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;"> 6</span>      <span style="color: #008000;">&lt;!--</span><span style="color: #008000;"> 新 Bootstrap 核心 CSS 文件 </span><span style="color: #008000;">--&gt;</span>
<span style="color: #008080;"> 7</span>     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">link </span><span style="color: #ff0000;">rel</span><span style="color: #0000ff;">="stylesheet"</span><span style="color: #ff0000;"> href</span><span style="color: #0000ff;">="//cdn.bootcss.com/bootstrap/3.3.5/css/bootstrap.min.css"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;"> 8</span>     <span style="color: #008000;">&lt;!--</span><span style="color: #008000;"> 可选的Bootstrap主题文件（一般不用引入） </span><span style="color: #008000;">--&gt;</span>
<span style="color: #008080;"> 9</span>     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">link </span><span style="color: #ff0000;">rel</span><span style="color: #0000ff;">="stylesheet"</span><span style="color: #ff0000;"> href</span><span style="color: #0000ff;">="//cdn.bootcss.com/bootstrap/3.3.5/css/bootstrap-theme.min.css"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;">10</span>     <span style="color: #008000;">&lt;!--</span><span style="color: #008000;"> jQuery文件。务必在bootstrap.min.js 之前引入 </span><span style="color: #008000;">--&gt;</span>
<span style="color: #008080;">11</span>     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script </span><span style="color: #ff0000;">src</span><span style="color: #0000ff;">="//cdn.bootcss.com/jquery/1.11.3/jquery.min.js"</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;">12</span>     <span style="color: #008000;">&lt;!--</span><span style="color: #008000;"> 最新的 Bootstrap 核心 JavaScript 文件 </span><span style="color: #008000;">--&gt;</span>
<span style="color: #008080;">13</span>     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script </span><span style="color: #ff0000;">src</span><span style="color: #0000ff;">="//cdn.bootcss.com/bootstrap/3.3.5/js/bootstrap.min.js"</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;">14</span> <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;">15</span>       <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">body</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;">16</span>        <span style="color: #008000;">&lt;!--</span><span style="color: #008000;">内容区</span><span style="color: #008000;">--&gt;</span>
<span style="color: #008080;">17</span>       <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">body</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #008080;">18</span> <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">html</span><span style="color: #0000ff;">&gt;</span></pre>
</div>