Css知识点
1.CSS指的是层叠样式表，样式表通常存储在样式表中。
可以在<head>或者<body>中进行编写样式
语法：p{color:red;text-align:center};

2.CSS的ID和Class
区别：id选择器可以为特定id的HTML元素指定特定的样式；class选择器可以为一组元素设置样式，可以有多个元素的class设置为一样的。

3.样式表的位置信息
	外部样式表：必须在<head>中使用link标签
	内部样式表：在头部中的<style>中进行编写样式
	内联样式：标签内编写样式 <p style="color:red;margin-left:20px">段落</p>
样式的优先级：
	内联样式>外部样式>浏览器默认样式
优先级顺序：
	通用选择器(*)	元素(类型)选择器	类选择器(.)		属性选择器		伪类	ID选择器	内联样式	important规则除外
	内联样式1000	ID选择器100		class类选择器10		HTML标签选择器1
	
4.Css背景
	background-color	
	background-image	
	background-repeat:水平或垂直方向铺平。		background-repeat：repeat-x;
	background-attachment:背景图像是否固定或者随着页面的其余部分滚动。		background-attachment：fixed；固定的
	background-position：改变图像在背景中的位置 center-top

5.Css文本属性
	（1）Css文本格式
		①文本对齐方式
			text-align：center；
		②文本修饰：设置或删除文本的装饰
			text-decoration：none；	（overline/line-through/underline）

	（2）文本转换
		是用来指定在一个文本中的大写或者小写字母。全部大写、全部小写、首字母大写 
		text-tranform：uppercase；	lowercase/capitalize

	（3）文本缩进
		text-indent：50px；
		
	（4）文本颜色：color
	（5）文本方向：direction
	（6）字符间距：letter-height
	（7）设置文本阴影：text-shadow
	（8）控制元素中的字母：text-transform
	（9）文本垂直对齐：vertical-align
	（10）字间距：word-spacing
	（11）设置行高：line-height
	（12）设置元素中空白的处理方式：white-space
	（13）禁用元素内的文字环绕：white-space：nowrap
	letter与word区别：
	单词之间的间距用word，字母与字母之间的间距用letter

10.Css文本字型
	字体系列：Font-Family："宋体"
	字体样式：Font-style：normal；		italic/oblique
	字体大小：Font-size：40px；		（16px=1em）
	设置字体加粗：Font-Wight：normal;	(lighter/bold/)
	设置字体的转变：Font-variant：normal;	(small-caps)
	
11.Css链接
	链接状态：
	（1）a:link			正常，未访问的链接
	（2）a:visited		用户已访问的链接
	（3）a:hover		当用户鼠标放在链接上时
	（4）a:active		链接被点击的那一刻
	a:link{color:red;}		a:link{background-color:red;}
	注意：hover必须在link和visited之后，active必须在hover之后
	
12.Css列表
	列表样式的类型list-style-type：circle；	（square、upper-roman、lower-alpha）
	列表项标记的图像：list-style-image：url（‘a.jpg’）;
	Css列表属性：
		list-style；简写属性
		list-style-image；将图像设置为列表项标志
		list-style-position：设置列表项中列表项标志的位置
		list-style-type；设置列表项标志的类型

13.Css表格
	指定Css表格边框，使用border属性
		border:1px	solid	red;
	折叠边框：border-collapse：collapse；
	caption：定义表格的标题
		caption {caption-side:bottom;}
	
14.Css盒子模型
	margin：外边距
		定义元素周围的空间，没有背景颜色，完全透明。可以用负值。
	border:边框
	padding：内边距填充
		p.padding{padding-left:2cm;}
	content：内容，显示文本和图片
	总元素的宽度：宽度+左填充+右填充+左边框+右边框+左边距+右边距
	
15.边框属性 
	border-style：none；默认无边框	（dotted-点线边框	dashed-虚线边框	 solid-实现边框	
	double-定义两个边框	 groove-定义3d沟槽边框	ridge-定义3d脊边框	inset-3d嵌入边框  outset-3d突出边框）
	border-weight：5px；	边框宽度
	border-color：red；		边框颜色
	border-top：dotted；	单独设置各边	（top、bottom、left、right）

16.Css轮廓
	outline
	outline-color	设置轮廓的颜色
	outline-style	设置轮廓的样式
	outline-width	设置轮廓的宽度
	例子：outline：green dotted thick；

17.嵌套选择器
	p{}:为所有p元素指定一个样式
	.marked{}:为所有class=“marked“元素内的p元素指定一个样式
	.marked p{}:为所有class=“marked”元素内的p元素指定一个样式
	p.marked{}:为所有class=“marked”的p元素指定样式

18.Css的Display(显示)和visibility(可见性)
	display属性设置一个元素应该如何显示 
	visibility属性设置一个元素应可见还是隐藏
	display：none；可以隐藏某个元素，且隐藏的元素不会占用任何空间。
	visibility：hidden；可以隐藏某个元素，但隐藏的元素仍然占用与未隐藏之前一样的空间。
	
19.Css的Position定位
	共5个
	①static：默认值，没有定位。
	②relative：相对定位元素的定位是相对其正常位置。
	③fixed：元素的位置相对于浏览器窗口是固定位置。不占据位置空间。
	④absolute：绝对定位的元素相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于<html>
	⑤sticky：粘性定位，基于用户的滚动位置来定位 
	重叠的元素：Z-index属性指定可一个元素的堆叠顺序。(哪个元素应该放在前面或者后面)
	
	如何设置元素的外形：img{position:absolute;clip:rect(0px,60px,200px,0px)} 
	overflow：属性规定内容溢出元素框时发生的事情。


20.如何改变光标
	<span style="cursor:auto">auto</span><br>
	(crosshair/default/e-resize/help/move/n-relize/nw-relize/pointer/progress/se-resize/sw-resize/text/w-resize/wait)

21.Css浮动(float)
	会使元素向左或向右移动，其周围的元素也会重新排列，往往用于图像，但在布局时一样非常有用。
	清除浮动：clear；
	
22.Css布局（水平&垂直对齐）
	元素居中对齐：如果没有设置width属性，居中将不起作用。
	
	
23.Css组合选择符
	后代选择器(以空格分隔)
	子元素选择器(以大于号分隔）(>)
	相邻兄弟选择器（以加号分隔）<+>
	普通兄弟选择器（以破折号分隔）<~>

24.Css伪类
	CSS伪类是用来添加一些选择器的特殊效果。
	语法：
		伪类的语法：
			selector:pseudo-class {property:value;}
		CSS类也可以使用伪类：
			selector.class:pseudo-class {property:value;}
		伪类可以与 CSS 类配合使用：
			a.red:visited {color:#FF0000;} <a class="red" href="css-syntax.html">CSS 语法</a> 	如果在上面的例子的链接已被访问，它会显示为红色。
	Css伪元素
		:first-line（向文本的首行设置特殊样式）
		:first-letter(向文本的首字母设置特殊样式)
	
	伪元素和Css结合
	p.article:first-letter{color:#ff0;}
	<p class="article">文章段落</p>
	
	:before(伪元素在元素的内容前面插入新内容)
		h1:before{content:url(a.jpg);}
	:after(在每个p元素之后插入数据)

25.Css导航栏
	垂直导航栏：
		激活/当前导航条实例：在点击了选项后,我们可以添加“active”类来标准哪个选项被选中。
	水平导航栏：
		使用内联和浮动。
			

	
