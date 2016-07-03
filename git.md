
1. 切换到master分支
git checkout master
2. 更新master代码
git pull --ff-only upstream master
3. 创建新的分支，并在新的分支上进行开发
git checkout -b "newbranch"
4. 开发完成后，将修改的文件加入到github
git add file
5. 提交修改的文件
git commit -m “注释”
6. 将正在开发的分支提交到远端代码库
git push origin newbranch
7. 在github上发起pull request
分支合并后在本地执行第2步


1. 从发生冲突的分支(如:modifypwd)切换到本地master分支
git checkout master
2. 从主版本pull最新代码
git pull --ff-only upstream master
3. 切换到发生冲突的分支
git checkout modifypwd
4. rebase，提示发生conflict的文件
git rebase master
5. 修改文件冲突的文件
vim file
6. 对比修改后的文件(可以忽略)
git diff file
7. 加入文件到索引
git add file
8. 继续rebase
git rebase --continue
9. 如何提示还有冲突的文件则跳转到第5步执行强制push当前分支
git push origin modifypwd -f


Pull request流程

git checkout -b fanwangwang-master master
git pull https://github.com/fanwangwang/fem.git master
git checkout master
git merge --no-ff fanwangwang-master
git push origin master

共享版本流程

http://www.worldhello.net/gotgithub/04-work-with-others/020-shared-repo.html

版本控制是一种记录一个或若干文件内容变化，以便将来查阅特定版本修订情况的系统

* 直接记录快照，而非差异比较
* 所有的操作都是本地执行
* Git保持完整性
* 以文件哈希值索引，而不是文件名
* Git 一般只添加数据





