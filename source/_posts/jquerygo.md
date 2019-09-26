---
title: jquery搭建
date: 2019-09-11 24:44:50
categories:
- 前端
tags:
- jquery
- 前端框架
---
<p>　　description</p>
<p>　　jQuery，顾名思义，<span style="color: #ff0000;">也就是JavaScript和Query(查询)，即辅助JavaScript开发的库。jQuery是一个快速、简洁的JavaScript框架</span>，是继Prototype之后又一个优秀的JavaScript代码库(或JavaScript框架)。jQuery设计的<span style="color: #ff0000;">宗旨是&ldquo;write Less，Do More&rdquo;</span>，即倡导写更少的代码，做更多的事情。<span style="color: #ff0000;">它封装JavaScript常用的功能代码，提供一种简便的JavaScript设计模式，优化HTML文档操作、事件处理、动画设计和Ajax交互，jQuery的理念就是&ldquo;write less do more&rdquo;。</span></p>
<p>　　jQuery库文件有2个版本，分别是1.x版本和2.x版本。但是<span style="color: #ff0000;">1.x版本支持IE6、IE7和IE8，而2.x则不再支持，</span>目前依旧有很多人在使用的6/7/8等的版本，市场依旧很大，所以最新的版本不一定是最好的，所以建议使用1.x版本的，jQuery库文件其实有2种类型：(1)开发版;(2)发布版。开发版是没有经过压缩的，供给我们学习jQuery的源码使用，一般用jquery.js命名。而发布版是经过压缩的，供给我们使用jQuery，一般用jquery.min.js命名，我们开发用的一般都是压缩的版本。</p>
<p>　　那么该如何安装jQuery呢?其实很简单，跟CSS的引入是一样的，只是自己的写的jq的代码必须写在引入源码的下面才会有效，否则是无效的，必须是这种模式：</p>
<div class="cnblogs_code">
<pre><span style="color: #008000;">&lt;!--</span><span style="color: #008000;">jQuery库</span><span style="color: #008000;">--&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script </span><span style="color: #ff0000;">type</span><span style="color: #0000ff;">="text/javascript"</span><span style="color: #ff0000;"> src</span><span style="color: #0000ff;">="jquery-1.11.3.min.js"</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script  </span><span style="color: #ff0000;">type</span><span style="color: #0000ff;">="text/javascript"</span><span style="color: #0000ff;">&gt;</span>
    <span style="background-color: #f5f5f5; color: #008000;">//</span><span style="background-color: #f5f5f5; color: #008000;">这里编写你的jQuery代码</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p>　　其实还有其他的方式引入，这种方式也很多人用，就是直接引入，主要有以下几个方式：Staticfile CDN、又拍云、新浪、谷歌或微软引用 jQuery</p>
<p>　　Staticfile CDN:</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">&lt;</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script </span><span style="color: #ff0000;">src</span><span style="color: #0000ff;">="https://cdn.staticfile.org/jquery/1.10.2/jquery.min.js"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p>　　又拍云 CDN:</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">&lt;</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script </span><span style="color: #ff0000;">src</span><span style="color: #0000ff;">="https://upcdn.b0.upaiyun.com/libs/jquery/jquery-2.0.2.min.js"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p>　　百度 CDN：</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">&lt;</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script </span><span style="color: #ff0000;">src</span><span style="color: #0000ff;">="https://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p>　　新浪 CDN:</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">&lt;</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script </span><span style="color: #ff0000;">src</span><span style="color: #0000ff;">="https://lib.sinaapp.com/js/jquery/2.0.2/jquery-2.0.2.min.js"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p>　　Google CDN:</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">&lt;</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script </span><span style="color: #ff0000;">src</span><span style="color: #0000ff;">="https://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span>
<span style="color: #0000ff;">&lt;/</span><span style="color: #800000;">head</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p>　　这些方式的引入会从缓存中加载 jQuery，这样可以减少加载时间。同时，大多数 CDN 都可以确保当用户向其请求文件时，会从离用户最近的服务器上返回响应，这样也可以提高加载速度。</p>