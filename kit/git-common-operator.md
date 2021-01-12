# GIT 常用操作

## 修改用户名

提交之后才发现**用户** / **邮箱**不正确，需要修改为正确的**用户** / **邮箱**

```bash
git rebase -i HEAD~1

git commit --amend --author "songxg <songxg@chanjet.com>"

git rebase --continue
```