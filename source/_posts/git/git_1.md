---
title: git初探(一)-git基本原理
date: 2020-03-16 10:18:00
tags: 
- git
---

### 1.仓库

仓库分为工作区 暂存区 提交区。   

- 文件夹即是工作区。  
- 使用 `git add` 命令添加文件到暂存区（stage）。  
- 使用 `git commit` 添加文件到版本库？（commit .git文件夹中的快照信息）。
- `git status` 可以查看被commit的文件（工作区和暂存区的状态）
- `git status -s` 文件状态的简写（M - 修改， A - 添加， D - 删除， R - 重命名，?? - 未追踪）。

![git仓库](/git_2/1.png)


- modified: 修改
- tracked: 跟踪