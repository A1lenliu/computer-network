1.前期工作
 cd 磁盘名:或 文件名（指定目录）
 eg. cd O:
     cd mygit1
 pwd（查看当前目录）
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
 git checkout --文件名.txt(撤销在工作区的工作，在add语句执行之前的工作)
5.

