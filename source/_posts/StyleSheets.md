---
title: css样式引入
date: 2019-09-17 19:09:26
categories:
- 前端
tags:
- html
- css
---
<p>　　首选来介绍一下什么是CSS?(英文全称：Cascading Style Sheets)是一种用来表现HTML(标准通用标记语言的一个应用)或XML(标准通用标记语言的一个子集)等文件样式的计算机语言,其实就是一种层叠样式表。</p>
<p>　　CSS不仅可以静态地修饰网页，还可以配合各种脚本语言动态地对网页各元素进行格式化。CSS能够对网页中元素位置的排版进行像素级精确控制，支持几乎所有的字体字号样式，拥有对网页对象和模型样式编辑的能力。</p>
<p>　　就像造房子一样，如果html是基地的话，那么CSS就是装修，只有装修的房子才可以住，自然至于那些灯光之类的是JS了，这是简单的比例，但也说明了css的重要性。</p>
<p>　　网页的核心就是内容与样式的分离，其中CSS就是分离的一种，那么如果分离了，该如何引用呢?一些网站中很多文件，只有相关的引用才可以实现，其中有四种方式，<strong>内链样式</strong>，<strong>嵌入式样式</strong>，<strong>外部样式</strong>，<strong>导入样式</strong>，下面为大家介绍一下：</p>
<p>　<span style="color: #ff0000;">　1：内联样式(行间样式)：<span style="color: #000000;">在标签的style属性添加样式：</span></span></p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">&lt;!</span><span style="color: #ff00ff;">DOCTYPE</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">html</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
  <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">meta </span><span style="color: #ff0000;">charset</span><span style="color: #0000ff;">="utf-8"</span> <span style="color: #0000ff;">/&gt;</span>
  <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>行内样式<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">body</span><span style="color: #0000ff;">&gt;</span>
     <span style="color: #008000;">&lt;!--</span><span style="color: #008000;">使用行内样式引入CSS</span><span style="color: #008000;">--&gt;</span>
     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">h1 </span><span style="color: #ff0000;">style</span><span style="color: #0000ff;">="color:red;"</span><span style="color: #0000ff;">&gt;</span>惊风随笔<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">h1</span><span style="color: #0000ff;">&gt;</span>
     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">p </span><span style="color: #ff0000;">style</span><span style="color: #0000ff;">="color:red;font-size:30px;"</span><span style="color: #0000ff;">&gt;</span>惊风随笔<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">p</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">body</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">html</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p><span style="color: #ff0000;">　　2、嵌入式样式表(内部样式表)：<span style="color: #000000;">在style标签内添加(加在head标签内部)</span></span></p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">&lt;</span><span style="color: #800000;">html</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
  <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">meta </span><span style="color: #ff0000;">charset</span><span style="color: #0000ff;">="utf-8"</span> <span style="color: #0000ff;">/&gt;</span>
  <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>内部样式表<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>
  <span style="color: #008000;">&lt;!--</span><span style="color: #008000;">使用内部样式表引入CSS</span><span style="color: #008000;">--&gt;</span>
  <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">style </span><span style="color: #ff0000;">type</span><span style="color: #0000ff;">="text/css"</span><span style="color: #0000ff;">&gt;</span><span style="background-color: #f5f5f5; color: #800000;">
    div</span><span style="background-color: #f5f5f5; color: #000000;">{</span><span style="background-color: #f5f5f5; color: #ff0000;">
        background</span><span style="background-color: #f5f5f5; color: #000000;">:</span><span style="background-color: #f5f5f5; color: #0000ff;"> green</span><span style="background-color: #f5f5f5; color: #000000;">;</span>
    <span style="background-color: #f5f5f5; color: #000000;">}</span>
  <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">style</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">body</span><span style="color: #0000ff;">&gt;</span>
     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>我是DIV<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">body</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">html</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p><span style="color: #ff0000;">　　3.外部样式表：<span style="color: #000000;">将css样式编写在扩展名为.css的文件中，再导入样式，导入在(head标签内部)</span></span></p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">&lt;!</span><span style="color: #ff00ff;">DOCTYPE</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">html</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
  <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">meta </span><span style="color: #ff0000;">charset</span><span style="color: #0000ff;">="utf-8"</span> <span style="color: #0000ff;">/&gt;</span>
  <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>外部样式表<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>
  <span style="color: #008000;">&lt;!--</span><span style="color: #008000;">链接式:推荐使用</span><span style="color: #008000;">--&gt;</span>
  <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">link </span><span style="color: #ff0000;">rel</span><span style="color: #0000ff;">="stylesheet"</span><span style="color: #ff0000;"> type</span><span style="color: #0000ff;">="text/css"</span><span style="color: #ff0000;"> href</span><span style="color: #0000ff;">="css/style.css"</span> <span style="color: #0000ff;">/&gt;</span> 
  <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">style</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">body</span><span style="color: #0000ff;">&gt;</span>
     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">ul</span><span style="color: #0000ff;">&gt;</span>
         <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>HTML<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
         <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>CSS<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>JavaScript<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
     <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">ul</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">html</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p><span style="color: #ff0000;">　　4、@import导入其他css文件。<span style="color: #000000;">就相当于原来的css文件中包含被导入的css文件中的样式。</span></span></p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">&lt;!</span><span style="color: #ff00ff;">DOCTYPE</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">html</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
  <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">meta </span><span style="color: #ff0000;">charset</span><span style="color: #0000ff;">="utf-8"</span> <span style="color: #0000ff;">/&gt;</span>
  <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>导入样式表<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>
  <span style="color: #008000;">&lt;!--</span><span style="color: #008000;">导入式-不推荐使用</span><span style="color: #008000;">--&gt;</span>
  <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">style </span><span style="color: #ff0000;">type</span><span style="color: #0000ff;">="text/css"</span><span style="color: #0000ff;">&gt;</span><span style="background-color: #f5f5f5; color: #800000;">
    @import url("css/style.css");
  </span><span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">style</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">body</span><span style="color: #0000ff;">&gt;</span>
     <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">ul</span><span style="color: #0000ff;">&gt;</span>
         <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>HTML<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
         <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>CSS<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
         <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>JavaScript<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
     <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">ul</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">html</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p>　　不过根据目前网站的做做法，要做到内容与样式的分离，一般都是使用第三种的做法，也就是使用外部式表。这是通用的方式了，第四种一般很少用，因为需要进一步的加载，不利于后期SEO的优化。</p>