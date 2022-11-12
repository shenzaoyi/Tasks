# html相关学习笔记

## 一.HTML 学习 

html是一种超文本标记语言，hyrer text marked language，意为not only just text ,还包含链接、图像、声音等。



### 1.HTML 文档结构

1.在开头必须加上<!DOCTYPE html> 且必须位于第一行，相当于一个声明，表明其为一个遵循HTML5 规范；

2.<html>和</html>，位于 文本的首尾，表明文本的开始和结束；

3.<head>和</head>标签，是用于包含HTML 文件的头部信息，其中包括文档的属性，标题，但是浏览器除了会在标题栏显示<title>元素的内容外，不会向用户显示head元素内的其他任何内容

4.<body>标签，用于包含文件的主体，是主要向用户显示内容的部分。

### 2.HTML的标签

1. **标签**由英文尖括号**<**`和**>**`括起来，如`<html>`就是一个标签;

2. html中的标签一般都是成对出现的，分**开始标签**和**结束标签**。结束标签比开始标签多了一个'/';

3. HTML标签不区分大小写;

   

   具体的HTML标签

   ***语义标签***

   1.<title>   </title>标签，用于涵盖文档的标题，并显示咋浏览器的标题处，用于向浏览者展示网页的大概内容

   2.注释标签<!--xxxxxxxx-->,此结构可以用来注释 

   3.段落标签，<p>xxxxx</p>,每一个标签内都含有一个段落

   4.标题标签，<hx>  </hx>{x|1<=x<=6};有一到六个标题，大小不一
   
   5.<span>标签

​       6.<div>   </div>确定单独的逻辑结构，说白话就是版面

​		7.<header> 顶部标签</header>  页面的最顶部内容的编辑，与之相对的，<footer> 底部标签</footer> 页面底部的内容

​		8.<section>  </section>定义区段，相比于div,这个玩意通常要有标题，节

​		9.<aside>侧边栏</aside>,但是需要css才能竖起来

***效果标签***

​		10.<br/!>换行标签，回车没有用的，斜杠可不要；

​		11。在HTML文本中，无论几个空格&回车都只会读为一个空格，而空格标签就解决了：&nbsp!;注意分号不要掉

​		12.<hr!/>与<br/!>均为空标签，只需要一个，<hr/!>为分割线

***制表***

​		13.<u!l><li!>列表，用于无序直接的条条分列；我愿称之为震惊体专用

<ul>
    <li>震惊！
     <li>浙江温州一家33口灭门惨案
         <li>竟是一男子所为
             <li>是人性的扭曲，还是道德的沦丧。

​    14.有序列表，<ol!><li!>标签，默认从1开始数，按照一两二三四五数数


<ol>
    <li>刀两断
        <li>话不说
            <li>心二意
                <li>面八方
</ol>
***图片***

15.img标签:

格式为：<img src="C:\Users\神造诣\Pictures\zeng mou ren de picture\WWUO`P)%0@S(}I3VT$`J)_E.png" title=呵呵呵呵 alt=牛>

首先是img 然后src 是图片路径，alt，title分别字面义，每一个都有等号&双引号

***链接***

16.超链接标签：语法：<!a href=目标网址>链接显示的文本<a/>  这种仅仅是在原窗口打开

17.想要打开一个新窗口，我们可以用target 属性标签；可以选择属性，第一种-self表示当前窗口打开，第二种-blank打开一种新标签页：

eg:<a href=[虎牙直播-技术驱动娱乐-弹幕式互动直播平台 (huya.com)](https://www.huya.com/) target="-blank"OR target="-self" >huya</a> 其中，self为默认的在当前页面打开，所以想要当前页面打开不用加target

***biaoge***

18.创建表格的标签：<table> 整个表格从他开始，到他兄弟结束。<tr>代表行，有几个他就有几行。<td>单元格，表格中一行几个他就几个列，<th>代表表头，border属性可以为表格添加边框，属性值为数字。caption用来定义标题；

实操一手：<table>

<caption>num</camption>

<tr> <th>一</th> <th>二</th> <th>三</th></tr>

<tr> <td>1</td> <td>2</td> <td>3</td></tr>

<tr> <td>1</td> <td>2</td> <td>3</td></tr>

<tr> <td>1</td> <td>2</td> <td>3</td></tr>

</table>



  19.表格进阶：thead,tfoot,tbody；设置表头，表脚，表身；







---

***HTML的交互：***

1.表单标签：格式：<form method="传送方式" action="服务器文件">xxxx</form>

2.表单内部：输入框：<input type="text" name="xxx" value="xxxx"文本输入

<input type="password" name="xx" value="xx" 密码输入

<input type="number" 同上； 数字输入框

<input type="url"同上；网址输入框

<inout type="email" 邮箱输入

可见：input 标签作为输入框，当type 取不同的值，输入框类型不同；

文本输入：<textarea rows="行数" cols="列数"（别掉了s）</textarea>





