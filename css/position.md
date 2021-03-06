---
author: lunar
date: Sun 26 Jul 2020 05:09:22 PM CST
---

### **CSS定位属性**

CSS的定位属性有三种：绝对定位、相对定位、固定定位。

```css
position: absolute;
position: realtive;
position: fixed;
```

#### **相对定位**

相对定位：让元素相对于自己的位置进行偏移。

```css
position: relative;
left: 50px; /*横坐标：正值表示向右偏移，负值表示向左偏移 */
top: 50px; /*纵坐标：正值表示向下偏移，负值表示向上偏移 */
```

如图的代码即相对原来的位置向右偏移50px，向下偏移50px。

相对定位的真实位置还是留在原来的地方，只不过与原来的地方偏移了。其它元素不能占用该元素原来的地方。

#### **绝对定位**

绝对定位的盒子脱离了标准文档流。所以可以通过绝对定位将元素覆盖在其它元素上面。

**绝对定位的参考点**

如果是用top描述，那么参考点就是页面的左上角，而不是浏览器的左上角。意思是当页面滚动时，那么元素会跟着滚动。

如果是bottom描述，参考点就是页面的左下角。

通过left和right来分别描述在行坐标上距左边或右边的距离

**子绝父相**

所谓子绝父相：即如果父辈元素出现了已经定位的元素，那么子辈的元素的绝对定位都是相对于父辈元素而言的。而不是相对于整个页面。

**top与margin-top的区别**

top专用于决定定位，只有在定义了position:absolute;的情况下才可以使用；而margin-top则用于相对定位,表示相对于相邻元素的距离。

#### **相对定位**

元素相对与自己原来的位置进行调整。其它元素不能霸占自己原来的位置。

注意left,right,top,bottom等属性与移动方向是相反的。

#### **固定定位**

固定定位即盒子的位置不随窗口的滚动而变化。通常导航栏就可以用这个做。

#### **z-index属性**

z-index属性：正整数，数值大的盖住数值小的。如果都没有设置这个属性，则后写的HTML代码盖住前面写的。

其次，只有定位了的元素才可以使用这个值，本文讲到的三种定位都可以，但是浮动不可以。

从父现象：只有父类没被其它元素盖住，子类元素才可能显现，不管子类的z-index值多大。
