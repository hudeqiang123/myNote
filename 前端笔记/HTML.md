> Webstorm常用快捷键
> 1. 新建文件：alt+alt+insert
> 2. 光标移到当前行最后：end
> 3. ctrl+滚轮：放大缩小文字
> 4. ctri+shift+d：复制当前行
> 5. ctrl+shift+k：删除当前行
> 6. 光标移到当前行最前：home
> 7. 让光标在多行中闪烁：alt+滚轮滑动
> 8. 快速复制光标的所在行：ctrl+d
> 9. 自动在一段内容前后加上标签：ctrl+alt+t+回车+输入标签
> 10. 注释：ctrl+/
> 11. 快速合并和展开代码--合并：ctrl+shift+-     展开：ctrl+shift+ +
> 12. 快速新起以行：shift+回车
> 13. 快速移动选中的代码，上下移动
>
> - 往上移动：ctrl+shift+方向键上
> - 往下移动：ctrl+shift+方向键下

---



# html
> 上网的时候，是有真实的、物理的文件传输的<br>
> 第二次打开网页，比第一次打开的快，因为缓存
> 上网就是请求数据
> - 服务器存放着网页的相关文件，包括html文件、css文件、js文件、图片等。当我们打开浏览器，输入网址，我们的计算机就会对这些文件发出HTTP请求。
> - 服务器接收到请求之后，会把这些文件通过HTTP协议，传输到我们的计算机中。这些文件将在我们计算机本地浏览器，进行渲染、呈递。

## 一、 HTML基础--基本概念

### 1. 什么是浏览器

- 浏览器是安装在电脑里面的一个软件，能够让网页内容呈现给用户查看，并让用户与网页交互的一个软件。
- 常见的主流浏览器以及内核
  1. IE浏览器--Trident
  2. 谷歌浏览器--Blink
  3. 火狐浏览器--Gecko
  4. Safira浏览器--Webkit
  5. Opera浏览器--Presto（想在是谷歌浏览器内核Blink）

> 作为前端开发，我们会使用HTML+CSS+JS编写代码，编写代码的时候要遵循一些规范（W3C）<br/>
> 浏览器开发商开发的浏览器，目的就是为了按照W3C的规范，识别出开发者编写的代码，并且在页面中绘制出开发者预想的页面和效果（GPU：显卡），我们把浏览器中识别代码绘制页面的东西称为“浏览器的内核或者渲染引擎”。
>
> 浏览器兼容：
> 1. W3C发布的规范都是开发者们不断尝试总结下来的产物，举个例子：谷歌浏览器开发了一个新的CSS属性（border-radius）可以让开发者快速实现盒子圆角。
> 2. 每个浏览器为了彰显自己的不一样，不按照标准来，但是把标准中规定的效果用另一种方式实现了。
> 3. window.getComputedStyle
> 4. currentStyle

### 2. 什么是服务器
- 服务器也是电脑，只不过是比我们的电脑配置更高的电脑，并且24小时不断电，不关机的计算机。
- 服务器是专门用户存储数据的电脑，访问者可以访问服务器上存储的资源
- 服务器一关机，访问者就无法访问

### 3. 服务器访问网页的原理

- 当我们利用浏览器访问网页时，其实是有真实的物理文件传输的，浏览器会先将网页上的内容缓存到本地文件夹中，然后再渲染出来呈现给用户查看
- 平时我们上网时，感觉第二次访问网页会比第一次访问网页要快，就是因为第一次访问时已经将这个网页上的信息缓存到了本地上
- 通过观察还发现缓存文件夹中除了图片以外还缓存了一些其他文件，例如js、css、html

### 4. 浏览器请求数据的原理
1. 发送请求--请求行+请求头+请求体
2. 处理浏览器请求
3. 将处理结果返回给浏览器
4. 发送响应--响应行+响应头+响应体

### 5. 什么是URL

- 我们在浏览器的地址栏中输入的这个地址就是URL
- URL拆分（http://127.0.0.1:80/index.html）
- - http://（协议类型）
  - 127.0.0.1（服务器的IP地址）
  - :80（服务器的端口号）
  - index.html（需要访问的资源名称）

### 6. 什么是HTTP协议

- HTTP是Typertext Transfer Protocol的缩写。超文本传输协议
- 什么是协议？
- - 用来规范/约束某一类事物
- HTTP协议就是用来规范/约束哪一类事物？
  - HTTP协议规范/约束浏览器和服务器之间如何沟通

---

## 二、HTML基础--认识HTML

> HTML其实就是HyperText Markup Language的缩写，超文本标记语言的缩写。
>
> html就是负责描述页面的语义；css负责描述描述页面的样式；js负责描述页面的动态效果的。

### 1. HTML的作用

- 作用：专门用来描述文本的语义，也就是说我们可以利用HTML告诉浏览器哪些是标签，哪些是段落
- 注意：HTML是专门用来添加语义的，而不是用来修改文本的样式的

### 2. HTML发展史

1. 1993年（IETF）html1.0
2. 1995年（W3C）html2.0
3. 2008年 HTML5正式版

### 3. 网页的固定模式

```html
<!DOCTYPE html>
<html>
  <head lang="en">
    <meta charset="utf-8">
    <!--网页中的所有超链接都在新的窗口打开-->
    <base target="_blank" />
    <title></title>
  </head>
  <body>
  </body>
</html>
```

- html标签：告诉浏览器这是一个网页
- head标签：用于给网页添加一些配置信息（不会显示给用户看）
  - 网站的标题/指定网站的小图标
  - 添加网站的SEO相关的信息（指定网站的关键字/指定网页的描述信息）
  - 外挂一些外部的CSS/JS文件
  - 添加一些浏览器适配相关的内容
- title标签：专门用于指定网站的标题，并且这个指定的标签将来还会作为用户保存网站的默认标题
- body标签：专门用于定义HTML文档中需要显示给用户查看的内容,属性text取值是一个颜色值，属性bgcolor也是一个颜色值

### 4. 字符集问题
- meta标签：指定当前网页的字符集
```html
<meta charset="UTF-8">
```
- 什么是字符集？
  - 字符集就是字符的集合
- 常见的字符集
  - gb2312--存储的字符比较少
  - UTF-8--存储了世界上所有的文字
注意：meta里面声明的字符集和保存的时候的设置要匹配

---
### 5. HTML标签
- html标签的分类
  - 双标签
  - 单标签：`<br/>、<hr/>、<img/>、<input/>`
- html标签关系分类
  - 并列关系
  - 嵌套关系
- 容器级标签
  - 里面可以放置任何东西
- 标记的属性
  - 用来修饰标记的效果的内容，就是属性。属性必须声明在开始标记中；属性与标记名称之间用空格隔开；属性的值与属性之间使用“=”连接；一个元素允许有多个属性，多属性间，排名不分先后，中间用空格隔开
- 四大标准属性：
 - id：定义元素在页面中独一无二的名称
 - title：鼠标悬停在元素上时，体现的文字
 - class：引用类选择器时使用（CSS）中
 - style：定义内联方式使用
- 文本级标签
  - 可以放置文字、图片、表单元素

---

### 6. DTD文档声明

1. 什么是DTD文档声明
   - 文档声明可告知浏览器文件使用哪种HTML或XHTML规范
   - 能够正确的编译/解析/渲染我们的网页
2. DTD文档声明的格式
   - html5声明的格式

```html
<!DOCTYPE html>
```

1. DTD文档声明的注意点
   - 文档声明必须在第一行
   - DTD文档声明不区分大小写
   - DTD声明不是一个标签

> 一共有6种DTD：
> - HTML4.01
> - Strict
> - Transition
> - Frameset
> - XHTML1.0
> - Strict
> - Transition
> - Frameset
>
> Strict：表示“严格的”，这种模式里面的要求更为严格。有一些标签不能使用。<br>
> Transition：普通的，这种模式就是没有一些别的规范<br>
> Frameset：带有框架的页面
---
### 7. meta标签

- 定义字符集

```
<meta charset=""utf-8 /?>
```

- 指定网页的描述（SEO：seach engine optimization搜索引擎优化）

```
<meta name="description" content="发布h5、js等前端相关的信息" />
```

- 设置网页的关键词（搜索引擎在检索页面时，会同时检索页面中的关键词和描述，但是这两个值不会影响页面在搜索引擎中的排名）

```
<meta name="keywords" content="HTML5、JavaScript、前端、Java" />
```

- 请求的重定向：使用meta可以用来做请求的重定向。

```
<meta http-equiv="refresh" content="秒数;url=目标路径"

<meta http-equiv="refresh" content="5;url=http://www.baidu.com" /?>
```

---

### 8. title标签
网页的标题、有利于SEO

```html
<title>网页的标题</title>
```

### 9. HTML语法规范

1. HTML不区分大小写，但是我们一般都使用小写

2. HTML中注释不能嵌套

3. HTML标签结构必须完整，要么成对出现，要么自结束标签

4. HTML标签可以嵌套，但是不能交叉嵌套

5. HTML标签中的属性必须有值，且值必须加引号

---
## 三、HTML基础--基础标签

### 1. 标题标签
- 被标题标签包裹的内容会独占一行

- 在标题标签中，`<h1>`最大，`<h6>`最小

- 在企业开发中，`<h1>`标签中只能出现一次（和SEO有关）

```html
在显示效果上h1最大，h6最小，但是文字大小我们并不关心

使用html标签时，关心的是标签的语义，我们使用的标签都是语义化标签

6级标题中，h1最重要，表示一个网页中的主要内容，h2~h6重要性依次降低

对于搜索引擎来说，h1的重要性仅次于title，搜索引擎检索完title，会立即查看h1中的内容

h1标签非常重要，它会影响到页面在搜索引擎中的排名，页面只能写一个h1

<h1> <h2> <h3> <h4> <h5> <h6>
```
---

### 2. 段落标签
- 在浏览器中会单独占一行，并且段与段之间会有一个间距

```html
<p>这是段落！！</p>
```

### 3. 分割线标签

```html
<hr size="2px" width="" align="" color="" />
```
- 在浏览器上是一条分割线
- 在浏览器上单独占一行

```
<hr/>
```
### 4. HTML注释
```html
<!--注释内容-->
```
### 5. 图像标签

1. img标签不会独占一行
2. 如果手动的指定图片的宽度和高度，可能会导致图片变形（只指定一个值就不会变形）

```html
<img src="" alt="" title="" />
```

- src：图片路径
- width：图片的宽度，一般使用px作为单位
- height：图片的高度，一般使用px作为单位
- title：当鼠标悬停在图片上时，需要弹出的描述框中显示什么内容
- alt：alt是英语“alternate”替代的意思，就表示不管什么原因，当这个图片无法被显示的时候，出现的替代文字（有的浏览器不支持）；搜索引擎可以通过alt属性来识别不同的图片，如果不写alt属性，则搜索引擎不会对img中的图片进行收录

```
- JPEG（PNG）：JPEG图片支持的颜色比较多，图片可以压缩，但是不支持透明。一般使用JPEG来保存照片等颜色丰富的图片。

- GIF支持的颜色少，只支持简单的透明，支持动态图。图片颜色单一或者是动态图时可以使用GIF。

- PNG：PNG支持的颜色多，并且支持复杂的透明。可以用来显示颜色复杂的透明的图片。

图片的使用原则：效果不一致，使用效果好的；效果一致，使用小的。

```

### 6. 段内换行标签

```html
<br/>
```

1. 多个换行标签可以连续使用，使用了多少个br标签就会换多少行
2. br标签不要用来另起一个段落

### 7. 路径问题

  url（Uniform Resource Locator），统一资源定位器。用来标识某个资源文件的位置

- 相对路径：从当前文件位置开始查找资源文件所经过的路径就是相对路径。
  - 同一级：图片和.html文件存储在同一个文件夹中
  - 下一级：就是存储图片的文件夹和.html文件在同一个文件夹中
  - 上一级：存储图片的位置和存储代码的文件夹在同一个文件夹中(../找上一级)


- 绝对路径：特点：从文件所在的最高级目录开始查找资源文件所经过的路径，就是绝对路径。使用场合：当向访问互联网上的资源时，只能用绝对路径。完整的绝对路径四部分：http://www.codebuy.com/img/header/logo.png
 - 协议名- http
 - 域名（主机名，IP地址） - www.codebuy.com
 - 目录路径 - img/header
 - 文件名 - logo.png


- 根相对路径：路径形式是以“/”作为开始的，/ 表示的是服务器的根目录。

---

### 8. 链接标签

文字超链接、图片超链接、导航栏
```html
<a href="网址" target="">文字或图片</a>
```
1. 什么是a（anchor）标签
   - 作用：就是控制页面与页面之间的跳转的
   - 注意点
     - a标签不仅可以让文字可以点击，还可以让图片也能被点击
     - 一个a标签必须有一个href属性，否则a标签不知道跳转到什么地方
     - 如果通过a标签的href属性指定一个URL地址，那么必须在地址前面加上http://或https://
     - a标签的href属性还可以链接本地文件
   - 格式：

```html
<!--href：hypertext reference超文本地址的缩写 -->
<a href="跳转的页面">给用户看的内容</a>  

<a href="网址">文字或图片</a>

<!--链接到本站点其他网页-->
<a href="news.html">新闻</a>

<!--链接到其他站点-->
<a href="http://www.baidu.com">百度</a>

<!--虚拟超链接-->
<a href="#">板块2</a>

```

1. target属性--控制如何跳转
   - _self：用于在当前选项卡中跳转，不新建界面跳转（默认的）
   - _blank：用于在新的选项卡中跳转，也就是新建界面跳转
2. title属性--控制鼠标悬停时显示的提示文本
3. base标签--指定当前网页中的所有的超链接（a标签）如何打开，写在head标签之间

```html
<base target="_blank" />
```

1. 假链接--就是点击不会跳转

```html
<!--第一种格式-->
<a href="#"></a>
<!--第二种格式-->
<a href="javascript:;"></a>
区别：#会回到顶部
	 javascript:不会回到顶部
```

1. 锚点链接
   - 要想通过a标签跳转到指定的位置，那么必须告诉a标签一个独一无二的id属性，这样a标签才能在当前界面中找到需要跳转的目标位置
   - html标签给一个id属性

> 1. 给目标位置的标签添加一个id或者name属性，
>
> ```h't'm
> <a href="#center">跳转到中部</a>
> ```
>
> 1. 告诉a标签需要跳转到的目标标签对应的id
>
> ```html
> <a name="center">我是中部<h1>
> ```

超链接的四种表现形式：

- 点击操作时，完成资源下载的操作。点击的资源为zip /rar 时则为下载操作

```html
<a href="day01.rar">下载</a>
```

- 电子邮件链接。必须在计算机中安装并配置好至少一个邮件客户端的信息

```html
<a href="mailto:zhaoxu@tedu.cn">联系我们</a>
```

- 返回页面顶部的空链接

```html
<!--如果将链接地址设置为#，则点击超链接以后，会自动跳转到当前页面的顶部-->
<a href="#">返回顶部</a>
```

- 执行JavaScript代码片段

```html
<a href="javascript:JS代码">执行JS</a>
```
---

9. 预留格式标签

```html
<pre>
保留空格！
</pre>
```

10. 实体

```html
在html中，一些如<，>这种特殊字符是不能直接使用，需要使用一些特殊的符号来表示这些字符，这些符号我们称为实体或者转义字符。

实体的语法：&实体的名字;

&nbsp; 空格
&gt;  >
&lt;  <
&copy; 版权符号
```

11. 文本样式相关的标签

```html
<b></b>: 加粗
<i></i>: 斜体
<u></u>: 下划线
<s></s>: 删除线
<sup></sup>: 上标
<sub></sub>: 下标

```

12. 内联框架

```
使用内联框架可以引入一个外部的页面

使用iframe来创建一个内联框架

在现实开发中不推荐使用内联框架，因为内联框架中的内容不会被搜索引擎所检索

属性：
  src：指向一个外部页面的路径，可以使用相对路径
  width：
  height：
  name：

<a href="demo.03" target="tom">跳转的内容在内联框架中打开</a>

<iframe src="demo02.html" name="tom"></iframe>
```

---


## 四、HTML基础--列表标签

> list：list item
>
> 注意：li不能单独存在，必须包裹在ul里面，ul的子元素也必须是li标签

### 1. 无序列表（最多）

> unordered list（菜单）



```html
<ul>
    <li>无序列表项1</li>
    <li>无序列表项2</li>
    <li>无序列表项3</li>
    <li>无序列表项4</li>
</ul>
```

```html
<body>
<h1>w物品清单</h1>
<ul>
    <li>
        <h2>蔬菜</h2>
        <ul>
            <li>白菜</li>
            <li>萝卜</li>
            <li>黄瓜</li>
        </ul>
    </li>
    <li>
        <h2>水果</h2>
        <ul>
            <li>苹果</li>
            <li>香蕉</li>
            <li>橘子</li>
        </ul>
    </li>
</ul>
</body>
```



### 有序列表（最少）

> ordered list

```html
<ol>
    <li>列表项1</li>
    <li>列表项2</li>
    <li>列表项3</li>
</ol>
```

### 定义列表（其次）

> definition list（网站页脚）

```html
<!--dt--definition title（定义列表标题）-->
<!--dd--definition description（定义标题对应的描述）-->
<dl>
    <dt>北京</dt>
    <dd>中国的首都</dd>

    <dt>上海</dt>
    <dd>富人的集中地</dd>
</dl>
```

## 五、div和span

> div+span是非常重要的标签，div的语义是division“分割”，span的语义是就是span“范围、跨度”。这两个东西，都是重要的盒子

### div

> div在浏览器中，默认不会增加任何的效果改变的，但是语义变了，div中的所有元素都是一个小区域。div标签是一个容器级标签，里面什么都能放，甚至可以放div自己。

### span

> span也是表达“小区域、小跨度”的标签，但是是一个“文本级”的标签。就是说，span里面只能放置表单、图片、文字元素。

## 六、HTML基础--表格标签

```html
<table>
    <caption>表格标题</caption>
    <tr>
        <th>1</th>
        <th>2</th>
        <th>3</th>
    </tr>
    <tr>
        <td>11</td>
        <td>22</td>
        <td>33</td>
    </tr>

</table>

```

> 基本标签：
>
> - table:表格标签
> - tr：行
> - td：单元格
> - caption：表格标题
> - th：当前列的标题
>
> 表格属性：
>
> - 宽度（width）
> - 高度（height）属性（table、td）
> - 水平对齐（align="center、left、right"）
> - 垂直对齐（valign="top、middle、bottom"）--（table、tr、td）
> - 外边距（cellspacing）：单元格和单元格之间的距离
> - 内边距（cellpadding）：单元格的边框和文字之间的距离
> - 边框：border
> - 背景颜色：bgcolor

- 表格的基本结构
  1. 表格的标题（caption）
  2. 表格的表头信息（thead）
  3. 表格的主体信息（tbody）
  4. 表格的页尾信息（tfoot）
- 单元格的合并
  - 合并列：colspan
  - 合并行：rowspan

## 七、HTML基础--表单

> form就是英语表单的意思，form标签里面有action属性和method属性<br/>action属性就是表示，表单提交到哪里<br//>mthod属性表示用什么HTTP方法提交，有get、post两种

1. 什么是表单？
   - 表单就是专门用来收集用户信息的
2. 表单的格式

```html
<form>
	<表单元素>
</form>
```

1. 常见的表单格式
   - input标签
     - 文本框：`<input type="text" />`
     - 密码框：`<input type="password" />`
     - 单选框：`<input type="radio" name="sex"/>`
     - 复选框：`<input type="checkbox"/>`
     - 图片按钮：`<input type="img" src="" />`
     - 重置按钮：`<input type="reset" />`
     - 提交按钮：`<input type="submit" />`
     - 普通按钮：`<input type="button">`
     - 隐藏域：`<input type="hidden" />`

```html
<form action="" method="get/method">
    文本框：<input type="text" value="值"/> <br/>
    密码框：<input type="password" value="123"/> <br/>

    <!--单选框-->
    <!--必须给name属性 属性值必须相同-->
    <!--添加check默认选中-->
    单选框1：<input type="radio" name="sex" checked="checked"/> <br/>
    单选框2：<input type="radio" name="sex"/> <br/>

    爱好：
    <input type="checkbox" checked/>
    <input type="checkbox"/>
    <input type="checkbox"/>
</form>
```



- label标签--通过for属性和输入框的id进行绑定即可

```html
<form action="">
        <label for="account">账号：</label>
        <input id="account" type="text"/>
        <br/>
        <label for="pwd">账号：</label>
        <input id="pwd" type="text"/>
       <br/>
</form>
```

- datalist标签--给输入框绑定待选项（datalist的id对应的值赋值给表单的list属性）

```html
<body>
请输入的车型：<input list="cars" type="text"/>
<datalist id="cars">
    <option>奔驰</option>
    <option>宝马</option>
    <option>奥迪</option>
    <option>路虎</option>
    <option>宾利</option>
</datalist>
</body>
```

- 邮箱：`<input type="email" />`
- 域名：`<input type="url" />`
- number：`<input type="number" />`
- 时间：`<input type="date" />`
- 颜色：`<input type="color" />`

1. select标签--下拉列表

```html
<body>
<select name="" id="">
    <optgroup label="北京">
        <option value="">朝阳区</option>
        <option value="">昌平区</option>
        <option value="">通州区</option>
    </optgroup>
    <optgroup label="广州">
        <option value="">天河区</option>
        <option value="">越秀区</option>
        <option value="">黄浦区</option>
    </optgroup>
</select>
</body>
```

1. textarea标签--文本域

```html
<textarea name="" id="" cols="30" rows="10">

</textarea>

设置onresize: none;可以让多行文本框不能拖动
```

1. fielset标签

```html
<fieldset>
	<legend>注册界面<legend/>
	<!--表单控件-->
<fieldset/>
```

1. 注意问题

>在单选框和多选框中，所有项目的name属性的值必须一样。<br/>在表单标签中，除了按钮标签以外的标签，都可以通过value来指定需要提交到服务器的数据。

## 八、HTML基础--文本格式化

### 1、HTML文本格式化标签

|   标签   |     描述     |
| :------: | :----------: |
|   <b>    | 定义粗体文本 |
|   <em>   | 定义着重文字 |
|   <i>    |  定义斜体字  |
| <small>  |  定义小号字  |
| <strong> | 定义加重语气 |
|  <sub>   |  定义下标字  |
|  <sup>   |  定义上标字  |
|  <ins>   |  定义插入字  |
|  <del>   |  定义删除字  |

### 2、html废除标签

> font
>
> b
>
> u
>
> i
>
> del
>
> hr
>
> em
>
> strong
>
> br

## 九、HTML基础-多媒体标签

- video标签--视频

```html
<video src=""></video>
```

- audio标签--音频

```html
<audio src=""></audio>
```

> 常用属性：
>
> - src：播放的视频地址
> - autoplay：是否需要自动播放
> - controls：用于告诉video是否需要控制条
> - poster：用于告诉video视频没有播放之前的占位图片（音频不支持）
> - loop：用于告诉video标签视频播放之前是否循环播放
> - preload：预加载视频，但是需要注意的是preload和autoplay相冲
> - muted：静音
> - width:（音频不支持）
> - sheight:（音频不支持）

## 九、HTML基础--HTML 5标签

- detail标签--概要与详情标签

```html
<details>
    <summary>夫的枪</summary>
    关雎
    作者：无名氏
    关关雎鸠，在河之洲。
    窈窕淑女，君子好逑。
    参差荇菜，左右流之。
    窈窕淑女，寤寐求之。
    求之不得，寤寐思服。
    悠哉悠哉，辗转反侧。
    参差荇菜，左右采之。
    窈窕淑女，琴瑟友之。
    参差荇菜，左右芼之。
</details>
```

- marquee标签--跑马灯

```html
<body>
<marquee>
    关关雎鸠，在河之洲。
    窈窕淑女，君子好逑。
    参差荇菜，左右流之。
    窈窕淑女，寤寐求之。
    求之不得，寤寐思服。
    悠哉悠哉，辗转反侧。
    参差荇菜，左右采之。
    窈窕淑女，琴瑟友之。
    参差荇菜，左右芼之。
</marquee>
</body>
```

> 常用属性：
>
> direction：滚动方向（right、up、down、left）
>
> scrollamount：设置滚动速度（值越大，滚动越快）
>
> loop：设置滚动次数（默认-1，无限次）
>
> behavior：设置滚动类型（slide--滚动到边界停止、alternate--滚动到边界就弹回）

## 十、HTML基础--字符实体



```html
空格：&nbsp;
大于：&gt;
小于：&It;
和号：&amp;
引号：&quot;
版权：&copy;

```
