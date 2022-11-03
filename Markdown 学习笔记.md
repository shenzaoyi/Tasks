# Markdown &Git&GitHup 学习笔记

## 一.对markdown的了解   

  这种语言吸收了很多在电子邮件中已有的纯文本标记的特征。在许多网站都通用。 Markdown是一种轻量级标记语言，创始人是约翰·格鲁伯(John Gruber)。它允许人们 “使用易读易写的纯文本格式编写文档，然后转换成有效的 HTML 文档。(来自维基百科) 简单地说，markdown语法和HTML语言（准备有空再尽快了解）一样，使用符号代替样式。有人评论，markdown相比于word，其本质是让人们回归到内容本身，注重文章本身结构，而不是样式。markdown对比word，更简洁，没有花里胡哨的界面、功能，使创作者能更加专注于文本本身。除了简便之外，其良好的兼容性也独具一格。
## 二.markdown的基本语法

首先是一篇详细的语法（from 知乎）[Markdown语法及原理从入门到高级（可能是全网最全](https://zhuanlan.zhihu.com/p/99319314)

'#'的个数来表示标题

'---'来表示分割线

'*'表示加粗

'**'表示斜体

'>'表示引用

‘[]()’表示链接

'![]()'表示图片

表格的表示
使用一根竖线来分隔各个单元格，使用冒号来决定单元格的对齐方向

## 三.markdown的个人使用举例

---



分割线

*hello world!* 斜体---



**hello world！** 加粗

---



***hello world！***斜体加粗

---



[1024程序员节](https://tw93.netlify.app/)    表示网站

---



表示图片：

![](![-2a003e3b5513968c.jpg (72×78) (raw.githubusercontent.com)](https://raw.githubusercontent.com/shenzaoyi/picture/main/-2a003e3b5513968c.jpg)
)
---



> to be or not to be,is a problem! 

引用

---



表格：

| 曾   | 子   | 豪   |
| ---- | ---- | ---- |
|      |      |      |







关于标题、脚注等markdown的基本用法归纳视频

【8分钟让你快速掌握Markdown】https://www.bilibili.com/video/BV1JA411h7Gw?vd_source=d25055abd0d2973fb03b7b091790844e    (按住CTRL然后点击可以查看)





## 关于GITHUP的学习笔记

​	GitHup即时被人调侃为同性交友平台的网站，但事实上，GitHub是一个软件源代码托管服务平台，按照本人的理解咧，就是程序员将自己辛辛苦苦敲的代码托管到一个网站上，也就是GitHup。它能；保留各个版本的代码，也就是从项目雏形到大功告成，也可以将自己的代码公开，供别人白嫖（doge）免费使用。但是必须遵守开源规则。而我也是成功创建了自己的仓库，完成了笔记，虽然还没有到需要嫖代码的时候，但我确定，我和老Gethup在未来一定会和睦共处。:smile:(刚学会的表情功能必须秀一下):sob:

---



​	![picture](![1667221071107.jpeg (720×495) (raw.githubusercontent.com)](https://raw.githubusercontent.com/shenzaoyi/picture/main/1667221071107.jpeg))

来自知乎的神奇GitHup介绍

---





## 关于Git的学习笔记1

### 1.专业术语

Git 是一款免费、开源的分布式版本控制系统，也是当今最为流行的版本控制系统之一，在众多的项目开发中普遍使用。

## 2.个人理解

![](![IMG_20221031_214637.jpg (4208×3120) (raw.githubusercontent.com)](https://raw.githubusercontent.com/shenzaoyi/picture/main/IMG_20221031_214637.jpg))



## 关于Git的学习笔记2

### 1.专业术语

Git 是一款免费、开源的分布式版本控制系统，也是当今最为流行的版本控制系统之一，在众多的项目开发中普遍使用。其特点是版本控制，以及版本回溯 。

## 2.git的运作流程

首先来一张专业的图（网上找的 :smile:）

![](C:\Users\神造诣\Desktop\[v2-49c265e6c878e26b314702d1f1cb9ee4.jpeg (666×242) (raw.githubusercontent.com)](https:\raw.githubusercontent.com\shenzaoyi\picture\main\v2-49c265e6c878e26b314702d1f1cb9ee4.jpeg))



然后是个人理解：git作为版本控制软件中最受欢迎的一个，它不仅有本地仓库，也可以链接远程仓库远程仓库，还有暂存区和工作区。用户可以将如gethup这种网站上面的项目clone到自己的工作区，然后在自己的电脑上面进行文件操作，之后可以用add 将文件添加到暂存区，如果文件需要进一步提交，可以用commit 提交到本地仓库，之后也可以利用push 将文件推送到远程仓库中。而每一次修改文件，git 都会对当前文件做一次”备份“（但是没有完全备份）操作



安装完git 后的git bush 操作的窗口其实是一种linux命令（操作系统还没学），利用一些简单代码，就可以进行操作了。



## 3.个人实操

### 1.初始化

git config --global user.name"xxxxxx"

git config --global user.emile"xxxx@xxxx"

### 2.个人实操

![]()

首先创建一个文件夹，在文件夹里面使用git bush 可以打开操作窗，输入 git init，文件夹中新建了一个名为.git 的文件夹，这个文件夹应该就包含了版本管理的各种文件，应该也就是本地仓库。版本的提交有add  和commit   ，格式为，git add .    git commit -m"这里是版本修该描述“，等价于readme ";此外，还可以单独提交，git add 后面跟要提交的文件。add 操作是将代码加入暂存区，commit则是将暂存区的代码加入本地仓库。git log 可以查看历史提交记录

 git commit -m"这里是版本修该描述"简化版本，不用写VIM版本日志



单词释义：config 配置    -- global  全局  log 日志

重点注意：**这个玩意每一个空格都不能错**

接下来就是本地和远程的联系实操。

git remote add origin 仓库地址告诉git 上传到哪个仓库，然后上传到网盘，输入密码即可。



以上是GIT的简单学习，关于GIT的许多命令都是跟操作系统有关，所以我准备在空闲时了解操作系统的基本知识，再深入学习GIT其他文件操作。 





