### 基本概念

| 英文 | 中文 |
| --- | --- |
| working tree | 工作区 |
| stage/index | 暂存区 |

### git-clean

> Remove untracked files from the working tree

从工作区中删除未跟踪的文件

`git clean [-d] [-f]`

#### -d

递归地删除目录和目录下包含的所有目录和文件

#### -f, --force

如果不添加该选项，`git clean`会没有删除文件和目录的权限



### git-revert

> Revert some existing commits

撤销已经存在的提交

**通过创建新的提交，去撤销已经存在的提交**

#### `git revert <commit>`

撤销一个已经存在的提交

#### `git revert <start-commit>..<end-commit>`

撤销指定区间的提交，**前开后闭，不包括`<start-commit>`，包括`<end-commit>`**

#### -n, --no-commit

不创建新的提交，直接把撤销后的代码添加到工作区和暂存区
