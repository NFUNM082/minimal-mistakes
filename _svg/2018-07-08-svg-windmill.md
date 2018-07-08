---
title:  "svg动画——旋转的风车"
modified: 2018-07-08
categories: 
  - 网页制作
tags:
  - SVG动画
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

{% include toc title="Getting Started" %}

# svg动画尝试——旋转的风车

把鼠标移到风车上试试看

<head>
    <meta charset="utf-8">
    <title>Title</title>
    <style>
    .rotate {
	    width: 500px;
      height: 500px;
		  transition: all 2.5S;
	}
	  .rotate:hover {
	    transform: rotate(1800deg); 
	    transform-origin:50% 50%; 
	}
    </style>
</head>
<body>
	<div class="rotate">
<?xml version="1.0" encoding="utf-8"?>
<!-- Generator: Adobe Illustrator 22.1.0, SVG Export Plug-In . SVG Version: 6.00 Build 0)  -->
<svg version="1.1" id="图层_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 viewBox="0 0 500 500" style="enable-background:new 0 0 500 500;" xml:space="preserve">
<style type="text/css">
	.st0{fill:#DBFF17;stroke:#000000;stroke-width:5;stroke-miterlimit:10;}
	.st1{fill:#FF2EC7;stroke:#000000;stroke-width:5;stroke-miterlimit:10;}
	.st2{fill:#00A9E7;stroke:#000000;stroke-width:5;stroke-miterlimit:10;}
	.st3{fill:#00B914;stroke:#000000;stroke-width:5;stroke-miterlimit:10;}
	.st4{fill:#FFFFFF;stroke:#000000;stroke-width:5;stroke-miterlimit:10;}
</style>
<g id="图层_1_1_">
	<polygon class="st0" points="246.5,244.5 155.8,244.5 155.8,370.8 247,461.5 	"/>
	<polygon class="st1" points="252.5,250.8 252.5,160.1 126.2,160.1 35.5,251.3 	"/>
	<polygon class="st2" points="247,256.3 337.7,256.3 337.7,130 246.5,39.3 	"/>
	<polygon class="st3" points="247,250.3 247,341 373.3,341 464,249.8 	"/>
	<circle class="st4" cx="247" cy="251" r="13.5"/>
</g>
</svg>
</div>
</body>

# 过程

先是用Ai做了风车的样式，很简单。

![windmill](https://upload-images.jianshu.io/upload_images/9437529-88b884016114b92d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

下面是让风车转的代码

```
    .rotate {
	    width: 500px;
      height: 500px;
		  transition: all 2.5S;
	}
	  .rotate:hover {
	    transform: rotate(1800deg); 
```

然后发现了一个问题就是风车不是沿着中间那个圆圈转的而是旋转中心在下方空白处。

找了旋转中心后，终于发现原来是做svg图时并不规范。也就是开始做的时候建的是一个长方形的画布，而且图形也没有居中，并非上面所展示的那样在正方形画布中间。然后就改成了目前这个样子。

并添加了代码：

```
transform-origin:50% 50%; 
```

风车就顺利转起来啦！（注意不能把速度弄得太快不然转起来看得眼瞎……）
