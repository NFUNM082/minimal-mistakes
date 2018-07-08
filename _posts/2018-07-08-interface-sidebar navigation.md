---
title:  "界面设计-侧边栏导航"
modified: 2018-06-26 T16:03:49-04:00
categories: 
  - 界面设计
tags:
  - 笔记 
classes: wide
header:
  overlay_image: /images/interface.jpg 
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
#  cta_label: "More Info" 
#  cta_url: "https://unsplash.com"
  caption:
excerpt: '网页界面设计'
sidebar:
  nav: "docs"
---

{% include base_path %}
 
{% include toc title="目录" %}

 
  
昨天尝试了增加侧边栏导航，成功了，所以今天来介绍下是怎么尝试成功的。

有关教程看这里 https://mmistakes.github.io/minimal-mistakes/docs/layouts/#custom-sidebar-navigation-menu

![Custom sidebar navigation menu example](https://upload-images.jianshu.io/upload_images/9437529-0828e8ad911ee659.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

---

## 添加侧边栏导航步骤

参照上面的教程，我做了如下的修改：

在_config.yml中添加如下代码

```
  # _docs
  - scope:
      path: ""
      type: docs
    values:
      sidebar:
        nav: "docs" 
```

在_data/navigation.yml中增加如下（一部分示例）
```
docs:
  - title: svg制作
    children:
      - title: "SVG的历史"
        url: https://nfunm082.gitee.io/minimal-mistakes/svg/2018-07-02-svg-history/
      - title: "SVG尝试"
        url: https://nfunm082.gitee.io/minimal-mistakes/svg/2018-07-02-svg-try/
      - title: "svg动画"
        url: https://nfunm082.gitee.io/minimal-mistakes/svg/2018-07-07-svg-train/
```

然后在相应的每一篇文章的开头添加这一小块：
```
sidebar:
  nav: "docs"
```

这样就成功了啦！
![侧边栏导航](https://upload-images.jianshu.io/upload_images/9437529-b748a5a4635b8cd8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

---
## 注意的点

其实这个操作是非常简单的，只要看懂了教程就很容易。虽然教程是英语的，但是翻译成中文后很容易理解。

还有一个很重要的点：一定要用Chrome浏览器查看是否成功，我之前使用其他浏览器的时候以后没成功改了好几次，后来才发现是浏览器的问题。这个侧边栏导航在其他浏览器上看不了的得用Chrome才能看到。

