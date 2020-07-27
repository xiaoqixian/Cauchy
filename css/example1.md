---
author: lunar
date: Sun 26 Jul 2020 10:50:26 PM CST
---

### **CSS案例分析**

本例旨在实现一个导航栏，目标效果为：

![](https://camo.githubusercontent.com/0cfd7e2e0aed3066edb54071921b746efc3b359a/687474703a2f2f696d672e736d79687661652e636f6d2f32303138303131345f313333322e676966)

完整代码在最后。

导航栏总体可以分为三个部分：logo部分，横向列表，“加入我们”部分。

logo使用一个使用img元素的div，横向列表则使用一个ul元素，最后的“加入我们”使用底色为绿色的div。原本因为效果中“加入我们”的部分的边角是圆的，考虑使用切图的方式来做，但是我没有那张图，所以使用矩形来做了。

所以不考虑CSS部分，可以写出HTML代码为：

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>Document</title>
        </head>
    <body>
        <div class="header">
            <div class="inner_c"> <!--定义导航栏-->
                <div class="logo">
                    <img src="http://www.boyaa.com/images/logo.png" alt="">
                </div>
                <div class="list">
                    <ul> <!--定义无序列表-->
                        <li><a href="#" class="index">首页</a></li>
                        <li><a href="#">博雅游戏</a></li>
                        <li><a href="#">博雅新闻</a></li>
                        <li><a href="#">关于我们</a></li>
                        <li><a href="#">客服中心</a></li>
                        <li class="last"><a hred="#">投资者关系</a></li>
                    </ul>
                </div>
                <div class="joinus_box"> <!--加入我们-->
                    <div class="joinus">
                        <a href="https://www.google.com" target="_blank">加入我们</a>
                    </div>
                </div>
            </div>
        </div>
    </body>
</html>
```
#### **CSS部分**

写出一个网页的HTML部分代码永远是最简单的，而CSS部分则是最难的。

一些基本的CSS属性设置不讲。讲一下浮动。

浮动是CSS中一种非常神奇的属性。如果设置一个float: left;的属性。那么该元素会首先的尽可能的向上浮动，能否继续向上浮动取决与其宽度能否允许其与其它非浮动元素存在与同一行。也就是说浮动元素是无法将其它元素“挤开”的。

然后在停止浮动后，元素才会考虑靠左或靠右停靠。

**line-height**

这里的line-height是一个很神奇的属性，将其设置为与行高同样的高度，就可以使得文字垂直居中。

**display**

display属性有多种用途，对于块元素使用display: inline;可以将其变为内联元素。对于超链接，使用display: block;可以将超链接通过块状展示。同时还要通过设置text-decoration: none;将超链接的下划线去除。

**padding-left和margin-left**

padding-left和margin-left用于设置边距的厚度。padding用于设置内边距，margin用于设置外边距。

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>Document</title>
        <style type="text/css">
            *{
                margin: 0px;
                padding: 0px;
            }
            body{
                font-size: 14px;
                font-family: "Microsoft Yahei", "SimSun";
                height: 8888px;
            }
            .header{
                height: 58px;
                background-color: #191D3A;
            }
            /*版心*/
            .inner_c{
                width: 1000px;
                margin: 0 auto; /*让导航条、内容区域等部分的版心在父元素里居中*/
            }
            .header .logo{
                float: left;
                margin-right: 40px;
                margin-top: 10px;
            }
            .header .list{
                float: left;
            }
            .header .list ul{
                list-style: none;
            }
            .header .list ul li{
                float: left;
                width: 100px;
                line-height: 58px; /*让行高等于这一行的高度，保证里面的文字垂直居中*/
                border-left: 1px solid #252947;
            }
            .header .list ul li.last{
                float: left;
                width: 100px;
                line-height: 58px;
                border-left: 1px solid #252947;
            }
            .header .list ul li a{
                display: block; /*将超链接转化为块，可以霸占父亲的整行*/
                height: 58px;
                text-decoration: none; /*去除超链接的下划线*/
                color: #818496;
                text-align: center;
            }
            .header .list ul li a.index{
                color: white;
                background: #252947;
            }
            .header .list ul li a:hover{
                color: white;
                background: #252947;
            }
            .header .joinus_box{
                float: left;
                height: 58px;
                width: 100px;
                padding-left: 48px;
                padding-top: 12px;
            }
            .header .joinus_box .joinus{
                height: 34px;
                background-color: green;
                text-align: center;
            }
            .header .joinus_box .joinus a{
                display: block;
                line-height: 34px;/*将行高设置为背景图片的高度，保证超链接在背景里垂直居中*/
                text-decoration: none;
                color: white;
            }
        </style>
    </head>
    <body>
        <div class="header">
            <div class="inner_c"> <!--定义导航栏-->
                <div class="logo">
                    <img src="http://www.boyaa.com/images/logo.png" alt="">
                </div>
                <div class="list">
                    <ul> <!--定义无序列表-->
                        <li><a href="#" class="index">首页</a></li>
                        <li><a href="#">博雅游戏</a></li>
                        <li><a href="#">博雅新闻</a></li>
                        <li><a href="#">关于我们</a></li>
                        <li><a href="#">客服中心</a></li>
                        <li class="last"><a hred="#">投资者关系</a></li>
                    </ul>
                </div>
                <div class="joinus_box"> <!--加入我们-->
                    <div class="joinus">
                        <a href="https://www.google.com" target="_blank">加入我们</a>
                    </div>
                </div>
            </div>
        </div>
    </body>
</html>
```
