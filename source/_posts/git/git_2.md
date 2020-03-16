---
title: git初探(二)-推送已有代码到远程仓库
date: 2020-03-12 14:18:00
updated: 2020-03-16 11:18:00
tags: 
- git
---

推送已有项目代码到远程仓库。

### 1.初始化仓库
```bash
//初始化
git init
//所有文件(.)添加到暂存区
git add .
//添加到版本库,形成快照
git commit -m "init project"
git status
```
<!-- more -->
现在使用`git push origin master `push到远程仓库上,会报如下错误,显示你并没有指定对应的远程仓库。
```bash
 fatal: 'origin' does not appear to be a git repository
 fatal: Could not read from remote repository.
 Please make sure you have the correct access rights
 and the repository exists.
```
### 2.GitHub上创建项目并在本地提交项目
在github（gitee/gitlab）上创建新项目，并且拿到对应的空项目的https（http）/ssh路径。  

例如我创建了`git@github.com:loyalvi/hexo.git`这个项目。

```
git remote add origin git@github.com:loyalvi/hexo.git
git push origin master
```
成功提交
```
Enumerating objects: 119, done.
Counting objects: 100% (119/119), done.
Delta compression using up to 8 threads
Compressing objects: 100% (110/110), done.
Writing objects: 100% (119/119), 555.08 KiB | 2.19 MiB/s, done.
Total 119 (delta 0), reused 0 (delta 0)
To github.com:loyalvi/hexo.git
 * [new branch]      master -> master
```