1.git add 文件名.txt（添加文件到暂存区）
2.git commit -m "注释"（提交文件到仓库）
3.git status(查看文件状况)
  3.1git diff 文件名.txt(查看文件修改部分)
4.cat 文件名.txt(查看文件内容)
当文件修改过后重复1，2步骤，同时在提交之前使用3检查
4.git log(查看版本记录)~只能查看到现在版本，不能查看回退前的
6.git reflog(查看版本号)~能查看所有的
5.版本回退
   5.1 git reset --hard HEAD^（回退一个版本）HEAD^^(回退两个版本)
   5.2 git reset --hard HEAD~N(回退N个版本)
   5.3 git reset --hard 版本号（回到指定版本） 