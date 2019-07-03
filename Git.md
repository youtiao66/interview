# Git

## git log
**以图表和单行的形式展示所有提交日志** `git log --graph --oneline --all`

## 统计
**指定作者的提交次数** `git log --author=username --oneline | wc -l`

**指定作者的代码量**
```
  git log --author=username --pretty=tformat: --numstat | awk '{ add += $1; subs += $2; loc += $1 - $2 } END { printf "added lines: %s, removed lines: %s, total lines: %s\n", add, subs, loc }'
```
