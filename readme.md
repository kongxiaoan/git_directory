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

