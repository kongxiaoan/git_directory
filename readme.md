我是学习git的文件
===

- git commit -m "提交说明"
- git status : 查看当前仓库状态
- git diff :查看文件改动
- git log : 查看文件提交记录 --pretty=oneline添加后会当行显示
- git reset --hard HEAD^  
> git版本回退非常快的原因是内部有个指向当前位置的指针 当回退的时候仅仅是将指针指向了上一个版本
- git reflog 用来记录每一次提交的命令

Git和其他版本控制系统如SVN的一个不同之处就是有暂存区的概念。
---

- 工作区：就是你在电脑里能看到的目录
- 版本库：工作区有一个隐藏的目录.git 就是版本库
> Git的版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的暂存区，还有Git为我们自动创建的第一个分支master，以及指向master的一个指针叫HEAD

- git checkout -- 文件名 ：丢弃工作区的修改
- git rm file 删除仓库中的文件

远程仓库
===

> 由于你的本地Git仓库和GitHub仓库之间的传输是通过SSH加密的，所以，需要一点设置：

第1步：创建SSH Key。在用户主目录下，看看有没有.ssh目录，如果有，再看看这个目录下有没有id_rsa和id_rsa.pub这两个文件，如果已经有了，可直接跳到下一步。如果没有，打开Shell（Windows下打开Git Bash），创建SSH Key：

1. 创建SSH key
```
$ ssh-keygen -t rsa -C "youremail@example.com"

```
2. 登录GitHub 打开settings ssh 页面添加或者新建SSH key


```
$ git remote add origin git@github.com:michaelliao/learngit.git
git push -u origin master 第一次推送master分支的所有内容

```
> origin 就是远程仓库的名字  

- git clone 地址 克隆远端的仓库

分支的创建与合并
===

- git checkout -b dev 常见并切换一个分支dev
相当于
- git branch dev git checkout dev

- git branch 查看当前分支
 


