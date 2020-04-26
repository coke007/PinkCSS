#   **css学习笔记**

# **css的样式规则**

![QQ图片20191007140854](D:\typora\typora_images\QQ图片20191007140854.png)

# **字体样式和字号**

## font-size:字号大小

## font-style：字体风格

   normal:正常字体

​	italic:指定文本字体为倾斜字体



## font-weight:字体粗细

​    其属性值：normal、bold、bolder、lighter、100~900（100的整数倍）

​    其中400等价于normal 、700等价于bold



## font-family:字体

![QQ图片20191007140903](D:\typora\typora_images\QQ图片20191007140903.png)

## font综合设置字体样式

![QQ图片20191007140911](D:\typora\typora_images\QQ图片20191007140911.png)

## google图标案例

![ggoogle](D:\typora\typora_images\ggoogle.png)

```css
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title></title>
	<style type="text/css">
		span{
			font-size: 100px
		}

		.blue{
			color: blue
		}
		.red{
			color: red
		}
		.orange{
			color: orange
		}
		.green{
			color: green
		}
	</style>
</head>
<body>
	<span class="blue">G</span>
	<span class="red">o</span>
	<span class="orange">o</span>
	<span class="blue">g</span>
	<span class="green">l</span>
	<span class="red">e</span>

</body>
</html>
```

## 无序表格去除小点

```css
ul {
	list-style:none;
}
```



# 类选择器（重点）

## id选择器和类选择器的区别

1.  id像身份证一样，只能唯一；

    设置style时，用.+class名

2. class可以定义多个，多个标签可以使用相同的class名称

   设置style时，用#+id名

## 通配符选择器

基本语法：

```css
*{
    /*属性：属性值*/
     /*这里对所有标签进行设置*/
}
```

## 伪类选择器

![伪类](D:\typora\typora_images\伪类.jpg)

​	目标伪类选择器

```css
：target{
/*目标伪例选择器，可用于选择当前活动的目标元素*/
}
```



注意属性：属性名；（这里的；不能省略）

```css
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title></title>
	<style type="text/css">
		a:link{  /*未访问的链接*/
			font-size: 20px;
			color:orange;
			font-weight: 700;
		}
		a:visited{/*已访问的链接*/
			font-size: 20px;
			color:green;
			font-weight: 700;
		}
		a:hover{/*鼠标经过时*/
			font-size: 20px;
			color: red;
			font-weight: 700;
		}
		a:active{/**/
			font-size: 16px
			color:orange;
			font-weight: 700
		}
	</style>
</head>
<body>	
	<div><a href="#">秒杀</a></div>
</body>
</html>
```

# CSS外观属性

![QQ图片20191007151303](D:\typora\typora_images\QQ图片20191007151303.jpg)

## color：文本颜色

## line-height:行间距

## text-align:水平对齐方式

 

```css
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title></title>
	<style type="text/css">
		div{
			letter-spacing: 10px;  /*字间距*/
		}
		p{
			word-spacing: 1px;   /*单词间距 针对英文不针对中文*/
		}
	</style>
</head>
<body>

<div>我现在的心情可美丽的呢</div>
<p>my name is andy </p>
</body>
</html>
```



## 颜色半透明（CSS3）

![QQ图片20191007202554](D:\typora\typora_images\QQ图片20191007202554.jpg)

# sublime快捷键

1. 生成标签：直接输入标签名+tab键
2. 如果想要生成多个相同标签+ *就可以了            
3. 如果有兄弟关系的标签，用+就可以了    比如 div+p
4. 如果有父子级关系的标签，比如ul>li就可以了
5. 如果生成带有类名或者id名字的，直接用.class名或者# id名 tab键就可以了

# CSS样式表

## 内部样式表

## 行内样式表

## 外部样式表

通常在<head></head>标签中添加<link /> ，使它关联style.css文件

```css
<link rel="stylesheet" type="text/css" href="style.css" />
```

```
href:链接外部样式表的url
type:定义所链接文档的类型
rel:定义当前文档与被链接文档之间的关系
```



## 三种样式表总结

| 样式表     | 优点                     | 缺点                   | 使用情况 | 控制范围     |
| ---------- | ------------------------ | ---------------------- | -------- | ------------ |
| 行内样式表 | 书写方便，权重高         | 没有实现样式和结构分离 | 少       | 控制一个标签 |
| 内部样式表 | 部分结构和样式相分离     | 没有彻底分离           | 较多     | 控制一个页面 |
| 外部样式表 | 完全实现结构和样式相分离 | 需要引入               | 最多     | 控制整个站点 |

# 标签显示模式

## 块级元素（block-level）

:每个元素通常都会独自占据一整行或者多整行，可以对其设置宽度、高度、对齐等属性，常用于网页布局和网页结构

```
常见的块元素：<h1>~<h6>、<p>、<div>、<ul>、<ol>、<li>等
```

特点：

1. 它们都是从新行开始
2. 高度、行高、外边距以及内边距都可以控制
3. 宽度默认使容器的100%
4. 可以容纳内联元素和其他块元素



## 行内元素（inline-level)

:不占有独立的区域，仅仅靠自身的字体大小和图像尺寸来支撑结构，一般不可义设置宽度、高度、对齐等属性

```
常见的行内元素：<a>、<strong>、<b>、<em>、<i>、<del>、<s>、<ins>、<u>、<span>等
```

特点：

1. 和相邻行内元素在一行上

2. 高宽无效，水平方向的padding和margin可以设置

3. 默认宽度是它本身内容的宽度

4. 行内元素只能容纳文本或其他行内元素（a特殊）

   

## 行内块元素（inline-block)

:具有行内元素的性质，具有块内元素的性质

```
<img>、<tab>...
```

## 显示模式转换

块转行内：display:inline;

行内转块：display:block;

块、行内元素转化伪行内快：display:inline-block

# CSS选择器

## 交集选择器

：标签和class名之间没有空格

![交集选择器](D:\typora\typora_images\交集选择器.jpg)



## 并集选择器

:标签集体声明

```css
<style type="text/css">
		div,
		p,
		span{
			color: blue;
			font-size:15px;
		}
	</style>
```

```
比如 .one,p,#test { 属性：属性值;}      表示.one和p和#test者三个选择器都会执行该属性
```

## 后代选择器

：父标签和子标签之间有空格

![后代选择器](D:\typora\typora_images\后代选择器.jpg)

## 子元素选择器

```html
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title></title>
	<style type="text/css">
		.nav li{   /* 空格 后代选择器 可以选择儿子 孙子 重孙子*/
			color: pink
		}
		.nav > li{  /*大于号 子元素选择器 只选择亲儿子*/
			color: blue
		}
	</style>
</head>
<body>
	<ul class="nav">
		<li>今天也要加油哦
			<ul>
				<li>二级菜单</li>
				<li>三级菜单</li>
				<li>四级标题</li>
			</ul>
		</li>
	</ul>
</body>
</html>
```

## 综合案例

<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title></title>
	<style type="text/css">
		.site-r a{
			color: red; /* 1，导航栏中链接文字改为红色*/
		}
		.nav ul li a{    /*1，将主导航栏的链接字体改为天蓝色*/
			color: skyblue;
		}
		.nav,.sitenav{		/*2，将所有链接的字体设置字体大小和字型*/
			font-size: 14px;
			font-family: "微软雅黑";
		}
		.nav >ul>li>a{   /*3,主导航栏里面的一级菜单链接文字颜色为绿色*/
			color:green;
		}
	</style>
</head>
<body>
	<!-- 主导航栏 -->
	<div class="nav">
		<ul>
			<li><a href="#">公司首页</a></li>
			<li><a href="#">公司简介</a></li>
			<li><a href="#">公司产品</a></li>
			<li>
				<a href="#">联系我们</a>
				<ul>
					<li><a href="#">公司邮箱</a></li>
					<li><a href="#">公司电话</a></li>
				</ul>
			</li>
		</ul>
	</div>
	<!-- 侧导航栏 -->
		<div class="sitenav">
			<div class="site-1">左侧导航栏</div>
			<div class="site-r"><a href="#">登录</a></div>
		</div>
</body>
</html>

## 属性选择器

```css
<style type="text/css">
		/*div标签中class属性前面为font的*/
		div[class^=font]{   
			color: pink;
		}
		/*div标签中class属性以footer结尾的*/
		div[class$=footer]{
			color:green;
		}
		/*div标签中class属性中包含有tao*/
		div[class*=tao]{
			color: blue;
		}
	</style>
```

## 伪元素选择器

![伪元素选择器](D:\typora\typora_images\伪元素选择器.jpg)

：**before和after在盒子div内部前面插入或者是内部后面插入**

```css
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title></title>
	<style type="text/css">
		div::before{
			content: "啊啊啊啊啊";
		}
		div::after{
			content: "一定要加油哦"
		}
	</style>
</head>
<body>
	<div>今年</div>
</body>
</html>
```

# CSS背景

## 背景图片

```css
background-image: url(images/ms.jpg)
```



## 背景平铺

```css
background-repeat：no-repeat  /*不平铺   默认平铺*/
```



## 背景位置

![背景位置](D:\typora\typora_images\背景位置.jpg)

## 背景附着

```css
background-attachment:scroll|fixed
```

参数：

scroll:默认，滚动

fixed:背景图片固定

## 背景大小

```css
background-size:200px 300px;/*只能通过这个来改变背景图片大小*/
```

## 背景简写

```
background:背景颜色 背景图片地址  背景平铺 背景滚动 背景位置
```

## 背景半透明

```css
background：rgba(0,0,0,0.5)
```

## 多背景

![多背景](D:\typora\typora_images\多背景.jpg)

**注意：**

​	**背景颜色一定写在最后一组 背景图片上面**

## 背景综合设置格式

```css
background:背景颜色 背景图片地址  背景平铺 背景滚动 背景位置
```

1. background: #ff0000 url(你图片的地址) no-repeat fixed 0 0;
   #ff0000 表示背景图片由于某种原因无法显示所显示的颜色
   url()  在括号中输入你想要作为[背景](http://www.so.com/s?q=背景&ie=utf-8&src=internal_wenda_recommend_textn)的图片
   no-repeat 表示该背景图片是否重复显示(repeat-x  repeat-y repeat 等)
   fixed 0 0; 背景图片想要显示[区域](http://www.so.com/s?q=区域&ie=utf-8&src=internal_wenda_recommend_textn)的定位

## 案例（凹凸文字）

```css
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title></title>
	<style type="text/css">
		body {
			background: #ccc;
		}
		div {
			color: #ccc;
			font: 700 80px "微软雅黑" ;
		}
		div:first-child {
			/*text-shadow: 水平距离 垂直距离 模糊距离 */
			text-shadow: 1px 1px 1px #000,
			-1px -1px 1px #fff;
		}
		div:last-child {
			text-shadow: -1px -1px 1px #000,
			1px 1px 1px #fff;
		}
	</style>
</head>
<body>
	<div>我是凸起的文字</div>
	<div>我是凹下的文字</div>

</body>
</html>
```

## 文本装饰

```css
text-decoration: none;
```

![文本装饰](D:\typora\typora_images\文本装饰.jpg)



# CSS三大特性

## CSS重叠性

## CSS继承性

## CSS优先性

:id > 类=伪类 > 标签 

# 盒子模型（CSS重点）

## 盒子边框

```css
border ：border-width||border-style||border-color
```

边框样式用于定义页面中边框的风格，常用属性如下：

1. none :没有边框
2. solid: 边框为单实线
3. dotted:边框为电线
4. double:边框为双实线

```css
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title></title>
	<style type="text/css">
		div {
			width:200px;
			height:200px;
			border-width:1px;
			border-color: pink;
			border-style: double;
		}
	</style>
</head>
<body>
	<div>盒子</div>
</body>
</html>
```

## 盒子边框写法总结表

**border：四边宽度  四边样式  四边颜色** 

![盒子边框](D:\typora\typora_images\盒子边框.jpg)

![盒子边框2](D:\typora\typora_images\盒子边框2.jpg)

## 圆角边框

```css
border-radius: 左上角和右下角  右上角和左下角(只有两个参数时)
border-radius:四个方位(以左上角为起点，顺时针旋转方向)
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		div {
			width: 200px;
			height: 200px;
			border:1px solid red;
		}
		div:first-child {  /*结构伪类选择器*/
			border-radius: 10px;
		}
		div:nth-child(2) {
            border-radius:50%;  /*50%则会变成一个圆形*/
		}
		div:nth-child(3) {
			border-radius: 10px 20px;  /* 左下角、右下角是10px,右上角、左下角是20px;*/
		}
		div:nth-child(4) {
			border-radius:10px 40px 80px 100px;
		}

	</style>
</head>
<body>
	<div></div>
	<div></div>
	<div></div>
	<div></div>
	<div></div>
</body>
</html>
```

## 盒子模型内边距

```css
padding:10px 40px;   /*表示上下10px 左右40px;*/
```

![盒子内边距](D:\typora\typora_images\盒子内边距.jpg)

## 课堂案例：新浪导航

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		.nav {
			/*width: 800px;*/
			height: 80px;
			background-color: #FCFCFC;
			border-top:3px solid orange;
			border-bottom:1px solid orange;
		}
		a {
			/*width: 200px;
			height: 50px;*/
			display: inline-block;
			text-decoration: none;
			/*text-align: center; 表示水平居中*/
			padding: 0px 15px;
			font-size: 16px;
			color: #4c4c4c;
			line-height: 80px;  /*行高等于高度则垂直居中*/
		}
		a:hover {
			background-color: #ccc;
		}
		
	</style>
</head>
<body>
	<div class="nav">
    <a href="#" calss="a1" >设为首页</a>
    <a href="#">手机新浪网</a>
    <a href="#">移动客户端</a>
		
	</div>
</body>
</html>
```

## 外边距（margin）

```css
margin：0px auto     /*实现盒子左右方向居中*/
```

![外边距](D:\typora\typora_images\外边距.jpg)

## 外边距合并问题

：外边距合并，以最大的外边距为准

![外边距合并](D:\typora\typora_images\外边距合并.jpg)解决方法：

1. 为父类元素添加overflow:hidden
2. 可以为父类元素定义1像素的上边框或者上内边框

## 嵌套块元素垂直外边距的合并

![嵌套块外边距合并](D:\typora\typora_images\嵌套块外边距合并.jpg)

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		div {
			width: 400px;
			height: 400px;
			background-color: pink;
			/*border:1px solid black;   给父标签添加边框,则父边框和子边框不会同时移动*/
			/*padding:50px;*/
			overflow: hidden;

		}
		div div {
			width: 200px;
			height: 200px;
			background-color: purple; 
            margin-top: 40px;
		}
	</style>
</head>
<body>
	<div class="father">
		<div class="son"></div>
	</div>  

</body>
</html>
```

## 综合案例：趣味搜索

```css
ul {
	  list-style: none;  /*取消列表自带的小点*/
	}
```



```css
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		ul {
			list-style: none;  /*取消列表自带的小点*/
		}
		* {
		margin:0px;
		padding:0px;
	}
    .search_picture {
    	width: 238px;
    	height: 294px;
    	border:1px solid #D9E0EE;
    	border-top:3px solid #FF8400;
    	margin: 100px;
    }
    .search_picture h3 {
    	height: 35px;
    	border-bottom: 1px solid #D9E0EE;
    	font-size: 16px;
    	font-weight: normal;
    	line-height: 35px;
        /*这个h3没有给定宽度，所以自动继承父标签的宽度*/
        padding-left: 12px;
    }
    img {
    	margin:7px 0 0 8px;
    }
    .search_picture ul li a {
    	font-size: 12px;
    	color: #666;
    	text-decoration: none;
    }
    .search_picture ul {
    	margin-left: 8px;
    }
    .search_picture ul li {
    	padding-left: 10px;
    	height: 26px;
    	line-height: 26px;
    	background:url(image02.jpg) no-repeat left center; 
    }
    .search_picture ul li a:hover {
    	text-decoration: underline; /*添加下划线*/
    	color: #ff8400;
    }
 
	</style>
</head>
<body>
	<div class="search_picture">
		<h3>搜索趣图</h3>
		<img src="image01.jpg"  width="218" height="160" alt="">
		<ul>
			<li><a href="#">C罗闭着眼都能让球队赢球 曼联5900万</a></li>
			<li><a href="#">C罗闭着眼都能让球队赢球 曼联5900万</a></li>
			<li><a href="#">C罗闭着眼都能让球队赢球 曼联5900万</a></li>
		</ul>
	 </div>

	
</body>
</html>
```



# CSS盒模型

```css
border-sizing:content-box;    /*以前的盒模型，盒子大小为width+padding+border*/
```

```css
border-sizing:border-box;  /*padding和border不撑开盒子  padding和border是包含在width里面的*/
```

## 盒子阴影

![+](D:\typora\typora_images\盒子阴影.jpg)



# 浮动（float）

1. 块级元素添加浮动之后，具有行内块的特性
2. 行内元素添加浮动，具有行内块的特性,元素的大熊啊完全取决于定义的大小或者默认的内容多少



## 普通流（normal flow）

![浮动](D:\typora\typora_images\浮动.jpg)



## 浮动的作用

浮动的目的：让多个块级元素在同一行上显示

# 版心和布局流程                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              

## 布局流程

提高网页制作效率，布局时通常需要遵守一定的布局流程，具体如下：

1.确定页面版心（可视区）

2.分析页面中的行模块，以及每个行模块中的列模块

3.制作HTML结构

4.CSS初始化，然后开始运用盒子模型的原理，通过DIV+CSS布局来控制网页的各个模块

### 网页整体布局案例

**margin:0px auto;          /*盒子居中,上下为0px,左右居中auto*/**

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		* {
			margin: 0;
			padding:0;
		}
		.top,
		.banner,
		.main,
		.footer{
			width: 800px;
			border:1px dotted red;
			text-align: center;
			margin:0px auto;/*盒子居中,上下为0px,左右居中auto*/
			margin-bottom: 20px;
 
		}
		.top {
			height: 100px;
			background-color: pink;
		}
		.banner {
			height: 340px;
			background-color: deeppink;
		}
		.main {
			height: 200px;
			background-color: purple;
		}
		.footer {
			height: 120px;
			background-color: skyblue;
		}
	</style>

</head>
<body>
	<div class="top">top</div>
	<div class="banner">banner</div>
	<div class="main">main</div>
	<div class="footer">footer</div>
</body>
</html>
```

## 两列左窄右宽型

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		* {
			margin: 0;
			padding: 0;
		}
		.top,
		.banner,
		.main,
		.footer {
			width: 960px;
			border:1px dotted red;
			background-color: pink;
			margin:0 auto;
			text-align: center;
		}
		.top {
			height: 100px;
		}
		.banner {
			height: 100px;
		}
		.main {
			height: 200px;
		}
		.left {
			width:360px;
			height: 200px;
			background-color: skyblue;
			float: left;
			
			/*margin-right: 8px;*/

		}
		.right {
			width:592px;
			height: 200px;
			background-color: purple;
			float:right;
		}
		.footer {
			height: 120px;
		}
	</style>
</head>
<body>
	<div class="top">top</div>
	<div class="banner">banner</div>
	<div class="main">
		<div class="left">left</div>
		<div class="right">right</div>
	</div>
	<div class="footer">footer</div>
</body>
</html>
```

## 通栏平均分布型

```css
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		* {
			margin: 0;
			padding-left: 0;
		}
		.top,
		.banner,
		.footer {
			width: 960px;
			border:1px dashed black;
			text-align: center;
			margin: 12px auto;
		}
		.top {
			height:30px;
			background-color: #3c3c3c;
			text-align: center;
		}
		.banner {
			height: 120px;
			background-color: pink;
		}
		.banner ul li {
			width:100px;
			height: 120px;
			float:left;
			list-style: none;
		}
	    li:nth-child(even) {
			background-color: purple;
		}
		.footer {
			background-color: #ccc;
			height: 80px;
		}
	</style>
</head>
<body>
	<div class="top">top</div>
	<div class="banner">
		<ul>
			<li>1</li>
			<li>2</li>
			<li>3</li>
			<li>4</li>
		</ul>
	</div>
	<div class="footer">footer</div>
</body>
</html>
```



# 清楚浮动的方法

：又名闭合浮动，清楚浮动就是把浮动的盒子圈到里面，让父盒子闭合出口和入口不让他们出来影响其他元素。

在CSS中，clear清楚浮动，其基本语法格式如下：

| 属性值 | 描述                       |
| ------ | -------------------------- |
| left   | 不允许左侧有浮动           |
| right  | 不允许右侧有浮动           |
| both   | 同时清楚左右两侧浮动的影响 |

## 额外标签法

在浮动元素末尾添加：

```css
clear:both;
```

## 父级添加overflow属性方法

通过触发BFC的方式，可以实现清除浮动的效果

可以给父级添加：

```css
overflow:hidden |auto |scroll;
```

## 使用after伪类清楚浮动

```css
.clearfix:after {
    content:".";
    display:block;
    height:0;
    clear:both;
    visibility:hidden;
}

.clearfix {*zoom:1; } /*IE6、7专有*/
```

## 使用before和after双尾元素清除浮动

```css
.clearfix:before,.clearfix:after {
    content:"";
    display:table;  /*这句话可以触发BFC,BFC可以清楚浮动*/
}
.clearfix:after{
    clear:both;
}
.clearfix {
    *zoom:1;
}
```

## 综合举例

```css
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		* {
			margin:0;
			padding:0;
		}
		.box1 {
			/*如果box1没有指定高度的话，并且子类孩子都是浮动，则下面的box2会自适应跑到上面来*/
			width: 200px;
			background-color: pink;
			/*第二种方法:直接给父盒子添加overflow;
			overflow: hidden;*/

		}
		.son1 {
			height: 60px;
			width: 40px;
			background-color: skyblue;
			float: left;
		}
		.son2 {
			height: 60px;
			width: 40px;
			background-color: purple;
			float: left;

		}
		.box2 {
			height: 100px;
			width: 200px;
			background-color: #ccc;
		}
		/*第一种方法*/
		/*.clear {
			clear: both;
		}*/

		/*第三种方法*/
		.clearfix:before,.clearfix:after {
			display: table;
			content: "";
		}
		.clearfix:after {
			clear:both;
		}
		.clearfix {
			*zoom:1;
		}

	</style>
</head>
<body>
	<div class="box1 clearfix">
		<div class="son1"></div>
		<div class="son2"></div>
		<!-- 第一种方法：添加空盒子清除浮动 -->
		<!-- <div class="clear"></div> -->

	</div>
	<div class="box2"></div>
</body>
</html>
```

# 定位

position属性用于定义元素的定位模式，其基本语法格式如下：

```
选择器{ 
position:属性值;
}
```

| 值       | 描述                   |
| -------- | ---------------------- |
| static   | 自动定位     标准流    |
| relative | 相对定位               |
| absolute | 绝对定位    脱离标准流 |
| fixed    | 固定定位               |

## 定位属性

### 静态定位

1.静态定位--对于片偏移无效的。



### 相对定位

2.相对定位

  	通过片偏移移动位置，但是原来的所占位置，继续占有；

​      其次，每次移动的位置，都是以**自己原来位置左上角**为基点移动；



### 绝对定位

3.绝对定位

  	不占位置，脱离标准流

​	  完全脱标，不占位置，飘起来的

​	  父亲没有定位，那么孩子以浏览器为基准点对齐

**注意：通常子类用绝对定位，不占位置；父类用相对定位，占位置；（子绝父相）**



### 固定定位

4.固定定位

​      固定定位与父亲没有任何关系，**只认浏览器**，**脱标**

​      一直固定在窗口位置，不随滚动条的滚动而滚动

​      一定要指定宽高，它也不占位置



## “子绝父类”举例

```css
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		div {
			height: 350px;
		    width: 240px;
		    border:1px solid #ccc;
		    padding: 20px;   /*padding值会撑大盒子*/
		    margin: 0 auto;
		    position: relative;   /*父类设置为相对定位，子类才不会以浏览器的开始处为起点*/


		}
		.topIcon {
			position: absolute;
			left:0;
			top:0;
		}
		.bottomIcon {
			position: absolute;
			right: 0px;
			bottom: 0px;
		}

	</style>
</head>
<body>
	<div>
		<img src="image01.jpg" alt="" >
		<img src="image02.jpg" alt="" class="topIcon">
		<img src="image02.jpg" alt="" class="bottomIcon">
	</div>
	
</body>
</html>
```





## 浮动和定位的区别

浮动的主要目的：让块元素能够在同一行显示；

定位的主要价值：移动位置，让盒子到我们想要的位置上去；



## 绝对定位的水平/垂直居中

```css
margin：0 auto;   /*加了绝对定位（注意是绝对定位！）的盒子，margin左右auto就无效了*/
```

```
left:50%;         /*表示父盒子宽度的一半*/
margin-left:-50px;   /*向左移动自身宽度的一半*/
```



## 课堂练习：淘宝轮播图

```css
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>

	<style>
		ul {
			list-style: none;
		}
		div {
			height: 280px;
			width: 520px;
			margin: 0 auto;
			position: relative;

		}
		.arrow-l,
		.arrow-r {
			position: absolute;
			top: 50%;
			margin-top:-18px; 
		}
		.arrow-l {
			left:0px;       /* 绝对定位，使用margin：auto是不能实现居中的*/
			                /*移动自身24*36 高度的一半; 由于向上移动，所以为负值*/
		}
		.arrow-r {
			right: 0px;
		}

		.circle {
			height: 13px;
			width: 65px;
			background-color: rgba(0,0,0,0.2);
			position: absolute;
			bottom: 15px;
			left: 50%;
			margin-left: -10px;
			border-radius: 6px;
		}

		.circle li {
			float:left;
			width: 9px;
			height: 9px;
			background-color: #B7B7B7;
			margin:2px;
			border-radius: 50%;
		}
	</style>
</head>
<body>
	<div class="slider">
		<img src="images/taobao.jpg" alt="">
		<img src="images/left.png"  class="arrow-l" alt="">
		<img src="images/right.png" class="arrow-r" alt="">
		<ul class="circle">
			<li></li>
			<li></li>
			<li></li>
			<li></li>
			<li></li>
		</ul>
		
	</div>
</body>
</html>
```

## 叠放次序（z-index)

1.z-index:默认属性值是0，取值越大，定位元素在层叠元素中越居上

2.如果取值相同，则根据书写顺序，后来居上

3.后面的数字不能加单位

4.只有相对定位，绝对定位，固定定位有此属性，其余标准流，浮动，静态定位都无此属性，不可指定该属性

## 四种定位总结

## 定位模式转换

![](D:\typora\typora_images\四种定位总结.jpg)

**注意：添加浮动、绝对定位、固定定位 之后，则不需要再多此一举将行内元素转化为块内元素**



# 元素的显示与隐藏

**(1) display**

```css
display:none;             /*隐藏，不保留位置*/
```

```css
display:block;            /*除了转换为块级元素之外，同时还有显示元素的意思*/
```

   特点：隐藏之后，不占位置

**(2) visibility**

```css
visibility:hidden;      /*隐藏元素,为其他保留位置*/
visibility:visible;     /*显示*/
```



# overflow

```css
overflow:auto ;     /*文字内容超出了，才会显示滚动条*/
overflow:scroll;    /*无论文字是否超出，都显示滚动条*/
overflow:hidden;    /*溢出隐藏*/
```



## 案例-显示二维码

```css
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		div {
			height: 40px;
			width: 40px;
			background-color: pink;
			margin:0px auto;
			position: relative;
		}
		img {
			position: absolute;
			left:40px;
			top: 0px;
			display: none;
		}

		div:hover img {
			display: block;

		}
	</style>
</head>
<body>
	<div>
		<img src="web_photos/images/erweima.png" alt="">
		
	</div>
</body>
</html>
```

、

# CSS高级技巧

## css用户界面样式



### 鼠标样式cursor

```css
cursor:default 小白| pointer 小手| move 移动 |text 文本
```



### 轮廓 outline

```css
outline:0    /*一般是去除轮廓线*/
```



### resize:none   

```
resize:none       /*防止文本域拖拽*/
```



### vertical-align 垂直对齐

vertical-align不影响块级元素的内容， 他只针对针对**行内元素，通常用来控制图片/表单与文字的对齐**

图片的文字默认的是基线对齐

![vertical-align](D:\typora\typora_images\vertical-align.jpg)

### 图片和盒子底部空白缝隙

当图片和盒子大小一样时，由于图片默认和盒子基线对齐，所以在低版本浏览器中会显示底部缝隙

解决办法：

1，将图片转换为块级元素

```css
img { display：block; }
```

2，使用vertical-align不使他取默认值（默认值是基线对齐）

```css
vertical-align：middle;
```



## 溢出的文字隐藏

![](D:\typora\typora_images\文字溢出.jpg)

```css
white-space:no-wrap;    /*首先先添加这句话，强制一行*/
text-overflow:clip;     
overflow:hidden;       /*其次必须要有这句话*/
```

```css
white-space:no-wrap;    /*首先先添加这句话，强制一行*/
text-overflow:ellipsis;  /*溢出部分用省略号显示*/
```

# CSS精灵技术（sprite）

将一些小图标放在一张透明的背景图上面去，通过位置访问具体的图片，这样浏览器访问具体一张图片就不需要每次都从访问服务器端。



# 字体图标

## 字体图标使用流程

### 字体网站

1.icomoon字库**

IcoMoon成立于2011年，推出的第一个自定义图标字体生成器，它允许用户选择他们所需要的图标，使它们成一字型。 内容种类繁多，非常全面，唯一的遗憾是国外服务器，打开网速较慢。

  推荐网站： http://icomoon.io

**2.阿里icon font字库**

http://www.iconfont.cn/

这个是阿里妈妈M2UX的一个icon font字体图标字库，包含了淘宝图标库和阿里妈妈图标库。可以使用AI制作图标上传生成。 一个字，免费，免费！！

### 字体引入到HTML

得到压缩包之后，最后一步，是最重要的一步了， 就是字体文件已经有了，我们需要引入到我们页面中。

1.首先把 以下4个文件放入到 fonts文件夹里面。 通俗的做法：将font文件夹放置到当前所写的.html文件夹中

![fonts](D:\typora\typora_images\fonts.png)

**第一步：在样式里面声明字体： 告诉别人我们自己定义的字**体

```css
@font-face {
  font-family: 'icomoon';
  src:  url('fonts/icomoon.eot?7kkyc2');
  src:  url('fonts/icomoon.eot?7kkyc2#iefix') format('embedded-opentype'),
    url('fonts/icomoon.ttf?7kkyc2') format('truetype'),
    url('fonts/icomoon.woff?7kkyc2') format('woff'),
    url('fonts/icomoon.svg?7kkyc2#icomoon') format('svg');
  font-weight: normal;
  font-style: normal;
}
```

**第二步：给盒子使用字体**

```css
span {
		font-family: "icomoon";
	}
```

**第三步：盒子里面添加结构**

```css
span::before {
		 content: "\e900";    /*此处使用unicode编码方式*/
	}

或者 

<span></span>  /*此处的图标是从下载的文件中index.html复制粘贴过来的*/
```

# 滑动门原理

**核心技术**

核心技术就是利用CSS精灵（主要是背景位置）和盒子padding撑开宽度, 以便能适应不同字数的导航栏。

一般的经典布局都是这样的：

利用两个盒子：a标签和span标签分别控制左右两端

```html
<li>
  <a href="#">
    <span>导航栏内容</span>
  </a>
</li>
```

总结： 

1. a 设置 背景左侧，padding撑开合适宽度。    
2. span 设置背景右侧， padding撑开合适宽度 剩下由文字继续撑开宽度。
3. 之所以a包含span就是因为 整个导航都是可以点击的。



**举例**

```css
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		a {
			display: inline-block;
			height: 33px;
			background: url(web_photos/images/ao.png) no-repeat;
			padding-left: 15px;
		}
		span {
			display: inline-block;
			height: 15px;
			background:url(web_photos/images/ao.png) no-repeat right;
			padding-right: 20px;
		}
	</style>
</head>
<body>
	<a href="#">
		<span>人生也太难了吧</span>
	</a>
</body>
</html>
```

## 案例-微信导航栏

```css
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		* {
			margin: 0px;
			padding: 0px;
		}
		body {
		    background: url(web_photos/images/wx.jpg) repeat-x;

		}
		li {
			list-style: none;
		}
		a {
			text-decoration: none;
		}
		
		.nav {
			margin-top: 10px;
		}
	
		.nav li {
			float:left;
			margin-right: 15px;
		}


		.nav li a {
			display: inline-block;
			/*height: 33px;*/
			padding-left:15px;    /*没有指定宽度，则不会显示背景图片，所以利用padding值来撑开盒子，显示图片*/
			background: url(web_photos/images/to.png) no-repeat;
			line-height: 33px;   /*指定了行高后，就不需要指定高度*/
		}

		.nav li a span {
			display: inline-block;
			/*height: 33px;*/
			padding-right: 10px;
			background: url(web_photos/images/to.png) no-repeat right;
			color: #fff;
			line-height: 33px;
		}
		.nav li a:hover {             /*这里只能控制a标签下的图片，并不能控制span下的标签*/
			background-image: url(web_photos/images/ao.png);
		}

		.nav li a:hover span {         /*a:hover下的span标签*/
			background-image: url(web_photos/images/ao.png);
		}

		
	</style>
</head>
<body>
	<div class="nav">
		<ul>
			<li>
				<a href="#"><span>首页</span></a>
			</li>
			<li>
				<a href="#"><span>帮助与反馈</span></a>
			</li>
			<li>
				<a href="#"><span>公众平台</span></a>
			</li>
			<li>
				<a href="#"><span>帮助与反馈</span></a>
			</li>
			<li>
				<a href="#"><span>帮助与反馈</span></a>
			</li>
			<li>
				<a href="#"><span>帮助与反馈</span></a>
			</li>
			<li>
				<a href="#"><span>帮助与反馈</span></a>
			</li>
			<li>
				<a href="#"><span>帮助与反馈</span></a>
			</li>
		</ul>
	</div>
</body>
</html>
```



## 鼠标经过显示边框

```css
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		div {
			width: 296px;
			height: 180px;
			/in:0px auto;
			position: relative;*/
			position: relative;
		}
		div:hover::before {   /* 鼠标经过div盒子，然后前面插入一个伪元素*/
			content: "";
			width: 100%;
			height: 100%;
			border:10px solid rgba(0,0,255,0.3);
			display: block;     /*伪元素都是属于行内元素*/
			top:0;
			right: 0;
			position: absolute;
			/*由于添加了border,会撑开盒子，所以box-sizing将padding、border都算入width里面*/
			box-sizing: border-box;
		}
	</style>
</head>
<body>
	<div>
		<img src="web_photos/images/mi.png">
	</div>
</body>
</html>
```



# 过渡(transition)

![](D:\typora\typora_images\过渡效果.jpg)

![](D:\typora\typora_images\认识过渡.jpg)

​             

```css
.timetable dd a {
      transition: all 2s;  /*与hover属性配合使用,all使得hover属性中的内容全部渐变*/
      }
 .timetable dd a:hover {
        	background-color: #00a4ff;
        	color:#fff;

        }

```

​                                       

举例：(注意：transition属性添加在原标签里面，不是添加在：hover里面)

```css
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		div {
			width: 100px;
			height: 50px;
			background-color: pink;
			/*过渡的属性，花费时间，运动曲线，何时开始*/
			transition: width 0.6s ease 0s,height 0.3s ease 0s;

		}
		div:hover {
			width: 200px;
			height: 100px;
		}
	</style>
</head>
<body>
	<div></div>
</body>
</html>
```

# 2D变形（CSS3）transform

## 移动translate(x,y)

```css
 translate(x,y)   水平方向和垂直方向同时移动（也就是X轴和Y轴同时移动）
 translateX(x)    仅水平方向移动（X轴移动）
 translateY(Y)    仅垂直方向移动（Y轴移动）
```

```css
            height: 200px;
			width: 200px;
			background-color: pink;
			/*transform: translate(50%);  水平移动100像素,自身的50%，与父级没有关系*/
            /* 以前我们让定位的盒子居中对齐*/
			position: absolute;
			left:50%;  /*以父级宽度为准*/
			/*margin-left: -100px; 移动自身的50%，不是父级的50%*/
			transform: translate(-50%); /*translate(50%)是移动自身的50%
```

## 缩放scale(x,y)

```css
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		div {
			height: 200px;
			width: 200px;
			border:1px solid red;
		/*	margin: 0 auto;*/
			position: absolute;
			left:50%;
			margin-left: -100px;  /*  等价于transform:translate(-50%);*/
			/*transition: height 1s,width 1s;*/



		}
		div:hover img {
			/*height: 150px;
			width: 150px;*/
			transform:scale(0.5);
		}

	</style>
</head>
<body>
	<div>
		<img src="web_photos/images/开心表情.png" alt="">
	</div>
</body>
</html>
```



## 旋转rotate（deg） 

deg是度数

```css
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
	div {
		height: 200px;
		width: 200px;
	}
	div img {
		transition: all 2s;  /*一定要记得渐变效果是写在这里！！*/
	}
	div:hover img {
		transform: rotate(90deg);
	}

	</style>
</head>
<body>
	<div>
		<img src="web_photos/images/开心表情.png"  alt="">
	</div>
</body>
</html>
```

## transform-origin（调整原点）

```css
 div{transform-origin: left top;transform: rotate(45deg); }  /* 改变元素原点到左上角，然后进行顺时旋转45度 */    
```

```css
div{transform-origin: 10px 10px;transform: rotate(45deg); }  /* 改变元素原点到x 为10  y 为10，然后进行顺时旋转45度 */ 
```



## 案例旋转楚乔传

```css
div {
			width: 250px;
			height: 170px;
			border: 1px solid pink;
			margin: 200px auto;
			position: relative;

		}
		div img {
			width: 100%;
			height: 100%;
			position: absolute;
			top: 0;
			left: 0;
			transition: all 0.6s;
			transform-origin: top right;
		
		}
		div:hover img:nth-child(1) {  /* 鼠标经过div  第一张图片旋转 */
			transform: rotate(60deg);
		}
		div:hover img:nth-child(2) {  
			transform: rotate(120deg);
		}
		div:hover img:nth-child(3) {  
			transform: rotate(180deg);
		}
		div:hover img:nth-child(4) {  
			transform: rotate(240deg);
		}
		div:hover img:nth-child(5) {  
			transform: rotate(300deg);
		}
		div:hover img:nth-child(6) {  
			transform: rotate(360deg);
		}
```

## 倾斜 skew(deg, deg) 

```css
transform:skew(30deg,0deg);
```

该实例通过skew方法把元素水平方向上倾斜30度，处置方向保持不变。

可以使元素按一定的角度进行倾斜，可为负值，第二个参数不写默认为0。

