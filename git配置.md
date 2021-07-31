# 1.配置用户名和邮箱
```
	git config --global user.name "chenwj"
	git config --global user.email "66969721@qq.com"
```

## 2. 公钥设置
公钥设置，是通过ssh与远程系统的凭证
linux 或者git bash钥生成步骤：
cd ~/.ssh 没有则创建
执行：ssh-keygen -t rsa -C "你的邮箱@xxx.com" 三次回车按钮

把公钥提交到git或者gitee上去

复制工程中ssh选项
git@gitee.com:dongquxiang/dqx-cloud.git 
使用命令
git clone git@gitee.com:xxx/xxxx.git 

至此，在项目中可以使用公钥进行通讯了。


# 简易的命令行入门教程:
```
Git 全局设置:

git config --global user.name "陈炜经"
git config --global user.email "66969721@qq.com"
创建 git 仓库:

mkdir layui_test
cd layui_test
git init
touch README.md
git add README.md
git commit -m "first commit"
git remote add origin git@gitee.com:chen_wei_jing/layui_test.git
git push -u origin master
已有仓库?

cd existing_git_repo
git remote add origin git@gitee.com:chen_wei_jing/layui_test.git
git push -u origin master




1.git基本指令

git init —— 新建git仓库

git add 文件/文件夹 —— 将文件添加到缓存区中

git add -A — 添加所有内容到缓存区中

git stutas ——— 查看git状态

git commit -m ‘提交信息’ —— 将缓存区中的内容全部提交到git本地仓库中

git log ——- 查看提交日志

git reset -- hard HEAD —— 让工作目录中的内容和仓库中的内容保持一致

git reset --hard HEAD^ —— 回到上一个版本

git reset --hard 版本号 —— 回到指定的版本

git checkout - - 文件名 —— 从暂存区中恢复工作目录中的内容(让工作区中的指定文件，回到上次提交的时候的状态)

git clone - 将服务器上的项目(仓库)克隆 (使用https地址需要输入密码，使用ssh地址需要添加公钥)

git remote add origin 地址 ----- 关联远程仓库(只需要关联一次)
git push [-u] origin master ----- 提交(-u在第一次提交分之的时候才用)
```
# 1.查看所有分支
> git branch -a
　　
# 2.查看当前使用分支(结果列表中前面标*号的表示当前使用分支)
> git branch
 
# 3.切换分支
> git checkout 分支名
————————————————
版权声明：本文为CSDN博主「wang_yq123」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/qq_44490008/article/details/88594059
