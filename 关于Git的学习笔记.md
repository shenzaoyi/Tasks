

## 关于Git的学习笔记

### 1.专业术语

Git 是一款免费、开源的分布式版本控制系统，也是当今最为流行的版本控制系统之一，在众多的项目开发中普遍使用。其特点是版本控制，以及版本回溯 。

## 2.git的运作流程

首先来一张专业的图（网上找的 :smile:）

![]([v2-49c265e6c878e26b314702d1f1cb9ee4.jpeg (666×242) (raw.githubusercontent.com)](https://raw.githubusercontent.com/shenzaoyi/picture/main/v2-49c265e6c878e26b314702d1f1cb9ee4.jpeg))



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





