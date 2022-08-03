# HTML
### 基础标签
* `<sub></sub>下标`
* `<sup></sup>上标`
* `<small></small>缩小`
* `<big></big>放大`
* `<mark></mark>标记文本（带背景色）`
* `<del></del>删除线`
* `<ins></ins>下划线`
* `<hr>横线`
* `<input>` type类型

* #### 图像标签

 > 给img标签添加usemap属性，map标签使用同样的name属性，包裹area标签，area标签通过绘制区域完成可点击部分：  
 > shape定义类型；coords定义关键点坐标；  
 > rect：矩形； circle：圆形； poly：多边形； default：整个区域；  
 > 矩形通过↖↘俩点坐标；圆形通过圆心+半径；多边形通过无数点坐标连接
  
```
<img src="workplace.jpg" alt="Workplace" usemap="#workmap">
<map name="workmap">
  <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">
  <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm">
  <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm">
</map>
```
 > picture标签  
picture元素包含一个或多个元素，每个元素通过 属性<source>引用不同的图像。srcset这样浏览器可以选择最适合当前视图和/或设备的图像。每个<source>元素都有一个 media属性，用于定义图像何时最合适。

```
<picture>
  <source media="(min-width: 650px)" srcset="img_food.jpg">
  <source media="(min-width: 465px)" srcset="img_car.jpg">
  <img src="img_girl.jpg">
</picture>
```

***********

### H5新标签

* `<header> <nav> <main> <article> <section> <aside> <footer>`
* `<video>视频标签`
  > loop 自动循环  controls 增加控制条  autoplay 自动播放  poster 预览图 

