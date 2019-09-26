---
title: display用法
date: 2019-09-09 12:06:15
categories:
- 前端
tags:
- html
- css
---
　　display这个属性用于定义建立布局时元素生成的显示框类型。对于 HTML 等文档类型，如果使用 display 不谨慎会很危险，因为可能违反 HTML 中已经定义的显示层次结构。对于 XML，由于 XML 没有内置的这种层次结构，所有 display 是绝对必要的,要了解display之前，来了解一些块级元素和内联元素。

　　**1、块级元素**

　　①总是在新行上开始(块元素独占一行);

　　②高度，行高以及外边距和内边距都可控制;

　　③宽度缺省是它的容器的100%，除非设定一个宽度。

　　④它可以容纳内联元素和其他块元素

　　比如：p、div、h1、ul等。

　　**1、内联元素**

　　①和其他元素都在一行上;

　　②高，行高及外边距和内边距不可改变;

　　③宽度就是它的文字或图片的宽度，不可改变

　　④内联元素只能容纳文本或者其他内联元素

　　比如：a、em、img、span等。

　　而display就是改变这些元素的固有属性，规定元素应该生成的类型，以达到自己布局网站的效果。 经常用到有下面四个：

　　none 此元素不会被显示

　　block 此元素将显示为块级元素，此元素前后会带有换行符。

　　inline 默认。此元素会被显示为内联元素，元素前后没有换行符。

　　inline-block 行内块元素。

　　当然还有很多属性，一般比较少用，主要有以下方面：
　　

	list-item：此元素会作为列表显示。

	run-in：此元素会根据上下文作为块级元素或内联元素显示。

	compact：CSS 中有值 compact，不过由于缺乏广泛支持，已经从 CSS2.1 中删除。

	marker：CSS 中有值 marker，不过由于缺乏广泛支持，已经从 CSS2.1 中删除。

	table：此元素会作为块级表格来显示（类似 <table>），表格前后带有换行符。

	inline-table：此元素会作为内联表格来显示（类似 <table>），表格前后没有换行符。

	table-row-group：此元素会作为一个或多个行的分组来显示（类似 <tbody>）。

	table-header-group：此元素会作为一个或多个行的分组来显示（类似 <thead>）。

	table-footer-group：此元素会作为一个或多个行的分组来显示（类似 <tfoot>）。

	table-row：此元素会作为一个表格行显示（类似 <tr>）。

	table-column-group：此元素会作为一个或多个列的分组来显示（类似 <colgroup>）。

	table-column：此元素会作为一个单元格列显示（类似 <col>）

	table-cell：此元素会作为一个表格单元格显示（类似 <td> 和 <th>）

	table-caption：此元素会作为一个表格标题显示（类似 <caption>）

	inherit：规定应该从父元素继承 display 属性的值。

　　display 属性规定元素应该生成的框的类型,用的最多的就是display:block;显示 display:none;隐藏。
