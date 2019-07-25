# Git

## git log
**以图表和单行的形式展示所有提交日志** `git log --graph --oneline --all`

## git update-index
**假定指定的文件为未更改的状态** `git update-index [--[no-]assume-unchanged] [--] [<file>...]`

**查看被假定为未更改状态的文件** `git ls-files -v`

## 统计
**指定作者的提交次数** `git log --author=username --oneline | wc -l`

**指定作者的代码量**
```
  git log --author=username --pretty=tformat: --numstat | awk '{ add += $1; subs += $2; loc += $1 - $2 } END { printf "added lines: %s, removed lines: %s, total lines: %s\n", add, subs, loc }'
```
