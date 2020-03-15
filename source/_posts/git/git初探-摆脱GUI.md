---
title: git初探-摆脱GUI
date: 2020-03-12 14:18:00
tags: 
- git
---

## git初探-尝试摆脱GUI

初始化仓库，推送已有代码到远程仓库（ssh）
```bash
//初始化
git init
//
git add .
//添加到 形成快照
git commit -m "init project"
git status
```

`git push origin master `

```bash
 fatal: 'origin' does not appear to be a git repository
 fatal: Could not read from remote repository.
 Please make sure you have the correct access rights
 and the repository exists.
```
在github上创建项目并且拿到对应的空项目的https/ssh路径
git@github.com:loyalvi/hexo.git

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