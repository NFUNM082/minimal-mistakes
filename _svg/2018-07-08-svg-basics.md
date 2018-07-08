---
title:  "svg动画"
categories: 
  - 网页设计
tags:
  - svg
classes: wide
excerpt: "制作svg动画"
header:
  overlay_image: /images/svg.jpg
  # caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
# cta_label: "More Info"
# cta_url: "https://unsplash.com"
sidebar:
  nav: "docs"
---
{% include base_path %}

{% include toc title="目录" %}

# svg动画基础示例

以下动画代码参考于菜鸟教程然后自己进行尝试，都是最基本的动画。

## 盒阴影

<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style> 
#box-shadow {
    width: 100px;
    height: 100px;
    background-color: #ea8b3d;
    -webkit-animation: mymove 6s infinite; /* Chrome, Safari, Opera */
}

/* Chrome, Safari, Opera */
@-webkit-keyframes mymove {
    30% {box-shadow: 10px 20px 20px #e3b265;}
}

</style>
	</head>
	<body>
<div id="box-shadow">
</div>
	</body>
</html>

阴影会动

## 跳

<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style> 
#clip {
    width: 200px;
    height: 200px;
    background-color: coral;
    position: absolute;
    -webkit-animation: mymove 2s infinite; /* Chrome, Safari, Opera */
}

/* Chrome, Safari, Opera */
@-webkit-keyframes mymove {
    50% {clip: rect(0px, 30px, 30px, 0px);}
}

}
</style>
	</head>
	<body>
		<div id="clip">
        </div>
	</body>
</html>

这个没什么，觉得很傻一直闪来闪去，有点好玩但其实没什么用，看看就行了。

## 放大

<html>
	<head>
  <meta charset="UTF-8">
   <style>
    .demo {
	    width: 100px;
        height: 100px;
        background-color: #81f1bb;
        transition: width 2s,height 2s;
	}
	.demo:hover {
	    width: 200px;
        height: 200px;
	}
   </style>
</head>
	<body>
		<div class="demo" ></div>
	</body>
</html>

鼠标移动到图形上会开始变化

## 变颜色

<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<style> 
#color {
    width: 300px;
    color: red;
    -webkit-animation: mymove 5s infinite; /* Chrome, Safari, Opera */
    animation: mymove 5s infinite;
}

/* Chrome, Safari, Opera */
@-webkit-keyframes mymove {
    50% {color: blue;}
}
	
</style>
	<body>
		<div id="color">
         <p>这个是会变色的</p>
         </div>
	</body>
</html>

# 体会

这些都是最基本的操作，就列出了几个。用几行代码就可以轻松实现，参考各种属性值来实现 。