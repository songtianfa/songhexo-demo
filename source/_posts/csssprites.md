---
title: 精灵图的使用
date: 2019-09-15 20:25:07
categories:
- 前端
tags:
- css
---
<p>　　在前端的页面中，网页上面的每张图片都要经历一次请求才能展示给用户，小的图标频繁的请求服务器，降低页面的加载速度，难免会用到许多的图片，如果每一个位置的图片都需要一张张的图片，那样不仅会占用大量的空间，而且会降低网页的速度。为了有效地减少服务器接收和发送请求的次数，提高页面的加载速度，因此，产生了css精灵技术。</p>
<p>　　css精灵图(sprite)(也叫雪碧图等)就是一种网页图片应用处理方式，它允许将一个页面涉及到的所有零星图片都包含到一张大图中。使用雪碧图的处理方式可以实现两个优点：</p>
<p>　　【1】减少http请求次数</p>
<p>　　【2】减少图片大小，提升网页加载速度 (多张图片加载速度小于拼合成的图片的加载速度)</p>
<p>　　应用方面：</p>
<p>　　【1】静态图片，不随用户信息的变化而变化(通常在网站上以常态的形式存在)。</p>
<p>　　【2】小图片，图片容积比较小。</p>
<p>　　【3】对于img标签设置的内容性图片，是不能合并到雪碧图的，如果合并这些图片会影响页面可读性，语义化降低且可调整的范围小。</p>
<p>　　【4】对于横向和纵向都平铺的图片，也不能合并到雪碧图中。如果是横向平铺，只能将所有横向平铺的图合并成一张大图，只能竖直排列，不能水平排列;如果是纵向平铺，只能将所有纵向平铺的图合并成一张大图，只能水平排列，不能竖直排列。</p>
<p>&nbsp; &nbsp; &nbsp; &nbsp;这是精灵图：</p>
<p><img src="https://img2018.cnblogs.com/blog/1740594/201907/1740594-20190718120151820-1260102185.png" alt="" /></p>
<p>&nbsp; &nbsp; &nbsp; &nbsp;HTML代码：</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">&lt;!</span><span style="color: #ff00ff;">DOCTYPE html</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">html </span><span style="color: #ff0000;">lang</span><span style="color: #0000ff;">="en"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">meta </span><span style="color: #ff0000;">charset</span><span style="color: #0000ff;">="UTF-8"</span><span style="color: #0000ff;">&gt;</span>
    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>Document<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">title</span><span style="color: #0000ff;">&gt;</span>
    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">link </span><span style="color: #ff0000;">rel</span><span style="color: #0000ff;">="stylesheet"</span><span style="color: #ff0000;"> href</span><span style="color: #0000ff;">="index.css"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">body</span><span style="color: #0000ff;">&gt;</span>
    <span style="color: #008000;">&lt;!--</span><span style="color: #008000;"> S= 页面的顶部 </span><span style="color: #008000;">--&gt;</span>
    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="top"</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="top_page"</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="top_page_l fl"</span><span style="color: #0000ff;">&gt;</span>您好！欢迎来到建材网！<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="top_page_r fr"</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">ul</span><span style="color: #0000ff;">&gt;</span>
                    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>建材网首页<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
                    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>我的商务室<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
                    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>我的收藏<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
                    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>建材服务<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
                    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>客服中心<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
                    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>网站导航<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">ul</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
    <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
    <span style="color: #008000;">&lt;!--</span><span style="color: #008000;"> E= 页面的顶部 </span><span style="color: #008000;">--&gt;</span>
    <span style="color: #008000;">&lt;!--</span><span style="color: #008000;"> S= logo </span><span style="color: #008000;">--&gt;</span>
    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="logo"</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">h1 </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="logo_l fl"</span><span style="color: #0000ff;">&gt;</span>梅兰商贸<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">h1</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="logo_r fr"</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="logo_r_content"</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">input </span><span style="color: #ff0000;">type</span><span style="color: #0000ff;">="input"</span><span style="color: #ff0000;"> class</span><span style="color: #0000ff;">="logo_r_searche fl"</span><span style="color: #ff0000;"> value</span><span style="color: #0000ff;">="请输入关键字"</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">input </span><span style="color: #ff0000;">type</span><span style="color: #0000ff;">="button"</span><span style="color: #ff0000;"> value </span><span style="color: #0000ff;">= "搜索"</span><span style="color: #ff0000;"> class</span><span style="color: #0000ff;">="logo_r_btn fl"</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
    <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
    <span style="color: #008000;">&lt;!--</span><span style="color: #008000;"> E= logo </span><span style="color: #008000;">--&gt;</span>
    <span style="color: #008000;">&lt;!--</span><span style="color: #008000;"> S=导航 </span><span style="color: #008000;">--&gt;</span>
    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="nav"</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">ul</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>首页<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>建筑材料<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>儿童安全座椅<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>工艺美术品<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">ul</span><span style="color: #0000ff;">&gt;</span>
    <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
    <span style="color: #008000;">&lt;!--</span><span style="color: #008000;"> E=导航 </span><span style="color: #008000;">--&gt;</span>
    
    <span style="color: #008000;">&lt;!--</span><span style="color: #008000;"> S= banner </span><span style="color: #008000;">--&gt;</span>
    <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="banner"</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="subNav fl"</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">h2</span><span style="color: #0000ff;">&gt;</span>商机市场<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">h2</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">ul</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>建筑材料<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>儿童安全座椅<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>工艺美术品<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>建筑材料<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>儿童安全座椅<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>工艺美术品<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">li</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">ul</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="ad fl"</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="message fr"</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="message_top"</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">p </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="fw"</span><span style="color: #0000ff;">&gt;</span>建材通大众版<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">p</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">s </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="fl"</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">p </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="cheap fl"</span><span style="color: #0000ff;">&gt;</span>价格实惠，量身为预算不<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">br</span><span style="color: #0000ff;">/&gt;</span>多的供应商所设。<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">a </span><span style="color: #ff0000;">href</span><span style="color: #0000ff;">="#"</span><span style="color: #0000ff;">&gt;</span>了解详情<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">a</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">p</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">div </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="message_bottom"</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">p </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="findMessage"</span><span style="color: #0000ff;">&gt;</span>找信息或者发信息遇到问题？<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">p</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">p </span><span style="color: #ff0000;">class</span><span style="color: #0000ff;">="phone"</span><span style="color: #0000ff;">&gt;&lt;</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">s</span><span style="color: #0000ff;">&gt;</span>0124-9792374987<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">p</span><span style="color: #0000ff;">&gt;</span>
                <span style="color: #0000ff;">&lt;</span><span style="color: #800000;">input </span><span style="color: #ff0000;">type</span><span style="color: #0000ff;">="button"</span><span style="color: #ff0000;"> class</span><span style="color: #0000ff;">="btn"</span> <span style="color: #0000ff;">&gt;</span>
            <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
        <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
    <span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">div</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">body</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">html</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p>&nbsp; &nbsp; &nbsp; CSS代码：</p>
<div class="cnblogs_code">
<pre><span style="color: #000000;">@charset "utf-8";
*{margin:0;padding:0;}
ul li{list-style:none;}
    a{underline:none;}
.fl {
    float: left;
}
.fr {
    float: right;
}
html{
    font: 12px '宋体';
}
a {
    color: #000;
}
.top {
    background-color: #F7F7F7;
    height: 26px;
    border-bottom: 1px solid #D8D8D8;
}
.top_page {
    width:  970px;
    height: 26px;
    margin: 0 auto;
}
.top_page_l {
    line-height: 26px;
}
.top_page_r ul li {
    line-height: 26px;
    float: left;
    padding-right: 10px;
}
.top_page_r ul li s {
    width: 14px;
    height: 12px;
    background: url(sprite.png);
    display: inline-block;
    vertical-align: middle;
}
.logo {
    width: 970px;
    height: 98px;
    margin: 0 auto;
}
.logo_l {
    width: 200px;
    height: 55px;
    margin: 24px 0 19px 9px;
    background: url(sprite.png) -20px 0;
    text-indent: -1000em;
}
.logo_r {
    width: 530px;
    height: 42px;
    border: 1px solid #C9C9C9;
    margin-top: 29px;
}
.logo_r_content{
    margin: 5px 5px 5px 4px;
}
.logo_r_searche {
    width: 418px;
    height: 28px;
    border: 1px solid #C9C9C9;
    color:#999999;
}
.logo_r_btn {
    width: 99px;
    height: 30px;
    color: white;
    background-color: #2F70D0;
}

.nav {
    width: 970px;
    height: 25px;
    margin: 0 auto;
    border-bottom: 2px solid #0266A3;
}
.nav li {
    padding: 0 15px 0 15px;
    font-size: 14px;
    line-height: 26px;
    float: left;
    font-weight: bold;
}
.nav li a {
    color: #0266A3;
}
.nav li:hover {
    background-color: #0266A3;
}
.nav li:hover a{
    color: white;
}

.banner {
    width: 970px;
    height: 210px;
    margin: 0 auto;
    margin-top: 10px;
}
.subNav {
    width: 200px;
    height: 210px;
    margin-right: 11px;
}
.ad {
    width: 520px;
    height: 210px;
    background-color: yellow;
}
.message {
    width: 230px;
    height: 210px;
}
.subNav h2 {
    padding-left: 20px;
    height: 30px;
    line-height: 30px;
    font-size: 14px;
    font-weight: bold;
    background-color: #0266A3;
    color: white;
}
.subNav ul {
    background: #EBF0F6;
    height: 180px;
}
.subNav s {
    display: inline-block;
    width: 15px;
    height: 13px;
    background: url(sprite.png) -225px 0;
    vertical-align: middle;
}
.subNav li {
    font-size: 15px;
    padding-top: 11px;
    margin-left: 9px;
}
.subNav li a {
    padding-left: 15px;
}
.message_top {
    height: 95px;
    border: 1px solid #DDDDDD;
    background: #F7FAFF;
    margin-bottom: 21px;
}
.message_top s {
    display: inline-block;
    width: 40px;
    height: 40px;
    background: url(sprite.png) -250px 0 ;
    margin: 20px 10px 0 10px;
}
.message_top .fw {
    padding: 7px 0 0 18px;
    font-weight: bold;
}
.message_top .cheap {
    margin-top: 25px;
}
.message_bottom {
    height: 92px;
    background: #F7F7F7;
}
.message_bottom .findMessage {
    text-align: center;
    font-size: 14px;
    padding-top: 11px;
}
.message_bottom .phone {
    margin-top: 10px;
    text-align: center;
    color: #3F9CE0;
}
.message_bottom .phone s {
    display: inline-block;
    width: 14px;
    height: 17px;
    background: url(sprite.png) -225px -30px;
    vertical-align: middle;
}
.message_bottom .btn {
    width: 81px;
    height: 23px;
    background: url(sprite.png) -295px 0;
    margin-top: 9px;
    margin-left: 75px;
}</span></pre>
</div>
<p>&nbsp; &nbsp; &nbsp; 效果图（选中都是精灵图的实现效果，全都是上面图片的展示出来）：</p>
<p><img src="https://img2018.cnblogs.com/blog/1740594/201907/1740594-20190718120705976-1751654011.jpg" alt="精灵图的使用" /></p>
<p>　　使用到的核心代码：background-image: url(sprite.png);---为sprites里的设置背景图像，引用了精灵图(sprite.png);background-position 属性---这是最关键的代码，图片定位,定位选择图片的位置，属性才可使用，所以图片大小，各个图片的位置要保存好一定的位置，可以使用Fireworks实现，通过一定的规则(间隙，间距，行高的等)整合到一张大的图片里，然后再通过CSS样式中&ldquo;background-image&rdquo;，&ldquo;background- repeat&rdquo;，&ldquo;background-position&rdquo;等基本样式进行处理，以便运用到网页中所需要的位置上。</p>