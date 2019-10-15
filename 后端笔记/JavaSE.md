# JavaSE

---



**JDK中包含JRE，JRE中包含JVM，所以开发的时候只需要安装JDK就行了。**




作为程序员要求掌握最基本的windows相关的DOS命令（DOS命令在DOS窗口编写DOS命令——打开DOS窗口：win键+r输入cmd就进入DOS命令窗口）：

- exit 推出当前DOS命令窗口

- cls 清楚屏幕：clear screen

- dir 列出当前目录下所有的子文件/子目录

- cd+目录的路径  命令进入该目录【change directory】

- cd ..  回到上级目录

- cd / 直接回到根目录

- d:回车 切换盘符

---

> 集成开发环境（IDE：Integrated Development Environment）
>
> 常用快捷键
>
> - Alt+/：内容辅助
> - Ctrl+D：删除选中行
> - syso+Alt+/：打出输出语句，

什么是软件工程师？是一种职位的名称，通常是通过计算机的某种编程语言完成软件的开发。

## Java基础介绍

**Java的加载与执行**

.java（Java源程序文件） --> .class（字节码文件） --> 类装载器 --> Java虚拟机（JVM） --> 操作系统

Java程序的运行包括念给非常重要的阶段：编译阶段、运行阶段

**编译阶段：**

- 编译阶段主要任务是检查Java源程序是否符合Java语法。符合Java语法则能够生成正常的字节码文件，不符合Java语法规则则无法生成字节码文件。（字节码文件中不是纯粹的二进制，这种文件无法在操作系统当中直接执行。）

- 编译阶段的过程：程序员需要在硬盘的某个位置<位置随意>新建一个.java扩展名的文件，该文件被称为Java源文件，源文件当中编写的是Java源代码/源程序。（而这个源程序是不能随意编写，必须符合Java语法规则<Java语法规则是需要记忆的>）

- Java程序员需要使用JDK当中自带的javac.exe命令进行Java程序的编译。（在DOS命令窗口中使用，Javac的使用规则：javac java源文件路径）

- javac是一个java编译器工具。（一个java源文件可以编译成多个.class文件）

- 字节码文件/.class文件是最终要执行的文件，所以说.class文件生成之后，java源文件删除并不会影响java程序的执行。但是一般java源程序不要删除，因为.class文件最终执行效果可能不是我们想要的，那么这个时候需要回头再重新修改java源文件，然后将java源程序重新编译生成新的class文件，然后再运行这个class程序，生成新的效果。

- 编译结束之后，可以将.class文件拷贝到其他操作系统当中运行。【跨平台】

**运行阶段**

- JDK安装之后，除了自带一个javac.exe之外，还有另一个工具/命令，叫做java.exe，java.exe命令主要负责运行阶段。（在DOS命令窗口中使用，java 类名，例如，磁盘上有一个A.class，那么就这样用：java A）
- 运行阶段的过程是：
 - 打开DOS命令窗口
 - 输入， java A
 - java.exe命令会启动Java虚拟机，JVM会启动类加载ClassLoader
 - ClassLoader会去硬盘上搜索A.class，找到该文件则将该字节码文件装载到JVM中
 - JVM将A.class字节码解释成二进制101010101这样的数据
 - 然后操作系统执行二进制和底层硬件平台进行交互



---

> #### 什么是软件：
>
> 软件：一系列按照特定顺序组织组织的计算机数据和指令的集合。
>
> #### 常见的软件：
>
> - 系统软件（直接和硬件交互的软件）：DOS、window、Linux
> - 应用软件（应用软件通常运行在系统软件中）：扫雷、迅雷
>
> #### 软件开发：制作软件
>
> #### 交互方式
>
> - 图形化界面（Graphical User Interface GUI）这种方式简单直观，使用者易于接收，容易上手操作。
> - 命令行方式（Command Line Interface CLI）需要有一个控制台，输入特定的指令，让计算机完成一些操作。
>
> #### 计算机语言
>
> 人与计算机交流的方式（Java、C、C++）
>
> #### 计算机语言发展史
>
> 1. 第一代：机器语言
>
> 每一个计算机只能理解他自己的机器语言，机器语言对于计算机来说就是自然语言了，由计算机的设计者定义。机器语言通常由数字组成。主要编写二进制编码
>
> 2. 第二代：低级语言（汇编语言）
>
> 程序开始使用英文的缩写来助记符来表示基本的计算机操作。这些助记构成了汇编语言的基础。
>
> 3. 第三代：高级语言
>    1. 面向过程：C、fortran、COBOL、PASCAL、ADA、
>    2. 面向对象：java、c++
>
> ------
>
> SUN公司：美国SUN（Stanford University Network）
>
> JAVA发明人：James Gosling
>
> 年份：1996年
>
> ------
>



#### Java语言概述

- 是SUN（Stanford University Network，斯坦福大学网络公司）1995年推出的一门高级编程语言。
- 是一种面向Internet的编程语言。
- 随着Java技术在web方面的不断成熟，已经成为web应用程序的首选开发语言。
- 简单易学，完全面向对象，安全可靠，与平台无关的编程语言。

------



#### Java语言的三种技术架构

- `JavaEE`（Java 2 Platform Enterprise Edition）企业版

> 是为开发企业环境下的应用程序提供提供的一套解决方案。
>
> 该技术体系包括的技术如：`Servlet`、`Jsp`等，主要针对于web应用程序开发。

- `JavaSE`（Java 2 Platform Standard Edition）标准版

> 是为开发普通桌面和商务应用程序提供的解决方案
>
> 该技术体系是其他两者的基础，可以完成一些桌面应用程序开发。

- `JavaME`（Java 2 Platform Micro Edition）微型版

> 是为开发电子消费产品和嵌入式设备提供的解决方案。
>
> 该技术体系主要应用于小型电子消费产品，如手机中的应用程序等。

------





> #### Java语言的特性
>
> - 跨平台性：安装虚拟机就可以跨平台
> - 简单性：相对而言的，例如Java中不再支持多继承，C++是支持多继承的，多继承比较复杂，C++中有指针，Java中屏蔽了指针的概念，所以相对来说Java是简单的。Java语言底层是C++实现的，不是C语言。
> - 面向对象：Java是纯面向对象的
> - 多线程
> - 健壮性：和自动垃圾回收机制有关，自动垃圾回收机制简称GC机制。Java语言运行过程中产生的垃圾是自动回收的，不需要程序员关心。
> - 安全性

------




#### Java语言搭建

- `JRE`：（Java Runtime Environment Java运行环境）

> 包括Java虚拟机（Java Virtual Machine JVM）和Java程序所需的核心类库等，如果想要运行一个开发好的Java程序，计算机只需要安装JRE即可。

- `JDK`：（Java Development Kit Java开发工具包）

> JDK提供给Java开发人员使用的，其中包含了java的开发工具，也包括了JRE，所以安装了JDK就不用在单独安装JRE了。
>
> 其中开发工具包括：编译工具（java.exe）、打包工具（jar.exe）

- `JVM`：（Java Virtual Machine Java虚拟机）

------



#### Java环境搭建

网址：https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

环境安装：

> - 点击系统变量下面的新建按钮，变量名JAVA_HOME（代表你的JDK安装路径），值对应的是你的JDK的安装路径。
>
> ```c
> JAVA_HOME
> C:\Program Files\Java\jdk1.8.0_191
> ```
>
>
>
> - 继续在系统变量里面新建一个CLASSPATH变量，对应的值为：（JDK 5.0以后不用配置此选项）
>
> ```c
> CLASSPATH
> .;%JAVA_HOME%\lib;%JAVA_HOME\lib\tools.jar%
> ```
>
> - 在你的系统变量里面找一个变量名是PATH的变量，需要在它的值域里面追加一段如下的代码：
>
> ```c
> ;%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;
> ```



> JDK目录介绍：
>
> - bin：该目录下存放了很多命令，例如：javac.exe（负责编译）和java.exe（负责运行）

测试安装

```c
java -version
```

------

#### JDK 7.0新增特性

> - 二进制整数
>
> 使用ob表示二进制
>
> ```java
> int a=0b000_0000_0000_0000_0000_0000_0000_0011;
> ```
>
> - 下划线分割符
>
> ```java
> public class TestBinaryNum {
> 	public static void main(String[] args) {
> 		
> 		int b=1_2312_3131;
> 		System.err.println(b);
> 	}
>
> }
> ```
>
>

#### Hello World初体验

```java
public class HelleWorld {
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		System.out.print("Hello World!!");
	}
}
```

- `****进入文件目录`****
- **`javac HelloWorld.class  ---->（编译层字节码）`**
- **`java HelloWorld----（运行字节码文件）**`

> 总结：
>
> （1）java对大小写敏感
>
> （2）main方法是java应用程序的入口方法，固定格式为：
>
> ```java
> public static main(String[] args){
>     //...
> }
> ```
>
> （3）在Java中，花括号划分程序的各个部分，任何方法的代码都必须以`"{"`开始，以`"}"`结束
>
>



## Java语言组成基础



> #### 关键字
>
> 特点：关键字都是小写
>
> ------
>



#### 标识符

作用：给变量、类和方法命名

命名规则

> - 标识符必须以字母、数字下划线_，美元符号$开头。
> - 标识符的其它部分可以是字母、下划线”_“、美元符号”$“和数字的任意组合。
> - Java标识符大小写敏感，且长度无限制。
> - 由26个英文字母大小写、数字0-9、符号、_、$组成
> - **数字不可以开头**
> - **不可以使用关键字**
> - 变量名尽量有意义
> - 驼峰命名法

------

#### 字符集简介

> - ISO8859-1
>
> 西欧字符集
>
> - GB2312
>
> 大陆使用最早、最广的简体中文字符
>
> - GBK
>
> GB2312的扩展，可以表示繁体中文
>
> - GB18030
>
> 最新GBK的扩展，中国所有非手持/嵌入式计算机系统的强制实施标准，可以表示汉字、维吾尔文、藏文等中华民族字符
>
> - Unicode
>
> 国际通用字符集





#### 注释

用于注解说明解释程序的文字就是注释

提高代码的阅读性

注释格式：

- 单行注释

```java
//注释内容
```

- 多行注释

```java
/*
* 注释内容
*/
```

------



常量和变量

常量

> 常量表示不能改变的数值
>
> **常量的分类**
>
> - 整数常量
> - 小数常量
> - 布尔型常量
> - 字符常量
> - 字符串常量
> - null常量
>
> **对于整数，四种表示形式**
>
> - 二进制：0,1 满2进1
> - 八进制：0-7 满8进1 用0开头表示
> - 十进制：0-10 满10进1
> - 十六进制：0-9，A-F 满16进1 用0x开头

------

#### 变量

> java是一种强类型语言，每个变量都必须声明其类型。
>
> java变量是程序中的最基本的存储单元，其要素包括变量名，变量类型和作用域
>
> 变量在使用前必须对其声明，只有在变量声明以后，才能为其分配相应长度的存储单元，声明格式为：
>
> ```
> 变量类型 变量名字=初始化值;
> ```
>
> 注意事项：
>
> - 每个变量都有类型，类型可以是基本类型，也可以是引用类型。
>
> - 变量名必须是合法的标识符
>
> ------
>
> 变量的概念：
>
> - 内存中的一个存储区域
> - 该区域有自己的名称（变量名）和类型（数据类型）
> - 该区域的数据可以在同一类型范围内不断变化
>
> 为什么定义变量
>
> - 用来不断的存放同一类型地常量，并可以重复使用
>
> 使用变量注意：
>
> - 变量的作用范围（一对{}有效）
>
> 定义变量的格式：
>
> - `数据类型 变量名=初始化值;`
>
>   ```java
>   byte b=8;
>   //结尾必须加L
>   long l=1354444L;
>   //结尾必须加f
>   float f=2.3f
>   ```
>





#### 数据类型

> Java语言是强类型语言，对于每一种数据都定义了明确的具体数据类型，在内存中分配了不同大小的内存空间。
>
> 数据类型
>
> - 基本数据类型（共6种）
>   - 数值型：整数类型（byte、short、int、long）、浮点类型（float、double）
>   - 字符型（char）
>   - 布尔型（boolean）
> - 引用数据类型
>   - 类（class）
>   - 接口（interface）
>   - 数组（[]）
>
> 1. 使用总结：默认是double，浮点数存在舍入误差，很多数字不能精确表示。如果需要进行不产生舍入误差的精确数字计算，需要使用BigDecimal
>
> 2. 科学计数法：e表示10的多少次方，e-2表示10的-2次方，e2表示10的2次方
>
> 3. 整数默认：int、小数默认（double）
> 4. 单引号用来表示字符常量。例如：`‘A’`是一个字符，它与`“A”`是不同的，`“A”`表示含有一个字符的字符串
> 5. char类型用来表示Unicode编码中的字符
> 6. boolean类型有两个值，true和false
> 7. boolean类型用来判断逻辑条件，一般用于流程控制实践
>
> |  类型   | 占用存储空间 | 表示范围 |
> | :-----: | :----------: | :------: |
> |  byte   |    1字节     |          |
> |  short  |    2字节     |          |
> |   int   |    4字节     |          |
> |  long   |    8字节     |          |
> |  float  |    4字节     |          |
> | double  |    8字节     |          |
> |  char   |    2字节     |          |
> | boolean |     1位      |          |
>
> ```java
> public class TestDataType {
> 	public static void main(String[] args) {
> 		int a=10;
>         /*使用long的时候需要加上L*/
>         long b=111111111111111111L;
> 		/*转换为二进制*/
> 		System.out.println(Integer.toBinaryString(a));
> 		/*转换为十六进制*/
> 		System.out.println(Integer.toOctalString(a));
> 		/*转换为十进制*/
> 		System.out.println(Integer.toHexString(a));
> 	}
> }
>
> ```
>
> ```java
> public class TestFloatType {
>
> 	public static void main(String[] args) {
> 		double d=3.14;
> 		float f=6.28F;
> 		System.out.println(f);
> 		/*科学计数法：e表示10的多少次方，e-2表示10的-2次方，e2表示10的2次方*/
> 		double g=314e-2;
> 		System.out.println(g);
>
> 	}
>
> }
>
> ```
>
> ```java
> public class TestCharType {
> 	public static void main(String[] args) {
> 		char c1='a';
> 		char c2='上';
> 		char c3='\'';
> 		char c4='a';
> 		System.out.println(c1);
> 		System.out.println(c2);
> 		System.out.println(c3);
> 		int i=c4+2;
> 		System.out.println(i);
> 		/*强制转型*/
> 		char c5=(char)i;
> 		System.out.println(c5);
> 	}
>
> }
> ```
>
>

------



#### 数据类型转换

>自动类型转换（隐式类型转换）
>
>容量小的数据类型可以自动转换为容量大的数据类型
>
>```java
>int x=3;
>byte b=5;
>x=x+b;
>```
>
>强制类型转换（显示类型转换）
>
>当将一种类型强制转换成另一种类型，而又超出了目标类型的表示范围，就会被截断成为一个完全不同的值
>
>```java
>int i=100;
>char c=(char)i;
>
>int a=3;
>long b=4;
>int c=(int)(a+b);
>
>int money=10000000000;
>int years=20;
>long total=(long)money*year;
>
>/*一个人70年的心跳*/
>long times=70L*60*24*365*70
>```
>
>

#### 运算符

> ##### 算数运算符
>
> +、-、*、/、%、++、--
>
> ##### 赋值运算符
>
> =、+=、-=、*=、/=
>
> ##### 关系运算符
>
> <、>、>=、<=、==、！=、instanceof
>
> ##### 位运算符
>
> &（按位与）、
>
> |（按位或）、
>
> ^（按位异或）相同为0，不同为1、
>
> ~（取反）、>>（右移运算符）右移一位相当于除2取商、<<（左移运算符）左移一位相当于乘2、>>>、
>
> ##### 逻辑运算符
>
> $$（逻辑与）、||（逻辑或）、!（逻辑与）
>
> ##### 条件运算符
>
> ？ ：
>
> > 三元表达式中
> >
> > a?b:c;
> >
> > 第一个数中得数字（a）大于0是true，小于等于0是false
>
>
>
>

## Java控制语句

> 顺序结构、选择结构、循环结构
>

### 选择结构

> 选择结构
>
> if单选择结构
>
> if语句对条件表达式进行一次测试，若测试为真，则执行下面的语句，否则跳过该语句
>
> ```java
> public class TestIf {
> 	public static void main(String[] args) {
> 		double b= Math.random();
> 		int e=1+(int)(b*6);
> 		System.out.println(e);
> 		if (e>3) {
> 			System.out.println("大数："+e);
> 			
> 		}
> 	}
>
> }
> ```
>
> ------
>
> if-else双选择结构
>
> 当条件表达式为真时，执行语句块1，否则，执行语句块2，也就是else部分。
>
> ```java
> public class TestIf {
> 	public static void main(String[] args) {
> 		double b= Math.random();
> 		int e=1+(int)(b*6);
> 		if (e>3) {
> 			System.out.println("大数："+e);
> 			
> 		}else {
> 			System.out.println("小数："+e);
> 		}
> 	}
>
> }
> ```
>
> ------
>
> if-else多选择结构
>
> ```java
> public class TestIf {
> 	public static void main(String[] args) {
> 		double b= Math.random();
> 		int e=1+(int)(b*6);
> 		if (e<=2) {
> 			System.out.println("小数："+e);
> 			
> 		}else if (e>2&&e<=4) {
> 			System.out.println("中数："+e);
> 		}else {
> 			System.out.println("大数："+e);
> 		}
> 	}
>
> }
> ```
>
> ------
>
> switch多值选择结构
>
> switch语句会根据表达式的值从相匹配的执行，一直执行到break标签处结束，如果没有就执行default里面的值
>
> ```java
> public class TestIf {
> 	public static void main(String[] args) {
> 		double b= Math.random();
> 		int e=1+(int)(b*6);
> 		switch (e) {
> 		case 1:
> 			System.out.println("小数："+e);
> 			break;
> 		case 2:
> 			System.out.println("小数："+e);
> 			break;
> 		case 3:
> 			System.out.println("中数："+e);
> 			break;
> 		case 4:
> 			System.out.println("中数："+e);
> 			break;
> 		default:
> 			System.out.println("大数："+e);
> 		}
> 	}
>
> }
> ```
>
> ------
>
> JDK7.0新特性：switch增强
>
> JDK7之前：表达式结果只能是int（可以自动转换为int的byte、short、char），枚举类型
>
> JDK7可以是字符串
>
> ```java
> /*测试JDK7的switch新特性*/
> public class TestSwitch{
>     public static void main(String[] args){
>         String a="hudeqiang";
>         switch(a){
>             case "hu":
>             	System.out.printIn("这是hu");
>             	break;
>              case "de":
>             	System.out.printIn("这是de");
>             	break;
>               case "qiang":
>             	System.out.printIn("这是qiang");
>             	break;
>               case "hudeqiang":
>             	System.out.printIn("这是hudeqiang");
>             	break;
>         }
>     }
> }
> ```
>
>

### 循环结构

> while循环
>
> 先判断，后执行
>
> - 在循环刚开始时，会计算一次“布尔表达式”的值，若条件为真，执行循环体，而对于后来每一次额外的循环，都会在开始前重新计算一次。
> - 语句中应有使循环趋向于结束的语句，否则会出现无限循环——“死循环”
>
> ```java
> /**
>  * 测试while循环
>  * @author 19254
>  *
>  */
> public class TestWhile {
>
> 	public static void main(String[] args) {
> 		int a=1;
> 		while(a<=100) {
> 			System.out.println(a);
> 			a++;
> 		}
> 		System.out.println("循环结束！");
> 		/*计算1+2+3+..+100*/
> 		int b=1;
> 		int sum=0;
> 		while(b<=100) {
> 			sum+=b;
> 			b++;
> 		}
> 		System.out.println("和为："+sum);
>
> 	}
>
> }
> ```
>
> ------
>
> do...while循环
>
> 先执行，后判断
>
> ```javascript
> /**
>  * 测试while循环
>  * @author 19254
>  *
>  */
> public class TestWhile {
>
> 	public static void main(String[] args) {
> 		/*计算1+2+3+..+100*/
> 		int b=100;
> 		int sum=0;
> 		do {
> 			sum+=b;
> 			
> 			b--;
> 		}while(b>=0);
> 		System.out.println("和为："+sum);
>
> 	}
>
> }
> ```
>
> ------
>
> for循环
>
> ```java
> /**
>  * 测试for循环
>  * @author 19254
>  *
>  */
> public class TestWhile {
>
> 	public static void main(String[] args) {
> 		for (int i = 0; i <= 100; i++) {
> 			System.out.println(i);
> 		}
> 	}
>
> }
> ```
>
> 使用for循环计算100以内奇数和偶数的和
>
> ```java
> public class TestWhile {
>
> 	public static void main(String[] args) {
> 		//用来保存奇数的和
> 		int oddSum=0;
> 		//y用来保存偶数的和
> 		int evenSum=0;
> 		for(int i=0;i<=100;i++) {
> 			if (i%2!=0) {
> 				oddSum+=i;
> 			}else {
> 				evenSum+=i;
> 			}
> 			
> 		}
> 		System.out.println(oddSum);
> 		System.out.println(evenSum);
> 	}
>
> }
> ```
>
> 用for循环输出1-1000之间能被5整除的数，且每行输出3个
>
> ```java
> public class TestWhile {
>
> 	public static void main(String[] args) {
> 		for(int i=0;i<=1000;i++) {
> 			if (i%5==0) {
> 				System.out.print(i+"\t");
> 			}
> 			if (i%15==0) {
> 				System.out.println();
> 			}
> 		}
> 	}
>
> }
> ```
>
> 九九乘法表
>
> ```java
> public class TestWhile {
>
> 	public static void main(String[] args) {
> 		for(int j=1;j<=9;j++) {
> 			for(int i=1;i<=j;i++) {
> 				System.out.print(i+"*"+j+"="+i*j+"\t");
> 			}
> 			System.out.println();
> 		}
> 		
> 	}
>
> }
> ```
>
>



### break和continue

> 在任何循环语句的主体部分，均可使用break控制循环的流程，break用于强行退出循环，不执行循环中剩余的语句。（break语句还可用于多分枝语句switch中）
>
> continue语句用在循环语句中，用于终止某次循环过程，即跳过循环体中尚未执行的语句，接着进行下一个是否执行循环的过程。
>
> ```java
> /*
> *（1）生成0-100的随机数，直到生成88为止，停止循环！
> *（2）把100-150之间不能被3整除的数输出
> */
> public class TestBreakContinue {
> 	public static void main(String[] args) {
> 		int total=0;
> 		System.out.println("Begin:");
> 		while(true) {
> 			total++;
> 			int i=(int)Math.round(100*Math.random());
> 			if(i==88) {
> 				break;
> 			}
> 		}
> 		System.out.println("Game over, used "+ total+"times.");
> 		System.out.println("-----------------------------------------");
> 		for(int i=100;i<150;i++) {
> 			if(i%3==0) {
> 				continue;
> 			}
> 			System.out.println(i);
> 		}
>
> 	}
>
> }
> ```
>
>



## 方法

> 什么是函数？
>
> > 函数就是定义在类种的具有特定功能的一段独立小程序。
> >
> > 函数也称为方法
>
>
>
> **设计方法的原则：方法的本意是功能模块，就是实现某个功能的语句块的集合。我们设计方法的时候，最好保持方法的原子性，就是一个方法只完成一个功能，这样有利于后期的扩展。**
>
> 函数的格式：
>
> ```
> 修饰符 返回值类型 函数名(参数类型 形式参数1,参数类型 形式参数2...){
>  执行语句
>  return 返回值;
> }
> ```
>
> 返回值类型：函数运行后的结果的数据类型
>
> 参数类型：是形式参数的数据类型
>
> 形式参数：是一个变量，用于存储调用函数时传递给函数的实际参数
>
> 实际参数：传递给形式参数的具体数值
>
> return：用于结束函数
>
> 返回值：该函数运算后的结果，该结果会返回给调用者
>
> ```java
> public class TestMethod {
>
>     private static int add(int a,int b){
>         int sum=a+b;
>         return  sum;
>     }
>
>     private static void test01(){
>         int oddSum=0;//用来保存奇数的和
>         int evenSum=0;//用来存放偶数的和
>         for (int i=0;i<=100;i++){
>             if (i % 2 != 0){
>                 oddSum += i;
>             }else {
>                 evenSum += i;
>             }
>         }
>         System.out.println("奇数和为："+oddSum);
>         System.out.println("偶数和为："+oddSum);
>     }
>     public static void main(String[] args){
>         test01();
>         int s= add(2,3);
>         System.out.println(s);
>     }
> }
>
> ```
>
>
>
> ------
>
>
>
>



## 递归

递归是一种常见的解决问题的方法，即把问题逐渐简单化。递归的基本思想就是“自己调用自己”，一个使用递归技术的方法将会直接或者间接的调用自己。

递归的结构包括两个部分：

- 定义递归头。解答：什么时候不调用自身方法，如果没有头，将陷入死循环。
- 递归体：解答：什么时候需要调用自身方法。

```java
public class TestRecursion {
    /*测试递归 计算:=====5*4*3*2*1*/
    static int a=0;

    public static void test01(){
        a++;
        System.out.println("此时a的值为："+a);
        if (a < 10){
            test01();
        }else {
            System.out.println("over");
        }
    };
    public static long factorial(int n){
        if (n == 1){
            return n;
        } else {
            return n*factorial(n-1);
        }
    }

    public static void main(String[] args) {
        test01();
        System.out.println(factorial(5));
    }
}

```



## 面向对象

> ##### 面向对象（类和对象）概述
>
> - 类：是一组相关属性和行为的集合
> - 对象：是该类的具体体现
> - 成员变量：事物的属性
> - 成员方法：事物的行为
>
> ------
>
> 案例：学生类的定义
>
> ```java
> public class Student {
> 	//姓名
> 	String name="胡德强";
> 	//年龄
> 	int age=20;
> 	//性别
> 	String gender;
> 	//定义学习的方法
> 	public void study() {
> 		System.out.println("学生学习！！");
> 	}
> 	//定义睡觉的方法
> 	public void sleep() {
> 		System.out.println("上课睡觉！！");
> 	}
>
> 	public static void main(String[] args) {
> 		// TODO Auto-generated method stub
> 		//创建对象
> 		Student stu=new Student();
> 		//对象调用属性
> 		System.out.println(stu.name);
> 		System.out.println(stu.age);
> 		//对象调用方法
> 		stu.study();
> 		stu.sleep();
>
> 	}
> 	
> }
> ```
>
> ------
>
> 案例：定义一个手机类
>
> ```java
> public class Phone {
> 	//品牌
> 	String brand;
> 	//价格
> 	int price;
> 	//打电话的方法
> 	public void call() {
> 		System.out.println("打电话！！");
> 	}
> 	public void sendMessage() {
> 		System.out.println("发短信！！");
> 	}
> 	
> 	public static void main(String[] args) {
> 		//创建对象
> 		Phone iPhone=new Phone();
> 		System.out.println(iPhone.brand="苹果");
> 		System.out.println(iPhone.price=1000);
> 		//调用方法
> 		iPhone.call();
> 		iPhone.sendMessage();
> 	}
>
> }
>
> ```
>
> ------
>
> 创建对象
>
> ```java
> 类名 对象名=new 类名();
> ```
>



# intellij idea

> 官网：http://www.eclipse.org/downloads
>
> 常用快捷键：
>
> System.out.print()：sout+tab
>
> public static void main(String[] args){}：psvm+tab
