# GIT版本控制系统

> 版本控制系统：
> 1.记录历史版本信息（记录每一次修改的记录）
> 2.方便团队相互之间协作的开发
### 常用的版本控制系统
- cvs/svn：集中式版本控制系统
- git：分布式版本控制系统
 1.GIT工作原理
+ 工作区：我们能看到的，并且用来写代码
+ 暂存区：临时存储用的
+ 历史区：生成历史版本
  工作区——>暂存区——>历史区
  1.GIT的全局配置
> 第一次安装后，我们在全局环境下配置基本信息
```
$ git config --global -l   查看全局配置信息
$ git config -l   查看配置信息
配置全局信息 用户名和邮箱
$ git config --global user.name 'xxx'
$ git config --global user.eamil 'xxx@xx.xxx'
```
2.创建仓库完成版本控制
> 创建本地仓库git 
```
$ git init  创建仓库
//=>会生成一个隐藏文件夹“ .git”（这个文件夹不能删除，因为暂存区和离市区还有一些其他文件信息都在这里，删除以后就不是一个完整的git仓库
$ pwd 查看定位
```
> 在本地编写完代码后（再工作区），把一些文件提交到暂存区
```
$ git add xxx 把某一个文件或者文件夹提交到暂存区
$ git add .   把当前仓库中所有最新修改的文件都提交到暂存区
$ git add -A
$ git status 查看当前文件的状态（红色代表在工作区，绿色代表在暂存区，看不见东西证明所有修改的信息都已经提交到历史区）
$ git diff xxx   查看文件修改处
cat xxx  快速查看文件内容
$ git reflog 记录操作命令
```
> 把暂存区内容提交到历史区
```
$ git commit -m'描述信息：本次提交内容的一个描述信息'
查看历史版本信息
$ git log
$ git log --pretty=oneline  版本信息一行显示
```

```
$ git reset --hard head^ 返回上一个版本
$ git reset --hard head~num 返回num版之前
$ git reset --hard 版本id（6位最合适）
$ git restore xxx 撤销修改
$ git checkout -- xxx 撤销修改
$ git checkout head 文件完全名   从暂存区直接撤销修改
$ git restore --staged xxx  从暂存区撤回工作区
rm xxx  删除某文件
$ git rm xxx 某文件在工作区删除也提交到暂存区
```

2.把本地信息提交到远程仓库

```
//建立连接
查看本地仓库和那些远程仓库保持连接
cd ~/ssh  在本地仓库查看SSH KEY
创建SSH KEY:ssh-keygen -t rsa -C "邮件地址"

$ git push -u 仓库名 要推送的分支名
$ git remote -v
让本地仓库和远程仓库穿件一个新的链接，origin是随意取的一个链接名（可以改成自己想要的）
$ git remote add origin [GIT仓库地址]
$ git remote add origin git@github.com:github账户/远程仓库名
删除相关联信息
$ git remote rm origin
```

```
提交前最好先拉取
$ git pull origin master
把本地代码提交到远程仓库（需要输入GitHub用户密码）
$ git push origin master

```

### 分支：

```
创建分支：$ git branch 分支名
切换分支：$ git switch 分支名（=git checkout 分支名）
创建并切换分支：git switch -c 分支名（git checkout -b 分支名）
查看所有分支：git branch (带*为当前操作的分支)
合并分支：
1.快速合并（合并删除分支后会丢掉分支信息）：git merge 要合并的分支名
2.非快速（合并删除分之后保留分支信息） ：git merge --bo-ff -m"说明" 要合并的分支名
删除分支：
1.git branch -d 删除分支
2.git branch -D 强制删除分支     

```


```
$ git clone [远程仓库git地址] [别名：可以不设置。默认仓库名]
/*
   真实项目开发流程：
      1.组长或负责人先建立中央仓库
      2.小组成员基于：$ git clone 把远程仓库及默认的内容克隆到本地一份（解决了三个事情：初始化一个本地仓库 git init 、和对应的远程仓库保持关联 git remote add 、吧远程仓库默认内容拉取到本地 git pull
      3.每个小组成员写完自己的程序后，基于 git add /git commit'' 把自己修改的内容放到历史区，然后 git pull/ git push 把本地信息和远程仓库信息同步即可（可能涉及冲突的处理）
*/
```

### 标签

```
git tag 标签（默认标签是打在最新提交commit上的）
git tag 标签名 commit：给指定的提交打标签
git tag -a 标签名 -m"说明" commit：打标签的同时附上说明
git tag 查看所有标签
git show 标签名  查看标签说明
git tag -d 标签名  删除本地标签
git push origin ：refs/tags/标签名
git push origin 标签名： 将单个标签推送到远程仓库
git push origin --tags ：推送全部尚未推送到远程的本地标签
git config --global alias 自定义命令  原命令
```



### GIT和GIT-HUB

> GIT和GIT-HUB：https://www.github.com
>
> 一个网站（一个开源的源代码管理平台），用户注册后，可以在自己账户下创建仓库，用来管理项目的源代码（源代码基于git传到仓库中）
>
> 我们所熟知的插件、类库、框架等都是在这个平台上有托管，我们可以下载观看和研究研究源码等

1.Settings 用户设置

+ Profile 修改个人信息
+ Account 修改用户名
+ Security 修改密码
+ Emails 邮箱

2.创建仓库

new repository ->填写信息 ->Creat repository 

- public 公共仓库作为开源的项目
- private 私有仓库作为内部团队协作管理项目

Settings   ->删除仓库Delete this repository 

​               ->Collaborators 设置协作开发者

Code 可以查看历史版本信息和分支信息