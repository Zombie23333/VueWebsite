---
title: 如何使用GIT
date: 2024-09-22 08:42:23
tags:
---
1. 确保目录中存在.git文件
2. git branch 查看分支

### 如何将本地代码上传

1. git add . 添加所有更改的文件到暂存区
2. git commit -m "提交信息" 提交更改
3. git push origin 分支名 将本地分支推送到远程仓库

注意：如果是第一次推送该分支到远程，可能需要使用 git push -u origin 分支名 来设置上游分支。

### 如何指定新的远程仓库

1. 使用 git remote add 命令添加新的远程仓库：git remote add [远程仓库名] [URL]
2. 例如：git remote add origin https://github.com/username/repo.git
3. 查看当前远程仓库：git remote -v
4. 如果要更改现有远程仓库的URL，使用 git remote set-url 命令：git remote set-url origin [新URL]

注意：更改远程仓库后，确保你有相应的权限来推送和拉取代码。