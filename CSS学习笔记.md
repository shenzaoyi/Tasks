# CSS学习笔记

## 1.css是什么：

给网页美化的，让咋们用上美丽的网页。如字体大小，颜色等；

## 2.css代码的语法：

css代码语法由选择符和声明组成，声明则是有属性&值构成，

eg:<p>{color:blue;}可以在一个花括号内声明多个声明，中间分号不要掉

选择符（选择器说明css的作用对象）

### 具体语法

1.注释：/*   xxxxxx     */,和C语法一样

#### 按照css插入样式可分为3类，内联，嵌入，外部

---

##### 内联

即直接将css的代码直接写在HTML的标签内，尤其注意是写在开始的标签；且必须注意css标签必须写在style：”的引号之内“

eg：<p style="color:blue">hello</p> 需要注意的是前面是等号，后面是不同定义用分号，属性&值之间仍‘：’

---

##### 嵌入式

可见，当修改项目过多的时候，内联式过于麻烦，所以需要一手嵌入式来玩玩，内联式相当于告诉每个人需要做啥子，而嵌入式则相当于C中的宏定义，在每个地方都可以用，格式如下：嵌入式css必须写在<style!></style!>当中，且一般写在HTML标签的<head>内

<style type="text/css"!>
    span{
        color:blue

    }

</style>

---

##### 外联式

我们也可以将css的代码置于一个文件中，以.css为后缀使用Link标签将css文件链接到HTML文件中

eg：<!link href="**base.css**" rel="stylesheet" type="text/css" />

---

此外，css插入样式的优先级：内联>嵌入 >外联（就近原则

----

##### 选择一个标签：



1.标签选择，如<h1><html>等可以直接用格式：名字{

声明}来选择；且注意此时只要名字而不需要尖括号

2.类选择器：相当于提前做好标记，在需要改变样式的地方，在开始标签里面如<！p class="所取得别名">xxxxxxxx</P!>,然后再head 标签里面单独设值，如，.所取得别名{声明&值}

3.id选择器：跟类选择器一样，区别仅仅在，原点变成了#

---

类选择器&id选择器的区别：

1.id等于身份证，唯一仅仅可以使用一次，而class则为类选择，可以无限用

2。可以使用类选择器词列表方法为一个元素同时设置多个样式

---

4.子代选择：假如我们想要选择ul列表里面的一个li标签改变样式，则必须用>符号来实现。如：.p>span{color:red}表示将P把标签之中的span内容改颜色

5.后代选择：后代选择器，空格，表示选择标签所有后代，注意与子代选择的区别：>仅仅表示第一子代， 空格表示选择所有的后代，孙代，曾孙代；

6.通用选择器：啥都要，在{}前面加*，表示选择全部，怎么有点熟悉，像gitup,ADD加.表示全部添加

7.？伪选择，它允许给不是HTML标签的玩意改样式 eg: a:hover{color:red}（***见文末***）

8.分组选择器：，可以将多个标签作为一组一同添加css样式。eg:p,span{color:red}等价于p{color:red}&slpan{color:red}

此处一张图：

---

注意优先级：***内联样式 > id选择器 > 类选择器 > 标签选择器 > 通配符选择器***

---



##### 关于字

1.设置字体：首先选择一个标签，然后font-family:"微软雅黑"

2.设置大小：font-size:12px

3.字体粗细：font-weight：bold;

4.字体样式：font-style:normal,italic,oblique;斜体&倾斜，斜体还可以：<em>hhhhhh</em>这样,<em标签；<strong>hhhhhh</strong>加粗也可以strong来；

5.字体颜色：有rgb&十六进制&直接颜色

---

***然而以上这么多可以简写：font ：后面直接放所有属性，属性之间用分号***

---



##### 文本修饰

1.加根线：underline ,upline ,line-through,eg:text-decoration:underline;

2.段首空格：p{text-indent:2em},缩进

3.行高：line-height：2em；

4.letter-spacing & word-spacing 字母间距&单词间距

5.块状元素居中&左右对齐：text-align:center&right&left;

---

---

---



##### css的盒模型

在css中，每个 HTML元素都是一个矩形盒子，包括四个区域，内容区域，内间距区域（padding），边框区域（border），外边距区域（margin），

###### HTML元素分类：做他一表

<table>
    <tr>
        <td>块状元素 </td>
        <td>内联元素</td>
        <td>内联块状元素</td>
    </tr>
   <tr>
       <td>div、p、h1...h6、ol、ul、dl、table、address、blockquote 、form</td>
       <td>a>、span>、br>、i>、em>、strong>、label>、q>、var>、cite>、code></td>
       <td>img、input</td>
    </tr>
</table>



1，块状元素：1.容器，2.排斥与其他元素同一行，3..width，height起作用，，，**块状元素有一个特点之一：在不设置宽度的情况下，显示为父容器的100%**

2，内联元素：1，只能容纳文本和其他内联元素，2.可以与其他内联元素同一行，3.width，height不起作用

---

内联元素可以做强制转换：

diaplay:block;强转为块状元素。 display:inline;强转为内联元素。display:inline-block;同理，注意是inline先

而隐藏元素的时候：display:none;就啥也看不见

---

###### 盒模型的宽度高度与我们平常所说的不一样：

![](https://img.mukewang.com/539fbb3a0001304305570259.jpg)

元素实际宽度（盒子的宽度）=左边界+左边框+左填充+内容宽度+右填充+右边框+右边界

---

######  把盒子变得好看

1.设置背景颜色：background-color:red;

2.设置边框：盒子的边框就是围绕着内容&补白的线，可以设置颜色，样式，宽度；

例子：border：2px solid red;这是简写，原为：{border-size:2px;border-color:red;border-style:solid}

border边框常见样式：solid（实线），dashed（虚线），dotted（点线）

3.盒子的四面八方：border-top,border-bottom,border-right,left提供我们只修改盒子一条边

4.边框原角:border-radius:10px,20px,30px,40px;<=>border-top-right:20px.........

If 四个角全为相同的角度，border-radius:20px;      有趣的是：一个正方形，当设置圆角效果值为元素宽度一半时，显示效果为圆形

此处一图：

5. 内边距：padding，也分为四个方向，eg:padding-top:20px; 
6.  {margin:20px 30px 30px 30px}中间用空格，也可以单独设置

---

---

---

#### css布局moxing

1.总体分类：flow流动型，float浮动型，layer，层模型

2.flow型：，**块状元素**都会在所处的**包含元素内**自上而下按顺序垂直延伸分布，因为在默认状态下，块状元素的宽度都为**100%**。实际上，块状元素都会以行的形式占据位置，在流动模型下，**内联元素**都会在所处的包含元素内从左到右水平分布显示

3.float模型：让两个块状元素并排显示，float：left or right;左右对齐并排；也可以单独设置左右实现左右分别对其浮动，类似于强转，float:left;左浮动；

4.层模型：	静态定位：position：static；

​					绝对定位：首先需要设置position:absolute;然后使用四个方位对其进行绝对定位，对于其最接近的一个具有定位属性的父包										含块进行绝对定位。如果不存在这样的包含块，则相对于body元素，即相对于浏览器窗口。

​					相对定位：首先需要设置position:relative;

​					固定定位：首先需要设置position:fixefd;

相对于其他元素定位 ：relative&absolute;

---

---

---



 ##### 弹性盒模型

1.flex属性：在父元素设置display:flex；将块级元素在一行显示；

2.justif-content属性：可取值有；flex-start;flex-end;center;space-between;space-around;

3,交叉轴上面的对齐方式：align-item;可取值为：flex-start;flex-end;center;baseline;stretch;



##### 伪类

1.啥事伪类

当已有元素处于某个状态时，**特殊状态**为其添加对应的样式，人话一点例如鼠标在链接上面链接有改变；hover

2. ​	a:{text-decoration:none}    a:hover{text-decoration:underline;


***new***
    # css定位机制
## 一.文本流定位---flow
文本流☞按照文本的规则，由上到下，由左到右分布，其中，HTML标签分为块状元素（block），行内元素（inline) & 块状行内元素（inline-block）。block独占一行，可以设置width，height，Margin等。inline则并不独占一行，并且他还不能设置width&height，其width是由标签内所容纳的图片或文本的宽度决定。

## 二.浮动定位--float
浮动定位是指元素脱离文本流，浮动起来，并且此时原来的位置已经失去，可以用float:right/left/center,来定义，也可以用clear来清除浮动，取值为：left，right，both。

除此之外，float属性还有一些特点：下降&下降卡住
![下降&卡住](C:\Users\神造诣\Pictures\Saved Pictures\Screenshot_20221121_161208.jpg)
clear属性用处：
![](C:\Users\神造诣\Pictures\Saved Pictures\Screenshot_20221121_161347.jpg)
![](C:\Users\神造诣\Pictures\Saved Pictures\Screenshot_20221121_161404.jpg)

## 三.层定位--layer
position属性：fixed固定定位，relative相对定位，absolute绝对定位，static（意思为静止的）此处指默认，在四个属性中，只要static对z-index生效。

<ul>
<li>fixed：固定的，也不随网页的下翻而消失，常见于小广告，早easypage里面的传奇体现。
<li>relative:相对的，定位为relative的元素脱离文档流，但是但是，其原位置依然存在，他的特点是总是相对其直接父元素定位。
<li>absolute：绝对定位，对于absolute定位总是相对于其最近的定义为absolute or relative 的父层，if没有，则相对于body.
将absolute&relative归纳为偏移定位（自己取的），均是根据top,bototm,right,left来相对父层定位。











