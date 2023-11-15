1.前期工作
 cd 磁盘名:或 文件名（指定目录）
 eg. cd O:
     cd mygit1
 mkdir 版本库名（创建版本库）
 pwd（查看当前目录）
 git init(将此库变成能被git管理的仓库)
2.提交文件
 git add 文件名.txt（添加文件到暂存区）
 git commit -m "注释"（提交文件到仓库）
 git status(查看文件状况)
   git diff 文件名.txt(查看文件修改部分)
 cat 文件名.txt(查看文件内容)
 当文件修改过后重复1，2步骤，同时在提交之前使用3检查
3.版本管理
 git log(查看版本记录)~只能查看到现在版本，不能查看回退前的
 git reflog(查看版本号)~能查看所有的
 版本回退
    git reset --hard HEAD^（回退一个版本）HEAD^^(回退两个版本)
    git reset --hard HEAD~N(回退N个版本)
    git reset --hard 版本号（回到指定版本） 
4.撤销修改
 git checkout -- 文件名.txt(撤销在工作区的工作，在add语句执行之前的工作)
 ”--“很重要，而且后面需要跟文件名时要加空格，否则无法识别
5.删除文件
 rm 文件名.txt
 git checkout -- 文件名.txt(此语句也可以用来回复删除的文件，在commit语句之前)
6.链接github
 只要本地作了提交，就可以通过如下命令
  git push -u origin master/main（代表分支名字）
 把本地master分支的最新修改推送到github上了
 由于远程库是空的，我们第一次推送master分支时，加上了 –u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令
后面推送可以使用 git push
 注意：当远程仓库名改变后需要用
 git remote set-url origin 仓库URL
 可以用git remote -v检查目前所关联的远程仓库名
7.从远程库克隆
 git clone github地址
 克隆前注意现在所处目录，用pwd语句
8.创建并合并分支
 每次提交，Git都把它们串成一条时间线，这条时间线就是一个分支。截止到目前，只有一条时间线，在Git里，这个分支叫主分支，即master分支。HEAD严格来说不是指向提交，而是指向master，master才是指向提交的，所以，HEAD指向的就是当前分支。
 git checkout -b dev(创建并切换分支)
= git branch dev 和 git checkout dev
 git branch(查看分支，会列出所有的分支，当前分支前面会添加一个星号)
  git merge dev(用于合并指定分支到当前分支上) 
 git branch -d dev(删除dev分支)
9.多人远程协同