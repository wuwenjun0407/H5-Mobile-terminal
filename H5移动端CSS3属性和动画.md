# H5移动端CSS3属性和动画

@(H5移动端知识)


### CSS3属性
#### 滤镜 filter
|属性|描述|默认值|
|--|--|--|
|filter:blur(10px|改变图片的清晰度|0|
|filter: brightness(50%|改变图片的亮度 |100%|
|filter: grayscale(100%) |灰度|100%|
|filter: invert(100%| 做出来的效果就像是我们照相机底面的效果一样|100%|
|filter：sepia（10%| 复古|100%|
|filter：saturate（50%）|图片的饱和度|100%|
|filter：hue-rotate（50deg|改变图片色相|0deg|
|filter:opacity（20%）|改变图片的透明度 |100%|
|filter：contrast（20%）|改变图片的对比度|100%|
|filter：drop-shadow（5px 5px 5px rgba(0,0,0,.2)）|给图片加阴影效果|无|

```
 div{
       margin: 0 auto;
       filter: blur(10px);
       filter: brightness(50%);
       filter: grayscale(100%);
       filter: contrast(20%);
       filter: invert(100%);
       filter：drop-shadow（5px 5px 5px rgba(0,0,0,.2)）;
       filter: brightness(50%);
       filter:opacity（20%）;
       filter：hue-rotate（50deg）;
       
        width: 600px;
        height: 200px;
       background-size: 100%   ;
       -webkit-background-size: 100%;
            background: url("img/timg.jpg") no-repeat center ;
        }
```

### D转换 transform

#### 移动
```
 <style>
        img{
            display: block;
            width: 200px;
            height: 200px;
            /*transform: translate();*/
            transition: transform 1s linear 1s（延时1s,在1s的时间内移动下面的像素）,height 0.8s linear 1s,（高度在延时1s，在0.8s的时间内增加）width 0.8s linear 1s;（宽度在1s的延时后，在0.8s的时间内增加）
        }
        .parent:hover img{
            transform: translate(100px,100px);
            鼠标移上向X轴移动100px,Y轴移动100px
            height: 600px;
            width: 600px;
        }
    </style>


<div class="parent">
    <img src="img/timg.jpg" alt="">
</div>
```
#### 旋转
```
<style>
        .parent{
            background: forestgreen;
        }
        img{
            display: block;
            width: 200px;
            height: 200px;
            transition: 0.8s;
            在0.8s的时间内
        }
    
        .parent:hover img{
            transform: rotateY(180deg);
            沿Y轴顺时针旋转180度
        }
    </style>
<div class="parent">
    <img src="img/timg.jpg" alt="">
</div>
```
#### 缩放
```
      img{
            display: block;
            margin: 100px auto 0;
            width: 200px;
            height: 200px;
            transition: 5s;

        }
        .parent:hover img{
            transform: scale(0,0);
            沿X和Y轴向内缩放图片在页面上显示。X和Y轴数值增加，表示放大多少倍。
        }

    </style>
<div class="parent">
    <img src="img/timg.jpg" alt="">
</div>
```

### 动画
#### 给元素添加动画效果
##### 第一步 定义一个动画 从开始到结束
##### 第二步 给一个元素添加上这个动画，并且定义这个动画的一些属性，例如时间，运动方式，执行次数
```
  <style>
        #myDIV{
            position: absolute;
            width: 300px;
            height: 200px;
            background: salmon;
            animation: myDIV 20s ;
        }
        @keyframes myDIV {
            0%{left:0;}
            50%{left: 1075px;}
            100%{left: 0;}
        }
        span{
            position: absolute;
            z-index: 1;
            top: 180px;
            border: 30px dashed;
            border-color: yellow red;
            border-radius: 50%;
            animation: car 1s infinite;

        }
        @keyframes car {
            from{transform: rotate(0deg);}
            to{transform:rotate(360deg);}
        }
        .left{
            left: 20px;
        }
        .right{
            left: 220px;
        }
    </style>

<div id="myDIV">
    <span class="left"></span>
    <span class="right"></span>
</div>
```
     