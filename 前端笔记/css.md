# CSS

快捷键
>bgc-->background-color：背景颜色
>
>fwb-->font-weight:normal：正常
>
>fsi-->font-style:italic：斜体
>
>fsn-->font-style:normal：不斜体
>
>tdn-->text-decoration:normla：没有下划线
>
> 类上样式，id上行为（css层面用class，id属性是给js用的）
>
> 就近原则：就近原则是标签近，不是CSS书写的位置近（注意：纠正观念！）
>
>书写位置一样近，然后再考虑谁写后面就听谁的。
>嵌套盒子用padding，相邻盒子用margin

> ### 常见兼容问题：
>
> 子代选择器：IE7开始兼容，IE6不兼容
>
> 序选择器：IE8兼容，IE6、7都不兼容
>
> 兄弟选择器：IE7开始兼容，IE6不兼容

> Cascading style Sheet层叠样式表

> - ## 清除默认边距
>
> ```css
> *{
>  padding: 0;
>  margin: 0;
> }
> ```
>
> - ### 行高（一行文字垂直居中，可以设置行高等于高）
>
> CSS中，所有的行，都有行高，绝对不是直接作用在文字上的，而是作用在“行”上的。
>
> ```css
> line-height: 80px;
> ```
>
> - 注意点：
> - 如果一个盒子存储的是文字，那么一般情况下我们会以盒子左边的内边距为基准，不会以右边的为基准，因为右边的内边距有误差
> - 右边的内边距误差从何而来？因为右边如果放不下一个文字，那么文字就会换行显示，所以文字和内边距之间的距离就有误差。
> - 顶部的内边距并不是边框到文字顶部的距离，而是边框到行高顶部的距离。
>
> - ### 常用的清除浮动方式（伪元素清除浮动）
>
> ```css
> .clearfix::before{
>  content: "";
>  display: block;
>  height: 0;
>  visibility: hidden;
>  clear: both;
>   *zoom: 1;（兼容IE6）
> }
> ```
>
> - ### overflow: hidden的作用
> - 可以将超出标签范围的内容剪掉
> - 清除浮动
> - 可以通过overflow: hidden，让里面的盒子设置margin-top之后，外面的盒子不会下来。（父盒子）











## CSS样式表引入

1. 内联（行内样式表--inline style）--直接在标记里面写
2. 外联（外部样式表--extranal style sheet）--放在一个以.css为扩展名的外部样式表文件中，通过link标签将外部样式表引入在HTML中
3. 内嵌（内部样式表--internal style sheet）--style标签位于head标签之中
4. 导入样式--`<style>  @import  "";（通过style标签）</style>`

> 多重样式优先级：内联 >内部 >外联
>
> 外联和导入的区别：
>
> - 外联是通过link标签关联，导入是通过@import关联（CSS2.1退出的，有兼容问题）
> - 外联在显示界面时，会先加载CSS样式，再加载结构，所以用户看到界面时一定设置了样式；导入样式在显示界面的时候，会先加载结构，再加载样式，所以用户看到界面的时候不一定加载了样式





## CSS文字属性

1. 规定文字样式的属性

> ```css
> font-style: italic（倾斜）、normal（正常）、oblique（斜体）
> ```

2. 规定文字粗细的属性

> ```css
> font-weight: bold=400（加粗）、bolder=900（更粗）、lighter=100（细线）、normal
> ```

3. 规定文字大小的属性

> ```css
> font-size: 16px;(默认)
> ```

4. 规定文字字体的属性

> ```css
> fint-family:"宋体","微软雅黑";（默认）
> //如果是中文，需要用引号括起来
> //设置的字体必须是用户电脑里面已经安装的字体
> //英文字体必须在中午了字体前面
>
> //企业常用的字体
> //中文：宋体、黑体、微软雅黑
> //英文："Times New Roman"、Arial
> ```

5. 文字属性的简写

> ```css
> font：italic bold 10px "微软雅黑";
> //格式：font: font-style font-weight font-size font-family;
> //注意点：字体大小和字体两个属性是必须的，位置也不能交换
> ```





CSS文本属性

1. 文本装饰的属性

> ```css
> text-decoration: line-through（删除线）、overline（上划线）、none（取消修实线）、underline（下划线）
> text-decoration: none;（取消超链接的下划线）
> ```

2. 文本水平对齐的属性

> ```css
> text-align: left（左）、center（中）、right（右）、justify(每一行展开为宽度相等，左右外边距时对齐)
> ```

3. 文本缩进的属性

> ```css
> text-indent: 2em;
> ```

4. 字符颜色属性

> ```css
> color: red
> ```
>
> 格式：
>
> - 英文单词：red
> - rgb--   ==r（red 红色）==           ==g（green 绿色）==         ==b（blue 蓝色）==
> - rgba--a（越小越透明）
> - 十六进制--十六进制转换为十进制（用十六进制的第一位*16加上十六进制的第二位）
> - 十六进制缩写--ff0000简写为f00（每两位必须相同）

5. 文本转换

```css
text-transform: uppercase（大写）、lowercase（小写）、capitalize（首字母大写）
```

6. 设置字符间距

```css
text-spacing:
```

7. 设置行高

```css
line-height:
```

8. 设置字间距（单词之间）

```css
word-spacing:
```

9. 字符之间距离（英文字符之间）

```css
letter-spacing:
```

10. 文本方向（默认从左到右）

```css
direction :rtl;
```

11. 禁用为了之环绕

```
white-spacing: nowrap;
```

12. 设置文本的垂直对齐图像

```css
vertical-align: text-top、vartical-bottom
```

13. 文本阴影

```css
text-shadow: 2px 2px #ff0000;
```

14. 背景颜色

```
background-color:red;
```



## CSS选择器

### 基础选择器

#### id选择器

```
#id名{

}
```



#### class选择器

同一个标签，可能同时属于多各类，用空格隔开。

> - class可以重复，也就是说，同一个页面上可能有多个标签同时属于某一个类
> - 同一个标签可以携多个类。

```css
.类名{

}
```



#### 标签选择器

```css
标签{

}
```



### 高级选择器

#### 后代选择器

```css
/*1.后代选择器必须用空格隔开
2.后代不仅仅是儿子，也包括孙子/重孙子，只要最终是放到指定标签中的都是后代*/
div p{

}
```

#### 子代选择器

```css
//1. 子代选择器只会查找儿子，不会查找其他被嵌套的标签
//2. 子代选择器之间需要使用“>”符号连接，并且不能有空格
div>p{

}
```

#### 交集选择器

```css
//作用：给所有选择器中的标签中，相交的那部分标签设置属性
//1. 选择器和选择器之间没有任何的连接符号
p.para1{

}
```

#### 并集选择器

```css
//作用：给所有选择器庄重的标签设置属性
//1. 并集选择器必须使用”,“来连接
.ht,para{

}
```

#### 兄弟选择器

```css
//1. 相邻选择器
//作用：给指定元素后面紧跟的那个选择器选中的标签设置属性
//相邻选择器必须通过”+“连接
//相邻选择器只能选中紧跟其后的那个标签，不能选中被隔开的标签
h1+p{

}

//2. 通用选择器
//作用：给指定选择器后面的所有选择器选中的所有标签设置属性（只选中后面的）
//通用选择器必须用”~“连接
//通用选择器选中的是指定选择器后面某个选择器选中的所有标签，无论有没有被隔开
h1~p{

}

```

#### 通配符选择器

```css
*{

}
```



### 序选择器

- CSS3中新增的选择器最具有代表性的就是序选择器

  - 同级别的第几个

  ```css
  p:first-child{    //选中同级别的第一个标签

  }

  p:last-child{    //选中同级别的最后一个标签

  }

  p:nth-child(n){    //选中同级别的第n个标签

  }

  p:nth-last-child(n){    //选中同级别的到数第n个标签

  }

  //注意点：不区分类型
  ```



  - 同类型的第几个

  ```css
  p:first-of-type{    //选中同级别中同类型的第一个标签

  }

  p:last-of-type{    //选中同级别中同类型的最后一个标签

  }

  p:nth-of-type(n){    //选中同级别中同类型的第n个标签

  }

  p:last-of-type(n){

  }
  //选中同级别中同类型的到数第n个标签


  ```




```css
p:only-child{    //选中父元素的唯一子元素

}
p:only-of-type{    //选中父元素唯一类型的某个标签

}
```



```css
p:nth-child(odd){  //选中同级别中的所有奇数

}

p:nth-child(even){  //选中同级别中的偶数

}

p:nth-child(2n+0){  //选中同级别中的偶数

}

p:nth-child(2n+1){  //选中同级别中的奇数

}


```





- 属性选择器



```
p[id]{	//根据指定的属性名称找到对应的标签，然后设置属性

}

p[class=para]{	//找到指定属性，并且属性的取值等于value的标签

}

//1. 属性的取值是以什么开头的
img[alt^=abc]{	//只能找到value开头，无论有没有被“-”隔开

}
img[alt|=abc]{	//只能找到value开头，并且value是被“-”和其他内容隔开的

}

//2. 属性的取值是以什么结尾的
img[alt$=abc]{

}

//3. 属性的取值时候包含某个特定的取值
img[alt*=abc]{

}
img[alt~=]{	//只能找到被空格隔开的

}

```











### 结构性链接伪类选择器

> a:link--正常：未访问过的链接的样式
>
> a:visited--用户已经访问过的链接的样式
>
> a:hover--当用户鼠标放在链接上时（悬停）
>
> a:avtive--链接被点击的那一刻（长按）
>
> love hate（爱恨原则，必须按照一定的顺序编写）
>
> a标签在使用的时候，我们一定要将a标签写在前面，:link、:visited、hover这些伪类写在后面。
>
> 记住，所有的a不继承text、font这些东西，因为a自己有一个伪类的权重。



- 伪元素选择器（添加的是一个行内元素）

> 伪元素选择器作用就是给指定的标签的内容前面添加一个子元素或者给指定标签的内容后面添加一个子元素
>
> ```css
> div::before{
>     content: "爱你";
>     width: 50px;
>     height: 50px;
>     background-color: pink;
>     display: block;（转换为块级元素）
>     visibility: hidden;（隐藏添加的内容）
> }
>
>
> div::after{
>     content: "爱你";
>     width: 50px;
>     height: 50px;
>     background-color: pink;
>     display: block;
> }
> ```
>
>







## CSS三大特性

### 继承性

> 作用：给父元素设置一些属性，子元素也可以使用，这个我们就称之为继承性。
>
> 注意点：
>
> - 并不是所有的属性都可以继承：只有以color/font-/text-/line-开头的属性才可以继承
> - 这些关于样式的，都能够继承；所有关于盒子的、定位的、布局的属性都不能继承。*- /0
> - 在CSS继承中不仅仅是儿子可以继承，只要是后代都可以继承
> - 继承性中特殊性
>   - a标签文字颜色和下划线是不可以继承的
>   - h标签的文字大小是不能继承的
>
> 应用场景：
>
> 一般用于设置网页上的一些共性信息，例如网页的文字颜色，字体，文字大小等内容。
>
> ```css
> body{
>     
> }
> ```



### 层叠性

> 什么是层叠性：
>
> 层叠性就是就是CSS处理冲突的一种能力
>
> 注意点：层叠性只有多个选择器选中“同一个标签”，然后又设置了“相同的属性”，才会发生层叠性。
>
> - 选择上了，数权重（id数量，类的数量，标签的数量）。如果权重一样，谁写在后面听谁的。
> - 没有选择上，通过继承影响的，就近原则，谁描述的近听谁的。如果描述的一样近，比选择器权重，如果权重再一样重，谁写在后面就听谁的。
>
> **注意**：同一个标签，携带了多个类名，有冲突：和在标签中的类名的顺序无关，只和CSS的顺序有关
>
> ```html
> .spec2{
>     color:blue;
> }
> .spec2{
>     color:red;
> }
>
> <p class="spec1 spec2">我是什么颜色？</p>
> <p class="spec2 spec1">我是什么颜色？</p>
> <!--显示为红色-->
> ```
>
> !import关键字：给一个属性提高权重，这个属性的权重就是无限大。一定要注意格式。
>
> **注意**：
>
> - !import提升的是一个属性，而不是一个选择器。
> - !import无法提升继承的权重
> - !import无法影响就近原则
>
> ```css
> color:green !inmport;
> ```
>
>





### 优先级

> 1. 什么是优先级：
>
> 作用：当多个选择器选中同一个标签，并且给同一个标签设置相同的属性
>
> 2. 优先级判断的三种方式
>
>    1. 是不是直接选中（间接选中就是继承：间接选中：谁离目标标签比较近就听谁的）
>    2. 是否是相同的选择器：如果都是直接选择器，并且都是同类型的选择器，那么就是谁写在后面就听谁的
>    3. 不同选择器：如果都是直接选中，并且不是相同类型的选择器，那么就会按照选择器的优先级来层叠
>
>    ==id>类>标签>通配符>继承>浏览器默认==
>
>
> 什么是：!important
>
> 作用：用于提升某个直接选中标签的选择器中的某个属性的优先级的，可以将被指定的属性的优先级提升为最高
>
> 注意点：
>
> - !important只能用于直接选中，不能用于间接选中
> - 通配符选择器选中的标签也是直接选中的
> - !important只能提升被指定的属性的优先级，其它的属性的优先级不会被提升
> - !important必须写在属性值的分号前面
> - !important前面的感叹号不能省略
>
> ```
> p{
>     color:red !important;
> }
> ```
>
>
>
> 权重问题：
>
> 1. 什么是优先级的权重
>    1. 作用：当多个选择器混合在一起使用时，我们可以通过计算权重来判断谁的优先级最高
>    2. 权重的就算
>       1. 首先计算选择器中有多个id，id多的选择器的优先级最高
>       2. 如果id个数一样，那么再看类名的个数，类名个数多的优先级最高
>       3. 如果类名个数一样，那么再看标签名称的个数，标签名称个数多的优先级最高
>       4. 优先级一样，采用最近原则
>    3. 注意点：只有选择器是直接选中标签的才需要计算权重





## CSS显示模式

> 在HTML将所有的标签分为两类，分别是容器集标签和文本级标签
>
> 在CSS中也将所有的标签分为两类，分别是块级元素和行内元素
>
>
>
> - 什么是块级元素？什么是行内元素？
> - - 块级元素独占一行（所有的容器级标签）
>   - 行内元素不会独占一行（除了p，h元素的文本级标签）
> - 块级元素和行内元素的区别
> - - 块级元素
>   - - 独占一行
>     - 如果没有设置宽度，就默认和父元素一样宽（100%）
>     - 如果设置了宽高，那么就按照设置的来显示
>   - 行内元素
>     - 不会独占一行
>     - 如果没有设置宽度，就和内容一样宽
>     - 行内元素不可以设置宽度高度
>   - 行内块级元素
>     - 为了能够元素既能够不独占一行，又可以设置宽度和高度，那么就出现了行内块元素
>
> 模式转换：
>
> ```css
> display：inline(行内元素)、inline-block(行内块元素)、block(块级元素)
> ```
>
> ------
>
> 普通流有哪些性质：
>
> 1. 空白折叠现象：只有行内元素才有这个现象
>    1. 比如，如果我们想让img标签之间没有空隙，必须紧密连接：
>
> ```html
>
> ```
>
>
>
> 2. 高矮不齐，底边对齐
> 3. 自动换行，一行写不满，换行写









## CSS背景

- background-color（背景颜色）

```css
body {background-color:#b0c4de;}
```

> css中，颜色值通常以下方式定义：
>
> 十六进制-如：#ff0000
>
> RGB-如：rgb(255,0,0)
>
> 颜色名称：-如：red

- background-image（背景图片）

```css
body {background-image:url('paper.gif');}
```

> 默认情况下，背景图像进行了平铺重复显示，覆盖整个实体

- background-repeat（背景平铺）

> 默认请款下background-image属性会在页面的水平或者垂直方向平铺
>
> ```css
> background-repeat: repeat-x（在水平方向上平铺） / repeat-y（在垂直方向上平铺） / no-repeat（不平铺） /repeat（默认，在水平和垂直都需要平铺）
> ```

1. background-attachment（背景滚动）

> 关联方式：
>
> 默认情况下，背景图片会随着滚动条的滚动而滚动，如果不想让背景图片随着滚动条滚动而滚动，那么我们可以修改背景图片和滚动条的关联方式
>
> ```css
> background-attchment: scroll(默认值，会随着滚动条的滚动而滚动)、fixd（不会随着滚动条的滚动而滚动）
> ```
>
>



- background-position（背景定位）--常用的设置值为：background-position: center top；

```css
background-position: top center;
第一个值是水平方向
第二个值是垂直方向
水平方向取值：right、center、left
垂直方向取值：top、center、bottom
也可以是具体的像素值（正值负值都可以）

经常设置为：background-position: center top;
```

- 背景简写

```css
background: 颜色 图像 是否平铺 是否滚动 定位
设置的顺序为：
background-color
background-image
background-repeat
background-attachment
background-position
```

### 背景尺寸

> ```css
> //第一个参数：宽度
> //第二个参数：长度
> background-size: 100px 100px;
>
> ```
>
> ```css
> //背景图片的当前元素的百分比
> background-size: 50% 50%;
> ```
>
> ```css
> //等比拉伸
> background-size: auto1 50%;
> ```
>
> ```css
> //cover含义：告诉系统徐娅萍图片等比拉伸，
> //需要拉伸到宽度和高度都填满元素（填满两边）
> background-size: cover;
> ```
>
> ```
> //container含义：告诉系统图片需要等比拉伸
> //需要拉伸到宽度或高度都填满元素（填满一边），
> background-size: container;
> ```
>
>

### 新增属性

#### background-orign

```css
//告诉系统背景图片从什么区域开始，默认请款下从padding区域开始显示
backgroundp-orign: padding-box;
//从border开始
backgroundp-orign: border-box;
//从content开始
backgroundp-orign: content-box;
```

#### background-clip

> 规定背景的绘制区域

```css
//背景绘制区域属性是专门用于指定从哪个区域开始绘制背景的，默认请款下会从border区域开始绘制的（其他没有的地方不会显示）
//从padding开始绘制
backgroundp-clip: padding-box;
//从border开始
backgroundp-clip: border-box;
//从content开始
backgroundp-clip: content-box;
```

### 多重背景

> 多张背景图片用逗号隔开，先添加的图片会盖住后添加的背景图片
>
> 建议在编写的多重背景拆开编写

```css
background: url("") no-repeat left top,url("") no-repeat right top;
```





## CSS精灵

> 1. 什么是CSS精灵图
>
> CSS精灵图是一种图像合成技术
>
> 2. CSS精灵图作用
>
> 可以减少请求的次数，以及降低服务器请求次数
>
> 3. 如果使用CSS精灵图
>
> CSS的精灵图需要配合背景图片和背景定位来使用







## CSS列表（在ul标签上设置）

- 无序列表

```css
list-style-type: circle、square、none
```

- 有序列表

```css
list-style-type: upper-roman、lower-alpha
```

- 作为列表项标记的图像

```css
list-style-image: url("");
```

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
<style>
ul
{
	list-style-type:none;
	padding:0px;
	margin:0px;
}
ul li
{
	background-image:url(sqpurple.gif);
	background-repeat:no-repeat;
	background-position:0px 5px;
	padding-left:14px;
}
</style>
</head>

<body>
<ul>
<li>Coffee</li>
<li>Tea</li>
<li>Coca Cola</li>
</ul>
</body>

</html>
```



## CSS表格

- 表格边框

```css
table{
 	border: 1px solod black;   
}

```

- 折叠边框

```css
table{
    border-collapse: collapse;
}
```

- 表格宽度和高度

```css
table{
    width: 100px;
    height: 100px;
}
```

- 表格文字对齐

```css
td{
    text-align: right;
    vertical-align:bottom
}
```

- 表格填充

```css
td{
    padding:15px;
}
```

- 表格颜色

```css
table{
    color:red;
}
```





## CSS盒子模型（Box Model）

- 盒模型组成：
  - 外边距：margin
  - 边框：border
  - 内边距：padding（内边距会撑开盒子）
  - 内容：content
  - 宽度和高度：height、width
- 元素宽度计算
  - 总元素的宽度=宽度+左填充+右填充+左边框+右边框+左边距+右边距
- 元素高度计算
  - 总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距

> #### 内边距
>
> 什么是内边距：
>
> 边框和内容之间的距离
>
> padding的区域有背景颜色，也就是说，backgroud-color将填充border区域内
>
> 格式：
>
> ```css
> //连写
> padding:上 下 左 右;
> padding:上 左右 下
> padding:上下 左右
> padding:
> //非连写：
> padding-top：
> padding-right:
> padding-bottom:
> padding-left:
> ```
>
> #### 外边距
>
> 什么是外边距：
>
> 标签和标签之间的距离
>
> 格式
>
> ```css
> //连写
> margin:上 下 左 右;
> margin:上 左右 下
> margin:上下 左右
> margin:四条边
> //非连写：
> margin-top：
> margin-right:
> margin-bottom:
> margin:left:
> ```
>
> 外边距的合并（塌陷）现象（注意：只有在标准文档流中）
>
> - 水平合并：左右相加
> - 垂直合并：默认情况下外边距是不会叠加的，会出现合并现象，谁的外边距大就为谁的
>
>
>
> #### 注意点：
>
> - 嵌套盒子里面：首先考虑padding其次考虑margin
> - 在嵌套关系的盒子中，我们可以利用margin: 0 auto 的方式来让里面的盒子在外面的盒子水平居中。（水平方向有效）
> - 使用margin:0 auto;的盒子，必须有**width**，有明确的width。
> - 只有标准流的盒子才能使用margin:0;居中。当一个盒子浮动了，绝对定位，固定定位了，都不能使用margin:0;。
> - margin:0 auto；是居中盒子，不是居中文本。文本居中要使用text-align:center；。
>
>
>
> #### 盒子模型
>
> - 所有的标签都可以设置宽度、高度、外边距、内边距、边框
> - 所有的标签都是盒子模型
>
>
>
> #### 盒子模型的宽度和高度
>
> - 内容的宽度和高度
> - 就是通过标签的width / height属性设置的宽度和高度
> - 元素的宽度和高度
> - 宽度=左右边框+左右内边距+宽度
> - 高度=上下边框+上下内边距+高度
> - 盒子的宽度和高度
> - 宽度=左右边框+左右内边距+左右外边距+宽度
> - 高度=上下边框+上下内边距+上下外边距+高度
>
>
>
> #### 注意
>
> - 增加了padding之后元素的宽高也会发生变化
> - 如果增加了border之后，还想保持元素的宽高，就必须减去内容的宽高。
> - 如果想保持一个盒子的真实占有宽度不变，那么加width就要减padding。加padding就要减width。
>
>
>
> **注意**：
>
> 嵌套盒子里面，如果给子盒子使用margin-top属性，父盒子也会跟着移动。可以给父盒子加border，或者使用padding属性
>
>
>
> ### box-sizing属性
>
> CSS3中新增了一个box-sizing属性，这个属性可以保证我们给盒子新增padding和border之后，盒子元素的宽度和高度不变
>
> box-sizing属性是如何保证增加了padding和border之后，盒子元素的宽度和高度不变
>
> （1）增加了padding和border之后，要想保证盒子元素的宽高不变，就必须减去一部分内容的宽度和高度
>
> ```
> box-sizing: border-box（恒等于width和height）、content-box（元素的宽高=边框+内边距+内容宽高）
> ```
>
>
>
>
>
>





## CSS 边框（border）

```css
border-style: dotted（点线）、dashed（虚线）、double（两个边框）、groove（定义3D沟槽边框）、ridge（定义3D脊边框）、inset（定义一个3D的潜入边框）、outset（定义一个3D突出边框）
//四条边连写
border: 边框的样式 边框的宽度 边框的颜色;
//四条边分开写
border-top: 边框的样式 边框的宽度 边框的颜色;
border-right: 边框的样式 边框的宽度 边框的颜色;
border-bottom: 边框的样式 边框的宽度 边框的颜色;
border-left: 边框的样式 边框的宽度 边框的颜色;

//连写（分别设置四条边的边框）
border-width: 上 右 下 左;
border-color: 上 右 下 左;
border-style: 上 右 下 左;

//分开写四条边
border-top-style:
border-top-color:
border-top-width:

border-right-style:
border-right-color:
border-right-width:

border-bottom-style:
border-bottom-color:
border-bottom-width:

border-left-style:
border-left-color:
border-left-width:

border: none（取消边框）
```



## CSS轮廓（outline）

> - outline
> - outline-color
> - outline-widht
> - outline-style

```css
p{
    outline: 1px solid red;
}
```



## CSS显示和隐藏

### display显示和隐藏

> display: none 可以隐藏某个元素，且隐藏的元素不会占用空间。也就是说，该元素隐藏了原本占用的空间也会从页面布局中消失

```css
//显示
display: block;
//隐藏
display: none;
```

### visibility显示和隐藏

> visibility: hidden可以隐藏某个元素，当隐藏的元素仍然占用空间。

```css
//显示
visibility: visible;
//隐藏
visibility: hidden;
```



## CSS浮动

```css
float: left（左浮动）、right（右浮动）
```



> 浮动的性质：**`脱标、贴边、字围、收缩`**
>
> ------
>
>
>
> ### 什么是浮动元素脱标
>
> - 脱标：就是脱离标准流
> - 当某一个元素浮动之后，那么这个元素看上去就像被从标准流中删除了一样，这就是浮动的脱标
>
> 证明：
>
> - 一个行内元素（span）标签不需要转成块级元素，就能够设置宽度、高度了。所以能够证明一件事儿。就是所有标签已经不区分行内、块级了。也就是说，一旦一个元素浮动了，那么，将能够并排了，并且能够设置宽高了。
>
> ### 浮动元素脱标之后会有什么影响
>
> - 如果前面一个元素浮动了，而后面一个元素没有浮动，那么这个时候前面的一个就会盖住后面的一个元素
> - 浮动的元素有相互贴靠的现象
> - 浮动元素的字围现象：图文混排（图片浮动，文字围绕图片）
>
> ### 浮动元素的排序规则
>
> - 相同方向上的浮动元素，先浮动的元素会显示在前面，后浮动的元素会显示在后面
> - 不同方向上的浮动
>
>   - 左浮动会找左浮动
>   - 右浮动会找右浮动
> - 浮动元素浮动之后的位置，由浮动元素浮动之前在标准流中的位置来确定
>
>
>
> 在浮动流中浮动的元素是不可以撑起父元素的高度。
>
>
>
>
>
> ### 清除浮动
>
> 1. 给浮动的元素的祖先元素加高度
>
> - ##### 给后面的父盒子添加clear属性
>
> ```css
> clear: none（默认取值，按照浮动元素的排序规则来排序）、left（不要找前面左浮动元素）、right（不要找前面右浮动元素）、both（不要找前面的左浮动和右浮动元素）
> 注意：margin会失效
> ```
>
> - ##### 额外标签法（样式在此标签写）
>
>   - 外墙法（两个大父级元素中间）
>     - 在两个盒子中间添加一个额外的块级元素
>     - 给这个额外标签的块级元素设置clear:both
>     - 注意点：
>       - 外墙法可以让第二个盒子使用margin-top属性
>       - 外墙法不可以让第一个盒子使用margin-bottom属性
>   - 内墙法（第一个父盒子的子元素的最后面）
>     - 在两个盒子中间添加一个额外的块级元素
>     - 给这个额外标签的块级元素设置clear:both
>     - 注意点：
>       - 内墙法可以让第二个盒子使用margin-top属性
>       - 内墙法可以让第一个盒子使用margin-bottom属性
>
>   - 外墙法和内墙法区别：
>     - 外墙法不可以撑起第一个盒子的高度
>     - 内墙法可以撑起第一个盒子的高度
>
> - ##### 伪元素清除浮动（给父元素添加）
>
> ```css
> .clearfix::before{
>     content: "";
>     display: block;
>     height: 0;
>     visibility: hidden;
>     clear: both;
>      *zoom: 1;（兼容IE6）
> }
>
> ```
>
> ------
>
> overflow清除浮动
>
> 本意：清除溢出到盒子外面的文字
>
> 一个父亲不能被自己浮动的儿子，撑出高度，但是，只要给父亲加上overflow:hidden;那么，父亲就能被儿子撑出高度。
>
> ```css
> .clearfix{
>     overflow: hidden;
>     *zoom: 1;（兼容IE6）
> }
> ```
>
> ------
>
> 总结：
>
> - 加高法：浮动的元素，只能被有高度的盒子关注。也就是说，如果盒子内部有浮动，这个盒子有高，那么妥妥的，浮动不会相互影响。但是，工作上，我们绝对不会给所有的盒子加高度，这是因为麻烦，并且不能适应页面的快速变化。所以，我们就要找到，不给盒子加高度，但是也能清除浮动的方法。
> - clear:both法：最简单的清除浮动的方法，就是给盒子增加clear:both;表示自己的内部元素，不受其他盒子的影响。浮动确实清除了，不会相互影响。但是有一个问题，就是margin失效。两个盒子之间，没有任何的间隙了。
> - 隔墙法（额外标签法）：
>   - 外墙法：在两部分浮动元素中间，建一个墙。隔开两部分浮动，让后面的浮动元素，不去追前面的浮动元素。墙用自己的身体当做了间隙。我们发现，隔墙法好用，但是第一个盒子还是没有高度。如果我们现在想让第一个div，自动的根据自己的儿子，撑出高度，我们就要想一些小技巧：“奇淫技巧”。
>   - 内墙法：内墙法优点，不仅仅能够清除浮动，并且第一个盒子的高度能够撑开。这样，这个盒子的背景、边框就能够根据高度来撑开了。
> - overflow:hidden：这个属性的本意，就是将所有溢出盒子的内容，隐藏掉，但是，我们发现这个东西能够用于浮动的清除。我们知道，一个父亲，不能被浮动的儿子撑出高度，但是，如果这个父亲加上了overflow:hidden；那么这个父亲就能够被浮动的儿子撑出高度了。这个现象，不能解释，就是浏览器的偏方，能够使用margin。



## CSS定位（position）

### 静态定位(static)

> 元素默认定位就是静态定位
>
> 静态定位不会受到top、buttom、left、right影响
>
> ```css
> position: static
> ```
>
>



### 固定定位（fixed）

> 固定定位的元素相对于浏览器窗口是固定位置。即使窗口是滚动的它也不会移动。
>
> ```css
> position: fiexd;
> ```
>
> 注意：
>
> 脱离标准流，不占据标准流空间
>
> 固定定位和绝对定位一样，不区分行内块/行内/块级元素
>
> 不随着滚动条的滚动而滚动
>
> 固定定位使元素的位置与文档流无关，因此不会占据空间
>
> 固定定位的元素和其他元素重叠



### 相对定位（relative）

> - 相对定位的元素不会脱离文档流（top、left、right、bottom相对于原来自己位置移动）
>
> - 同一个方向上的定位属性使用一个
>
> - 相对定位中区分块级元素/行内元素/行内块元素
>
> - 由于相对定位不脱离文档流，所以给相对定位的元素设置margin/padding等属性的时候会影响到标准流的布局
>
> ```css
> position: relative;
> ```
>
> 应用场景：
>
> - 位置微调
> - 配合绝对定位使用



### 绝对定位（absulute）



>
>
> 绝对定位：脱离文档流，因此不占据空间
>
> - 相对于body来定位（没有设置父相子绝）
>
>   - 如果是以body作为参考点，那么其是以网页首屏的宽度和高度作为参考点，而不是以整个网页的宽度和高度作为参考点
>   - 绝对定位的元素，会忽略祖先元素的padding
>
>
> ```css
> position:absolute;
> ```
>
> - 绝对定位的元素脱离标准流
> - 绝对定位的元素不区很块级元素/行内元素/行内块元素，都可以设置宽高
>
> 规律：
>
> - 默认情况下，所有的绝对定位的元素，无论有没有祖先元素，都会以body作为参考点。
> - 如果绝对定位的元素有祖先元素，并且祖先也是定位流，那么这个绝对定位的元素就会以定位流的那个祖先元素作为参考点。
>   - 只要是这个绝对定位元素的祖先元素都可以
>   - 定位流指的是绝对定位/相对定位/固定定位
>   - 定位流只有静态定位不行
> - 如果一个绝对地位的元素有祖先元素，并且祖先元素也是定位流，而且祖先元素中有多个元素都是定位流，那么这个绝对定位的元素会以离它最近的那个定位流的祖先为参考点
>
>
>
>
>
> ### 父相子绝
>
> 父元素用相对定位
>
> 子元素用绝对定位
>
>- 绝对定位的元素水平居中问题：
>
>```css
>left: 50%;
>marginleft: -元素宽度的一半
>```
>
>- 绝对定位的元素垂直居中问题：
>
>```css
>top: 50%;
>margintop: -元素宽度的一半
>```
>
>



### 粘性定位（sticky）

> 粘性定位：基于用户的滚动位置来定位。在position: relative与
>
> ```css
> position: sticky;
> ```
>
>



### z-index属性

> 只有定位了的元素，才能有z-index值，也就是说，，不管相对定位、绝对定位、固定定位都可以使用z-index值，而浮动的东西不能用。
>
> 默认情况下所有的元素都有一个默认的z-index属性，取值是0
>
> z-index的作用：
>
> 专门用于控制定位流元素的覆盖关系
>
> 1. 默认情况下定位流的元素会盖住标准流的元素
> 2. 默认情况下定位流的元素后面编写的会盖住前面编写的
>
> 注意点：
>
> - 如果两个元素的父元素都没有设置z-index属性，那么谁的z-index属性比较大谁就显示在上面
>
> - 如果两个父元素设置了z-index属性，那么子元素的z-index就会失效，也就是说谁的父元素z-index属性比较大谁就会显示在上面



## CSS过渡

> 过渡三要素：
>
> - 必须要有属性发生变化
> - 必须告诉系统哪个属性需要执行过渡效果
> - 必须告诉系统过渡效果持续时长
>
> ```css
>    /*告诉系统哪个属性需要执行过渡效果*/
>  transition-property: width,background-color;
> ```
>
> ```css
> /*告诉系统过渡效果持续的时长*/
> transition-duration: 5s,5s;
> ```
>
> ```c&#39;s&#39;s
> /*告诉系统延迟多少秒才开始执行过渡动画*/
> transition-delay: 2s;
> ```
>
> ```css
> /*告诉系统过渡动画的运动速度*/
> /* liear（匀速） ease（逐渐慢下来）ease-in（加速） easeout（减速）ease-in-out（先加速后减速）*/
> transition-timing-function: linear;
> ```
>
> ```css
> /*过渡属性 过渡时间 过渡时长 延迟时间*/
> /*多个属性可以用逗号隔开*/
> /*可以省略后面两个属性*/
> transition: all 5s linear 0s;
> ```
>
> 注意点：
>
> - 当多个属性需要同时执行过渡效果时用逗号隔开即可
>
> ```css
>     <style>
>         div{
>             width: 100px;
>             height: 50px;
>             background-color: red;
>             /*告诉系统哪个属性需要执行过渡效果*/
>             transition-property: width,background-color;
>             /*告诉系统过渡效果持续的时长*/
>             transition-duration: 5s,5s;
>              /*告诉系统延迟多少秒才开始执行过渡动画*/
>             transition-delay: 2s;
>             /*告诉系统过渡动画的运动速度*/
>               transition-timing-function: linear;
>         }
>         div:hover{
>             width: 300px;
>             background-color: blue;
>         }
>     </style>
> ```
>
>





## CSS 2D

### 旋转

```css
transsform: rotate(45deg);
```

### 平移

```
//第一个参数是水平移动
//第二个参数是垂直移动
transform: translate(100px 0);
```

### 缩放

```css
//等于1：不变 大于1：放大 小于1：缩小
//第一个参数：水平方向
//第二个参数：垂直方向
//第一个参数和第二个参数，只需要写一个
transform: scale(1,1.5);
```

### 综合

```
//如果需要进行多个转换，用空格隔开
//2D的转换模式会修改元素的坐标系，所以旋转之后再平移就不是水平平移
transform: rotate(45deg) translate(100px 0px) scale(1.5);
```





------



### 形变中心点

```css
//默认情况下所有的元素都是以自己的中心点作为参考来旋转的，，我们可以通过形变中心点属性来修改它的参考点
//第一个参数：水平方向
//第二个参数：垂直方向
//注意：取值（具体像素 百分比 特殊关键字:center center）
transform-orign: 0px 0px;
```



------

### 旋转轴向

```css
//默认为Z轴
transform: rotateZ(45deg);
//轴X
transform: rotateX(45deg);
//Y轴
transform: rotateY(45deg);
```

------



### 透视属性

```
//什么是透视：近大远小
//注意点：透视属性必须添加到需要呈现近大远小效果的元素的父元素上面
//500px的意思是距离多远观察这个物体
perspective: 500px;
```





## CSS阴影

### 盒子阴影

> 盒子的阴影分为内外阴影（默认为外阴影）
>
> 快速添加阴影只需要编写三个参数即可
>
> box-shdow: 水平偏移 垂直偏移 模糊度；
>
> 默认情况下盒子阴影的颜色和文字的颜色一样

```css
box-shadow: h-shadow（水平偏移） v-shadow（垂直偏移） blur（模糊度） spread（阴影扩散） color （阴影颜色）inset（内外阴影）;
box-shadow: 10px 10px 10px 10px skyblue inset;

```

### 文字阴影

```css
text-shadow: 10px 10px 10px black
text-shdow: h-shadow（水平偏移）v-shadow（垂直偏移） blur（模糊度）color （阴影颜色）
```

## CSS 3D

```css
//给父元素添加,让子元素有厚度
transform-style:flat（默认2D）、preserve-3d;
```

### 3D 转换模块-正方体

```css
  <style>
        *{
            padding: 0;
            margin: 0;
        }
        ul{
            width: 200px;
            height: 200px;
            border: 1px solid #000;
            box-sizing: border-box;
            margin: 100px auto;
            position: relative;
            transform: rotateY(0deg) rotateX(0deg);
            transform-style: preserve-3d;
        }
        li{
            list-style: none;
            width: 200px;
            height: 200px;
            font-size: 60px;
            text-align: center;
            line-height: 200px;
            position: absolute;
            left: 0;
            top: 0;
        }
        ul>li:nth-child(1){
            background-color:red ;
            transform: rotateX(90deg) translateZ(100px);
        }
        ul>li:nth-child(2){
            background-color: green;
            transform: rotateX(180deg) translateZ(100px);
        }
        ul>li:nth-child(3){
            background-color: blue;
            transform: rotateX(270deg) translateZ(100px);
        }
        ul>li:nth-child(4){
            background-color: yellow;
            transform: rotateX(360deg) translateZ(100px);
        }
        ul>li:nth-child(5){
            background-color: purple;
            transform: translateX(-100px) rotateY(90deg);
        }
        ul>li:nth-child(6){
            background-color: pink;
            transform: translateX(100px) rotateY(90deg);
        }
    </style>

<!--编写的顺序为上，后，下，前-->

<ul>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
    <li>5</li>
    <li>6</li>
</ul>

```



## CSS动画

> #### 动画和过渡的异同：
>
> - 相同
>   - 过渡和动画都是给元素元素添加动画的
>   - 过渡和动画需要满足三要素才会有动画效果
> - 不同
>   - 过渡必须人为的触发才会执行
>   - 动画自动执行
>
> #### 动画三要素
>
> - 告诉系统需要执行哪个动画
>
> ```css
> animation-name: 动画名称-Inj;
> ```
>
> - 告诉系统我们需要创建一个动画
>
> ```css
>  @keyframes Inj {
>             from{
>                 margin-left: 0;
>             }
>             to{
>                 margin-left: 500px;
>             }
>         }
> ```
>
> - 告诉系统动画持续的时长
>
> ```css
> animation-duration: 3s;
> ```
>
> #### 动画的其他属性
>
> - 动画延迟执行
>
> ```css
> animation-delay: 2s;
> ```
>
> - 动画执行速度
>
> ```css
> animation-timing-function: linear;
> ```
>
> - 动画执行次数
>
> ```css
> animation-iteration-count: 3、infinite;
> ```
>
> - 动画是否往返执行
>
> ```css
> animation-directon: normal(默认的，回到起点继续执行)、alternate（往返动画）;
> ```
>
> - 控制动画执行和暂停
>
> ```css
> animation-play-state: running（执行）、paused（暂停）;
> ```
>
> - 指定动画等待和结束状态的样式
>
> ```css
> animation-fill-mode: none(默认)、forwards(让元素等待状态下的时候显示动画第一帧的样式)、backwords(结束状态保持最后一帧)、both(让元素等待状态下的时候显示动画第一帧的样式，结束状态保持最后一帧)
> ```
>
>
>
> #### 创建动画的其他方式
>
> ```c&#39;s&#39;s
>  @keyframes Inj {
>             0%{
>                 top: 0;
>                 left: 0;
>             }
>             25%{
>                 top: 0;
>                 left: 300px;
>             }
>             50%{
>                 top: 300px;
>                 left: 300px;
>             }
>             75%{
>                 top: 300px;
>                 left: 0;
>             }
>             100%{
>                 top: 0;
>                 left: 0;
>             }
>         }
> ```
>
> #### 动画状态
>
> - 等待状态（延迟）
> - 执行状态
> - 结束状态
>
> #### 动画连写
>
> ```css
> animation: 动画名称 动画时长 动画运动速度 延迟时间 执行次数 往返动画;
> ```
>
>





## 网页排版

- 标准流（普通流/文档流）排版方式

> - 浏览器默认排版方式就是标准流
> - 在CSS中将元素分为三类，分别就是块级元素/行内元素/行内块元素
> - 在标准流中，有两种排版方式，一种是垂直排版，一种是水平排版
>   - 垂直排版：如果元素是块级元素，，那么就会垂直排版
>   - 水平排版：如果是元素行内元素/行内块元素，那么就会水平排版

- 浮动流排版方式

> - 浮动流是一种“半脱离标准流”的排版方式
> - 浮动流只有一种排版方式，就是水平排版，它只能设置某个元素左对齐或者右对齐
>
>
>
>
>
> 注意：
>
> - 在浮动流中是不区分块级元素/行内元素/行内块元素的，无论是块级元素/行内元素/行内块元素都可以水平排版
> - 在浮动流中，无论是块级元素/行内元素/行内块元素都可以设置宽高
> - 浮动中的元素和标准流中的行内块元素很像
>
>

- 定位流排版方式





# 兼容问题



1. IE6不支持小于12px的盒子（看起来比较大）

> 解决办法：将盒子的字号，设置小。比如0px。（像素小于盒子的高）
>
> ```css
> div{
>     width: 700px;
>     height: 4px;
>     /*针对IE6不支持小于12px的盒子*/
>     _font-size: 0;
>     backgound-color: red;
> }
> ```
>
>



2. IE6不支持用overflow:hidden;来清除浮动

> 解决办法：
>
> ```css
> _zoom:1;
> ```
>
>



3. 关于margin的IE6兼问题

> IE6双倍margin bug
>
> 当出现连续浮动的元素，携带和浮动方向相同的margin时，队首的元素，会双倍margin。
>
> 解决方案：
>
> （1）使浮动的方向和margin的方向，相反。（前端开发工程师，把这个当做习惯了）
>
> （2）使用hack
>
> ```html
> <style>
> 	*{
>         padding: 0;
>         margin: 0;
> 	}
> 	ul{
>         /*padding-left: 40px;*/
>         list-style: none;
>         height: 400px;
> 	}
> 	ul li{
>         float: left;
>         width: 120px;
>         height: 40px;
>         margin-left: 40px;
>         /*margin-right: 40px;*/
>         background-color: orange;
> 	}
>     /*单独给队首的外边距减一半*/
>     ul li.no1{
>         _margin-left:20px;
>     }
> </style>
>
> <body>
> 	<ul>
> 		<li class="no1"></li>
>         <li></li>
>         <li></li>
> 	</ul>
> </body>
> ```
>
>





4. IE6的 3px bug

> 解决办法：不用管，因为嵌套盒子不使用margin，使用padding。
>
> ```html
> <style>
> 	*{
>         padding:0;
>         margin:0;
> 	}
> 	div{
>         width:400px;
>         height:400px;
>         backgroud-color:orange;
> 	}
> 	div p{
> 		float:right;
> 		margin-right:10px;
>         widht:100px;
>         height:100px;
>         background-color:green;
> 	}
> </style>
>
> <body>
> 	<div>
> 		<p></p>
> 	</div>
> </body>
> ```
>
>





1.
2. 浏览器hack

> - 只要给css属性之前，加上下划线，这个属性就是IE6认识的专属属性（_）

```
div{
    width: 200px;
    height: 200px;
    border: 1px solid red;
    /*只要给css属性之前，加上下划线，这个属性就是IE6认识的专属属性*/
    _background-color: green;
}
```
