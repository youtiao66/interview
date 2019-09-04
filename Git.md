# Git

## git log
**以图表和单行的形式展示所有提交日志** `git log --graph --oneline --all`

## git rebase
### 合并多个commit为一个完整commit
`git rebase -i  [startpoint]  [endpoint]`

- `-i`即`--interactive`，即弹出交互式的界面让用户编辑完成合并操作
- `[startpoint] [endpoint]`则指定了一个编辑区间，如果不指定`[endpoint]`，则该区间的终点默认是当前分支`HEAD`所指向的commit（注：该区间指定的是一个前开后闭的区间）

## git update-index
**假定指定的文件为未更改的状态** `git update-index [--[no-]assume-unchanged] [--] [<file>...]`

**查看被假定为未更改状态的文件** `git ls-files -v`

## 统计
**指定作者的提交次数** `git log --author=username --oneline | wc -l`

**指定作者的代码量**
```
  git log --author=username --pretty=tformat: --numstat | awk '{ add += $1; subs += $2; loc += $1 - $2 } END { printf "added lines: %s, removed lines: %s, total lines: %s\n", add, subs, loc }'
```
