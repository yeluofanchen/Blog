# CSS动画

## 前言

灵魂三问?

1. 为啥子要搞CSS 动画?

为了页面元素更加丰富, 内容更加多样化.

2. 什么是 CSS 动画?

首先要理解, 什么是动画? 先看下[维基百科](https://zh.wikipedia.org/wiki/%E5%8A%A8%E7%94%BB)上对于动画的定义.

> 动画（英语：Animation）是一种通过定时拍摄一系列多个静止的固态图像（帧）以一定频率连续变化、运动（播放）的速度（如每秒16张）而导致肉眼的视觉残象产生的错觉——而误以为图画或物体（画面）活动的作品及其视频技术。 

回想之前看的动画, 进击的巨人, 灌篮高手, 其实在动画创作过程是有原稿这一步的, 也就是静止的画面. 当这些静止的画面连播的时候, 肉眼因为视觉残象产生的错觉, 而误以为是活动的画面, 就成了动画.

那么 CSS 动画也是同样的道理了, 用 CSS 实现的动画呗.

3. CSS 动画怎么用? 有哪些需要注意的点呢?

CSS 动画有几种不同的方式, 今天主要讲使用 `transition `和 `animation`来实现 CSS 动画. 在这之前, 需要先理解一下**浏览器渲染原理**.

## 浏览器渲染原理

### 怎么查看浏览器的渲染过程?

开发者工具-ESC-打开`Rendering`-勾选第一个`Paint flashing`, 观察页面视口的颜色变化, 变绿色的话就是浏览器在重新渲染页面.

### 浏览器渲染的过程：

1. 根据HTML标记并构建DOM树
2. 根据CSS构建CSS树（CSSOM）
3. 将两棵树合并成一棵渲染树（render tree)
4. layout布局（文档流，盒模型，计算大小或位置等）
5. paint绘制（边框颜色，背景颜色，阴影等绘制）
6. compose合成（根据层叠关系展示画面）

![渲染树-render tree](https://gitee.com/xiefengjun/images/raw/master/test/image-20210318111104380.png)

### 更新样式的三种方式:

1. JS / CSS > 样式 > 布局 > 绘制 > 合成

![JS / CSS > 样式 > 布局 > 绘制 > 合成](https://gitee.com/xiefengjun/images/raw/master/test/image-20210318111558773.png)

根据浏览器的渲染原理，若是开发者更新了样式（即元素的几何属性，类似于宽高，位置等），则浏览器会检查所有属性然后重新绘制，最后再合成。

2. JS / CSS > 样式 > 绘制 > 合成

![JS / CSS > 样式 > 绘制 > 合成](https://gitee.com/xiefengjun/images/raw/master/test/image-20210318111658300.png)

如果开发者只是更新了`paint only`的属性（例如背景，文字颜色等），由于不影响页面布局，则浏览器直接执行绘制。

3. JS / CSS > 样式 > 合成

![JS / CSS > 样式 > 合成](https://gitee.com/xiefengjun/images/raw/master/test/image-20210318111807819.png)

在开发者只是更改一个既不更改布局也不需要绘制的属性时，浏览器将只执行合成，例如动画(animation)和`transform`。

可以用以下网址查询不同的CSS属性会触发的不同过程：

https://csstriggers.com/



以上总结自Google 官方文章:

[渲染树构建、布局及绘制](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-tree-construction)

[渲染性能](https://developers.google.com/web/fundamentals/performance/rendering/)

[坚持仅合成器的属性和管理层计数-即, 使用 transform 来实现动画](https://developers.google.com/web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count)



## CSS 动画的两种做法（transition 和 animation)



用transform+ transition + hover

http://js.jirengu.com/nonud/1/edit?html,css,output

用animation实现

http://js.jirengu.com/lesokosaki/1/edit?html,css,output





















