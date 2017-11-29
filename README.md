# git_practice
目的为了练习git命令行命令
#git 常用的命令

#git 远程仓库相关命令
1.检出  git clone  "地址"
2.查看一个本地仓库的远程仓库是什么  git remote -v
3.为本地仓库添加远程仓库地址：  git remote add [origin]  "123.git"  -->这里的name是随便取的，可以添加多个远程地址，
  push或者pull的时候根据这里的name去区分远程仓库
4.删除一个远程仓库  git remote rm [origin]
5.修改一个远程仓库的URL  git remote ste-url [origin] [456.git]
6.拉取远程仓库： git pull [origin] [master(本地的)]  -->(声明拉取的是哪个远程的哪个分支)
7.推送到远程仓库  git push [origin] [master(本地的)]
8.如果拉取或者推送的本地分支在远程上没有对应，你要把本地的test分支的东西push到远程的master分支  git push [origin] test:master

#git 分支的相关操作
1.查看本地分支  git branch
2.查看远程存在的分支  git branch -a
3.查看本地所有的分支  git branch -r
4.创建一个本地分支  git branch [name]  -->(创建后并不会切换到新创建的分支)
5.切换到某个分支  git checkout [name]
6.创建一个分支，并且立刻切换到这个分支  git checkout -b [name]
7.删除一个分支  git branch -d [name]
8.合并一个分支 git merge [name]
9.将本地分支提交到远程 git push origin [name]
10.删除远程分支  git push origin :[name]->(等于将空的分支推到远程，所以需要先删除本地对应的分支)
11.拉取远程的所有分支  git fetch
12.放弃本地变更 git checkout .

#git 如何diff代码？
git diff(文件路径)：进入vi编辑，下拉箭头可查看所有改动

#tag的相关操作
1.查看所有tag git tag
2.创建新的tag git tag -a [1.1.1] -m "这是分支的注释"
3.查看一个tag的信息(包括注视)  git tag -v 1.1.1
4.回滚到某个tag git reset --hard 1.1.1
5.tag创建就在本地代码仓库了，删除有 git tag -d 1.1.1 提交 git push origin  --tags

