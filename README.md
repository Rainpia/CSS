# CssDemo

#### multipleColumnEqualHeight.html
```
尝试多列等高问题，
利用padding-bottom|margin-bottom正负值相抵, 保持内容的高度；
设置父容器设置超出隐藏（overflow:hidden），这样父容器的高度就还是它里面的列没有设定padding-bottom时的高度，
当它里面的任 一列高度增加了，则父容器的高度被撑到里面最高那列的高度，
其他比这列矮的列会用它们的padding-bottom补偿这部分高度差。
```

#### selectOptionCheckStyle.html
```
解决html element select -> options 默认样式问题，
option 默认 focus checked 状态 background 是 blue， color 是 white ; blur checked 状态 background 是 grey ， color 是black 
使用-webkit-text-fill-color  and background linear-gradient 模式可以覆盖彻底覆盖默认样式
```
