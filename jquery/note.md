jquery:能解决大多数js的兼容性问题，但是不能解决css的兼容性问题
jQuery：是JavaScript库中的一种，免费的无on
Javascript库：把一些浏览器兼容性的代码或者常用的函数封装在一个js文件中
封装了很多js代码的一个js文件，就是一个js库

原因：DOM代码量大，兼容性问题多，代码的容错性很差，window.onload只能有一个

特点：解决了兼容性问题  体积小 插件丰富、开源、免费 链式编程，隐式迭代，插件丰富

jQuery中的顶级对象是jQuery，可以用$符号代替
如果想要使用jQuery中的属性或方法，jQuery.属性或者jQuery.方法(),简写为$.属性/$.方法()
大多数情况下，jQuery都是方法，属性很少
jQuery中几乎把DOM中的事件封装成了一个方法



这个按钮---如果通过DOM获取---DOM对象
	var btnObj1=document.getElementById("btn");
这个按钮---如果通过$/jQuery的方式获取---jQuery对象
	var btnObj2=$("btn");
两者是不同的对象
DOM对象转成jQuery对象，就可以使用jQuery中的方法或者属性了
如何转换：$(DOM对象)---->jQuery对象 
jQuery对象转成DOM对象
如何转换：jQuery对象[0]---->DOM对象
DOM操作很麻烦（兼容，一个功能好多代码）---转jQuery对象

jQuery操作中，有一些兼容代码没封装在jQuery中----转DOM对象

jQuery文件引入问题：代码写到引入的文件中，这时候就不执行代码，也不报错

表单标签DOM操作中设置和获取value属性的值---->对象.value
jQuery中：jQuery对象.val();---表示的是获取该元素的value属性值
jQuery对象.val("值")---表示的是设置该元素的value属性值
jQuery对象.css("css的属性名字","属性的值")---表示的是设置样式属性
注意：
.css("属性","值")中的属性可以用DOM中的写法：backgroundColor，也可以用css中的写法：background-color,更推荐第一种

DOM中页面加载事件---页面全部加载完毕才触发（标签，文字，图片，文件）
window.onload=function(){};所有js文件应该写在其中
jQuery中页面加载事件
方法1：$(window).load(function(){});---页面全部加载完毕才触发（标签，文字，图片，文件）
方法2：$(document).ready(function(){});---页面中的基本元素加载后就触发
方法3：jQuery(function(){});---页面中的基本元素加载后就触发
方法4：$(function(){});---页面中的基本元素加载后就触发

.val();----设置或者是获取表单标签的value属性值
.text();---设置或者是获取标签中的文本内容---就相当于DOM中的innerText
.css()---设置元素的css的样式属性值
.html()---设置或者是标签中的html内容---就相当于DOM中的innerHTML

总结选择器
id选择器   $("#id属性值")
标签选择器  $("标签名字")
类选择器  $(".类样式的名字")
交集选择器 $("标签名.类样式的名字")--------标签+类选择器
并集选择器 $("标签名,.类样式的名字,#id属性值")--------多条件选择器
层次选择器 $("选择器 选择器")；=========》$("dv span")；
$("选择器>选择器")；=========》$("dv>span")；
$("选择器~选择器")；=========》$("dv~span")；
$("选择器+选择器")；=========》$("dv+span")；