---
title: meta大全
date: 2019-09-09 08:25:15
categories:
- 前端
tags:
- html
- css
---
　　meta是html文档在head标签里定义的一个对文档进行描述的功能性标签。

　　它并不是一个可以显示在网页的标签属性，但对于整个网页来说却是至关重要的，特别是对于SEO优化来说更是如此，它描述了作者、日期和时间、网页描述、关键词、页面刷新等相关信息，在有关搜索引擎注册、搜索引擎优化排名等网络营销方法内容中，通常都要谈论meta标签的作用，合理利用meta标签的description和keywords属性，加入网站关键词或者网页的关键字信息，可使网站更加贴近用户体验。

　　meta标签主要有下面的作用：

　　1.搜索引擎优化（SEO）

　　2.定义页面使用语言

　　3.自动刷新并指向新的页面

　　4.实现网页转换时的动态效果

　　5.控制页面缓冲

　　6.网页定级评价

　　7.控制网页显示的窗口

　　META标签可分为两大部分：HTTP-EQUIV和NAME变量。

　　HTTP实例

　　HTML代码实例中有一项内容是

　　<meta http-equiv="Content-Type"content="text/html;charset=gb2312">

　　其作用是指定了当前文档所使用的字符编码为gb2312，也就是中文简体字符。根据这一行代码，浏览器就可以识别出这个网页应该用中文简体字符显示。类似地，如果将"gb2312"换为"big5"，就是我们熟知的中文繁体字符了。

　　HTTP使用方法

      <meta http-equiv="Content-Type"content="text/html;charset=gb_2312-80">
       <meta http-equiv="Content-Language"content="zh-CN">
      <!-- 用以说明主页制作所使用的文字以及语言；又如英文是ISO-8859-1字符集，还有BIG5、utf-8、shift-Jis、Euc、Koi8-2等字符集； -->
      <meta http-equiv="Refresh"content="n;url=http://yourlink">
      <!-- 定时让网页在指定的时间n内，跳转到你的页面； -->
     <meta http-equiv="Expires"content="Mon,12May200100:20:00GMT">
     <!-- 可以用于设定网页的到期时间，一旦过期则必须到服务器上重新调用。需要注意的是必须使用GMT时间格式； -->
　　  <meta http-equiv="Pragma"content="no-cache">
     <!-- 是用于设定禁止浏览器从本地机的缓存中调阅页面内容，设定后一旦离开网页就无法从Cache中再调出； -->
　　  <meta http-equiv="set-cookie"content="Mon,12May200100:20:00GMT">
     <!--cookie设定，如果网页过期，存盘的cookie将被删除。需要注意的也是必须使用GMT时间格式； -->
　　 <meta http-equiv="Pics-label"content="">
     <!-- 网页等级评定，在IE的internet选项中有一项内容设置，可以防止浏览一些受限制的网站，而网站的限制级别就是通过meta属性来设置的； -->
　   <meta http-equiv="windows-Target"content="_top">
    <!-- 强制页面在当前窗口中以独立页面显示，可以防止自己的网页被别人当作一个frame页调用； -->
    <meta http-equiv="Page-Enter"content="revealTrans（duration=10,transition=50）">
    <meta http-equiv="Page-Exit"content="revealTrans（duration=20，transition=6）">
    <!-- 设定进入和离开页面时的特殊效果，这个功能即FrontPage中的"格式/网页过渡"，不过所加的页面不能够是一个frame页面。 -->
　　HTTP-EQUIV用于向浏览器提供一些说明信息，从而可以根据这些说明做出反应。HTTP-EQUIV其实并不仅仅只有说明网页的字符编码这一个作用，常用的HTTP-EQUIV类型还包括：网页到期时间、默认的脚本语言、默认的风格页语言、网页自动刷新时间等。

        网页描述方法

　　1、网页描述为自然语言而不是罗列关键词（与keywords设计正好相反）；

　　2、尽可能准确地描述网页的核心内容，通常为网页内容的摘要信息，也就是希望搜索引擎在检索结果中展示的摘要信息；

　　3、网页描述中含有有效关键词；

　　4、网页描述内容与网页标题内容有高度相关性；

　　5、网页描述内容与网页主体内容有高度相关性；

　　6、网页描述的文字不必太多，一般不超过搜索引擎检索结果摘要信息的最多字数（通常在100中文字之内，不同搜索引擎略有差异）。

 <meta name="description"content="网络营销教学网站提供《网络营销基础与实践》教学支持:网络营销课件">
　　"description"中的content="网页描述"，是对一个网页概况的介绍，这些信息可能会在搜索结果中出现，因此需要根据网页的实际情况来设计，尽量避免与网页内容不相关的“描述”，

       经常用到的主要有以下几种：

        <!-- 判断字符集，一般是utf-8 -->
        <meta charset="utf-8">
        <!-- 作者 -->
        <meta name="author" content="https://www.cnblogs.com/songtianfa/">
        <!-- 网页描述 -->
        <meta name="description" content="码农下的天空 - 博客园">
        <!-- 关键字 -->
        <meta name="keywords" content="码农下的天空,博客园">
        <!-- 设定网页到期时间，一旦网页时间到期，必须到 -->
        <meta http-equiv="expires" content="Wed, 26 Feb 199708 : 21 : 57 GMT">
        <!-- 禁止浏览器从本地机的缓存中调阅页面内容 -->
        <meta http-equiv="Pragma" content="no-cache">
        <!-- 用来防止别人在框架里调用你的页面 -->
        <meta http-equiv="Window-target" content=" top">
        <!-- 跳转页面, 5指时间停留5秒网页搜索机器人向导。用来告诉搜索机器人哪些页面需要索引，哪些 页面不需要索引 -->
        <meta http-equiv="Refresh" content="5;URL=https://www.cnblogs.com/songtianfa/">
        <!-- content的参数有all,none,index,noindex,follow,nofollow , 默认是all -->
        <meta name="robots" content="none">
        <!-- 收藏图标 -->
        <link rel="Shortcut Icon" href="favicon.ico">
        <!-- 网页不会被缓存 -->
        <meta http-equiv="Cache-Control" content="no-cache, must-revalidate">
        meta标签是HTML标head区的一个关键标签，它位于HTML文档的<head>和<title>之间（有些也不是在<head>和<title>之间）。它提供的信息虽然用户不可见，但却是文档的最基本的元信息。<meta>除了提供文档字符集、使用语言、作者等基本信息外，还涉及对关键词和网页等级的设定。