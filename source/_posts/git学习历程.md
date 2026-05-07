---
title: 4.26学习历程
date: 2026-04-26 17:35:40
tags: 学习 
cover: /images/scenery4.png
---

# 今日知识点汇总：
## 1. 重新熟悉在vscode上拉(clone/pull)推(push)代码：
先clone或者pull到本地/工作区代码进行更改后add加commit到本地仓库，若有其他人在远程仓库（github）上进行更改的话，工作区pull代码会产生冲突，之后解决冲突
## 2. 了解了branch的用法：
在 ` clone/pull ` 代码之后，一般来说会新建一个分支进行编写代码，编写完代码之后使用 ` git add,commit ` ,之后切换到主分支：` git switch/checkout [文件名] ` ,若这段代码在编写期间别人在远程仓库进行了更改，最好先进行 ` git pull ` 操作，若有冲突，先解决冲突，之后进行新建分支和主分支的合并: ` git merge [新建分支名] ` ,最后确认无误可以push提交
## 3. git checkout代码
` git checkout ` 可以用来切换分支，也可以将暂存区的文件恢复到工作区。若 ` git checkout [文件名]  ` ，那么这个命令就是将暂存区的文件覆盖工作区，若 ` git checkout [branch] ` ，那就是切换分支，也可用 ` git switch [branch] ` 来切换分支 ，而切换分支的前提是要把这个分支 ` commit ` 到本地仓库。
## 4. 模拟每天工作日常
早上到岗：git pull
       ↓
切换分支：git checkout -b feature-login
       ↓
写代码、改文件
       ↓
查看状态：git status
       ↓
暂存修改：git add .
       ↓
提交到本地：git commit -m "完成登录框样式"
       ↓
继续工作，重复 写代码 → add → commit
       ↓
下午完成功能：git checkout main
       ↓
拉取最新代码：git pull
       ↓
合并分支：git merge feature-login
       ↓
推送成果：git push
## 5.git remote
` git remote -v ` 检查远程仓库 ，` git remote show origin ` 显示远程仓库的信息

## 6. tips:
一般来说只有增，删，改过的代码或文件才可以进行add,commit等操作