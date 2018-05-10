# CssDemo

#### multiple_column_equal_height.html
```
尝试多列等高问题，
利用padding-bottom|margin-bottom正负值相抵, 保持内容的高度；
设置父容器设置超出隐藏（overflow:hidden），这样父容器的高度就还是它里面的列没有设定padding-bottom时的高度，
当它里面的任 一列高度增加了，则父容器的高度被撑到里面最高那列的高度，
其他比这列矮的列会用它们的padding-bottom补偿这部分高度差。
```

#### select_option_check_style.html
```
解决html element select -> options 默认样式问题，
option 默认 focus checked 状态 background 是 blue， color 是 white ; blur checked 状态 background 是 grey ， color 是black 
使用-webkit-text-fill-color  and background linear-gradient 模式可以覆盖彻底覆盖默认样式
```
#### px, em, rem, %, vh, vw, vm [参考博客](https://www.jianshu.com/p/82f02af17e78)
```
1, px
px 就是像素，是一种绝对单位
2, em
em 是一种相对单位；
font-size的参照物是父元素字体大小，1em 等于一倍的父元素字体大小；
其他的(border, width, height, padding, margin, line-height)都是相对于当前元素的字体大小，1em 等于一倍的当前元素字体大小；
3, rem
rem 是一种相对单位；
它的参照物是根元素html，新技术，不支持ie8以下，但是移动端支持良好
4, %
如果对 html 元素设置 font-size 为百分比值，则是以浏览器默认的字体大小16px为参照计算的（所有浏览器的默认字体大小都为 16px），如62.5%即等于10px（62.5% * 16px = 10px）。
5, vh,vw,vm,
它们也是相对单位，是基于视窗大小（浏览器用来显示内容的区域大小）来计算的。
* vw：基于视窗的宽度计算，1vw 等于视窗宽度的百分之一

* vh：基于视窗的高度计算，1vh 等于视窗高度的百分之一

* vmin：基于vw和vh中的最小值来计算，1vmin 等于最小值的百分之一

* vmax：基于vw和vh中的最大值来计算，1vmax 等于最大值的百分之一

举个例子：浏览器高度900px，宽度1200px，取最小的浏览器高度， 1 vmin = 900px/100 = 9 px，1 vmax = 1200px/100 = 12 px。
现在vm的兼容性较差

注：chrome 浏览器最小的字体为 12px，如果设置 10px 也会渲染成 12px 。
```