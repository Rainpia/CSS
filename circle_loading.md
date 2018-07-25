### 圆形进度条

#### HTML

```
<div class="circle">
  <div class="pie_left"><div class="left"></div></div>
  <div class="pie_right"><div class="right"></div></div>
  <div class="mask"><span>{{progress}}</span>%</div>
</div>
```

#### CSS

```
.circle {
  $progressSize:80px;
  width: $progressSize;
  height: $progressSize;
  position: relative;
  border-radius: 50%;
  background: #2098c3;
  margin: 0 auto;
  .pie_left, .pie_right {
    width:$progressSize;
    height:$progressSize;
    position: absolute;
    top: 0;left: 0;
    .left, .right {
      width:$progressSize;
      height:$progressSize;
      background:grey;
      border-radius: 50%;
      position: absolute;
      top: 0;
      left: 0;
    }
  }
  .pie_right, .right {
    clip:rect(0,auto,auto,$progressSize / 2);
  }
  .pie_left, .left {
    clip:rect(0,$progressSize / 2 ,auto,0);
  }
  //mask 是中间显示值的部分，它的  width + left * 2 = $progressSize
  .mask {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    left: 15px;
    top: 15px;
    background: #FFF;
    position: absolute;
    text-align: center;
    line-height: 50px;
    font-size: 14px;
    font-weight: bold;
    color: #00aacc;
  }
}
```

#### JS
```
var progress = 15 ;
var num = progress * 3.6;
if (num<=180) {
    $('.circle').find('.right').css('transform', "rotate(" + num + "deg)");
} else {
    $('.circle').find('.right').css('transform', "rotate(180deg)");
    $('.circle').find('.left').css('transform', "rotate(" + (num - 180) + "deg)");
}
if(num == 0){
  $('.circle').find('.right').css('transform', "none");
  $('.circle').find('.left').css('transform', "none");
}
```