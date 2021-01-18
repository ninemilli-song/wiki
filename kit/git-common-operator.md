# GIT 常用操作

## 修改用户名

提交之后才发现**用户** / **邮箱**不正确，需要修改为正确的**用户** / **邮箱**

```bash
git rebase -i HEAD~1

git commit --amend --author "songxg <songxg@chanjet.com>"

git rebase --continue
```

## git四连

```
git add .                                将所有改动放进暂存区
git commit -m "描述"                     提交并附带概要信息
git pull                                 从远程仓库拉去代码
git push                                 推送代码到远程仓库（master分支）
```

## 其余常用命令

```
# 查看日志
git log

# 查看详细历史
git log -p  

# 查看简要统计
git log --stat

# 查看工作区状态
git status  

# 创建分支
git branch 名称 

# 切换分支
git checkout 名称  

# 创建并切换到新分支
git checkout -b 名称 

# 创建并跟踪远程分支
git checkout -t <branch-name>

# 删除该分支（不能删除当前所在的分支，不能删除没有合并到master上的分支）
git branch -d 名称 

# 删除该分支（可以删除没有合并到master上的分支）
git branch -D 名称 

# 对最新的一条commit进行修正
git commit --amend 

# 丢弃最新提交（未提交的内容会被擦掉）
> git reset --hard HEAD^ 

# 丢弃最新提交（未提交的内容不会被擦掉）
git reset --soft HEAD^ 

# 回到某个commit
git revert HEAD^ 

# 重新设置基础点
git rebase 目标基础点

# 将分支合并到head指向的分支
git merge 名称 

# 将代码推送到远程仓库的指定分支
git push origin localbranch 

# 删除远程分支
git push -d origin branchName 

# 暂存代码
git stash 

# 弹出暂存代码
git stash pop 
```