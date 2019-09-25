
# web前端开发

## 1. 概述

### 1-1 web前端开发概述

**web前端开发**：web指web系统、前端指网页上用户呈现的部分、开发指编写代码

**web系统**：以网站形式呈现，通过浏览器访问，完成一定功能的系统。

**前端**：网页上为用户呈现的部分
**后端**：与数据库进行交互，完成数据存取

网站架构师——> 网页美工——> 前端开发人员

---

### 1-2 网站与网页

**网站（website）**：互联网上用于展示特定内容的相关网页的集合

**网页(web page)**：网站中的一页，一个网站中的网页通过“超链接”的方式被组织在一起

**主页（home page）**：进入网站看到的地一个网页，主页的文件名通常是index

**网页元素**：logo、导航栏、文字超链接、banner广告横幅、表单

网站——> 文件夹
网页——> 文件

服务器端 客户端

浏览器：解析网页源代码，渲染网页

世界上主流浏览器：chrom、firefox、IE、safari、opera

---

## 2. HTML基础

### 2-1 HTML概述

HTML（HyperText MarkUp Language）：“超文本标记语言”，它是制作网页的标准语言，HTML不区分大小写（通常采用小写）。

标签：由尖括号包围，比如`<title>`，通常是成对出现的。
<br/>

`<title>网页标题</title>`——> 开始标签、内容、结束标签

标签分为双标签和单标签
- 双标签:`<title>网页名称</title>`
- 单标签:`<img/>`


元素：把开始标签、内容和结束标签一起称之为元素

标签嵌套:外层标签（父元素）、内层标签（子元素）、同级元素（兄弟元素）
```html
<!--外层：父元素-->
<html>
  <!--内容：子元素-->
  <head>
  </head>
  <!--同级元素：兄弟元素-->
  <body>  ——>
  </body>
</html>
```

DOM：Document Object Model：文档对象模型

属性：<img src="" alt="">，一个标签可能有多个属性，属性先后顺序无关

---

### 2-1 HTML文件结构

HTML基本文件结构：.html或.htm
```HTML
<html>
  <!--头部：浏览器、搜索引擎所需信息-->
  <head>
    <title>网页标题</title>
  </head>
  <!--主体：网页众包含的具体内容-->
  <body>
    网站内容
  </body>
</html>
```

HTML5文档基本结构：

```html
<!DOCTYPE html>
<!--文档类型：符合HTML5标准-->
<!--lang属性：搜索引擎,en—— 英文,zh—— 中文-->
<html lang="en">
  <head>
    <!--meta 元数据-->
    <!--charset属性：字符集编码方式，浏览器UTF-8是国际编码-->
    <meta charset="utf-8">
    <title>网页标题</title>
  </head>
  <body></body>
</html>
```

字符集与编码

字符（Character）：文字、符号

字符集（charset）：字符的集合，字符集——语言文字

编码：将字符和二进制码对应起来

ASCII：数字、英文字母、符号进行了编码

GB2312：简体中文

Unicode：所有语言

UTF-8：所有语言，占用空间更小

乱码问题
- 源文件保存时的编码
- 源文件声明`<meta charset="编码方式" />`，不一致，就会出现乱码问题

---

### 2-3 HTML标签（1）h1~h6、p、br、pre、span、hr

标题：h1-h6

段内换行：br

段内分组：span

段落：p

预留格式：pre

水平箱：hr

---

### 2-4 HTML标签（2） a

文字超链接、图片超链接、导航栏

```html
<a href="网址">文字或图片</a>

<!--链接到本站点其他网页-->
<a href="news.html">新闻</a>

<!--链接到其他站点-->
<a href="http://www.baidu.com">百度</a>

<!--虚拟超链接-->
<a href="#">板块2</a>
```
---

### 2-5 HTML标签（3）img

图像格式，网页中常见的图片格式：jpg、gif、png

- JPG：有损压缩，色彩丰富图片

- GIF：简单动画、背景透明

- 无损压缩、透明、交错、动画

透明：可以给图片指定一种颜色，使其不被显示而成为透明

交错：在显示图片的过程中可以从概貌逐渐到全貌，看上去也就是清晰度的从小变大  

插入图像 img

```html
<!--src属性是图片的来源，alt属性设置的图片替换文本。-->
<img src="w3cschool.gif" alt="w3c"/>
```

绝对路径与相对路径：
- 绝对路径：以根目录为基准

```html
<img src="C:/site/logo.gif" />
```
- 相对路径：以该文档所在位置为基准

```html
<img src="logo.gif" />
```
---

### 2-6 HTML标签（4）div、ul、ol、table

区域：div

列表：ol、ol、li

表格：table、tr、td

区域：确定一个单独的区域，如页面的一个组成部分，一个栏目板块

列表：

- 无序列表：ul li

```html
<ul>
  <li>列表项1</li>
  <li>列表项2</li>
  <li>列表项3</li>
</ul>
```

- 有序列表：ol、li

```html
<ol>
  <li>列表项1</li>
  <li>列表项2</li>
  <li>列表项3</li>
</ol>
```

表格 table、tr、td

```html
<table>
  <tr>
    <td>单元格</td>
    <td>单元格</td>
    <td>单元格</td>
  </tr>
  <tr>
    <td>单元格</td>
    <td>单元格</td>
    <td>单元格</td>
  </tr>
</table>
```

---

### 2-7 HTML标签（5）form、input、select、textarea

表单：是一个区域，采集用户信息

表单元素：文本框、按钮、单选、复选、下拉列表、文本域

表单`<form>`标签

```html
<form action="数据处理网页">
表单元素
</form>
```

文本框、密码框 input

```html
<!--文本框：type="text"-->
<!--密码框：type="password"-->
<form>
  <input type="text | password" name="userName | userPassword"/>
</form>
```

提交按钮、重置按钮

```html
<!--提交按钮：type="submit"-->
<!--密码框：type="resit"-->
<form>
  <input type="text | password" value="提交 | 重置"/>
</form>
```

单选框：只能选择一项

```html
<!--当设置checked="checked"时，该选项被默认选中-->
<!--同一组name属性的值要一样-->
<form>
  <input type="radio" value="值" name="名称" checked="checked"/>
</form>
```

复选框：任意选择多项

```html
<!--当设置checked="checked"时，该选项被默认选中-->
<!--同一组name属性的值要一样-->
<form>
  <input type="checkbox" value="值" name="名称" checked="checked"/>
</form>
```

下拉列表框

```html
<select>
  <option>选项1</option>
  <option selected="selected">选项2</option>
  <option>选项3</option>
</select>
```

文本框

```html
<form>
  <textarea rows="行数" cols="列数">文本</textarea>
</form>
```
---

### 2-8 web语义化 em、strong、dl、dt、dd

web语义化：让页面具有良好的结构与含义，从而让人和机器都能快速理解网页内容。

- 结构清晰，利于团队的开发、维护

- 有利于搜索引擎的理解

- 搜索引擎优化（SEO：Search Engine Optimization）

- 容易兼容不同设备

em、strong

```html
<p>
  <em>强调</em>
  <i>斜体、无语义</i>
</p>

<p>
  <strong>粗体</strong>
  <b>粗体、无语义</b>
</p>
```

dl、dt、dd

```html
<dl>
  <dt>HTML</dt>
  <dd>超文本标记语言</dd>
  <dt>css</dt>
  <dd>层叠样式表</dd>
</dl>
```

---

## CSS样式

### 3-1 CSS概述

CSS：Cascading Style Sheet 层叠样式表

内容和样式相分离，便于修改样式

```CSS
选择器{
  属性名:属性值;
}
```
- 最后一条声明可以没有分号，但是为了以后修改方便，一般也加上分号

- 为了使用样式更加容易阅读，可以将每条代码写在一个新行内

---

### 3-2 CSS添加方法

 - 行内式

```html
<!DOCTYPE html>
<html>
  <head></head>
  <body>
    <p style="color:red;font-size:14px">天使投资指早期投资，尤其指个人早期投资。</p>
  </body>
</html>
```
- 内嵌式

```html
<!DOCTYPE html>
<html>
  <head>
    <style type="text/css">
      p:{
        color:red;
        font-size: 14px;
      }
    </style>
  </head>
  <body>
    <p>天使投资指早期投资，尤其指个人早期投资。</p>
  </body>
</html>
```

>- 即使有公共CSS代码，也是每个页面都要定义的
>
>- 适合文件很少，CSS代码也不多的情况
>
>- 如果一个网站有很多页面，每个文件都会变大，后期维护难度很大

- 外链式

外部样式表文件 style.css
```css
p{
  color:red; /*设置文字颜色*/
}
```

网页文件 1.html

```html
<html>
  <head>
    <link rel="stylesheet" href="style.css"
  </head>
  </style>
  <body>
    <p>天使投资指早期投资，尤其指个人早期投资。</p>
  </body>
</html>
```

>- 页面结构HTML代码与样式CSS代码的完全分离
>
>- 维护方便
>
>- 如果需要改变网站风格，只需要修改公共CSS文件
>
>- 可以在同一个HTML文档内部引用多个外部样式表

> 多种样式可以层叠，可以覆盖
>
>样式的优先级按照“就近原则”
>
>行内样式>内嵌样式>外链样式>浏览器默认样式

---

### 3-3 CSS选择器

标签选择器、类选择器、id选择器、并集选择器、后代选择器、子代选择器、相邻兄弟选择器、通用兄弟选择器

---

### 3-4 CSS样式（1） 文字样式

单位：px（像素）、em（1em = 一个字符，2em = 两个字符）、%（百分比）
