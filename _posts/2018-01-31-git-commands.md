---
layout: post
title:  "Git Bash版本控制管理"
date:   2018-01-31 16:04:00
categories: git
tags: git 版本控制
share: true
---

* content
{:toc}


Git Bash版本控制管理


![](https://git-scm.com/images/logos/1color-darkbg@2x.png)





## Git Bash版本控制管理

工作中用到哪个忘记了就随时添加

> [廖雪峰的git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

### git init

### git status

### git add

### git reset

### git commit

   #### git commit -a 
   
 可以快速提交本地所有修改过的文件
 
 #### git commit -m "msg"
  
  提交修改和修改描述

### git branch
  显示本地所有的分支
  
  #### git branch -a 
 显示本地和远程仓库所有的分支
 
 #### git branch dev
 创建`dev`分支
    
 #### git branch -d dev
 删除`dev`分支
 
### git checkout

 #### git checkout dev
 切换到dev分支
 
 #### git checkout -b dev
 创建并且切换到dev分支

### git merge
   #### git merge dev
   在`master`分支使用时会把`dev`分支合并到`master`分支

### git stash

   保存当前的工作进度。会分别对暂存区和工作区的状态进行保存。
   
   #### git stash pop `[--index]` `[<stash>]`
   
   如果不使用任何参数，会恢复最新保存的工作进度，并将恢复的工作进度从存储的工作并进度列表中清除。
   
   如果提供`<stash>`参数（来自`git stash list`显示的列表），则从该`<stash>`中恢复。恢复完毕也将从进度列表中删除`<stash>`。
   
   选项`--index`除了恢复工作区的文件外，还尝试恢复暂存区。开始恢复进度的时候显示的状态和保存进度前的略有不同。
   
   #### git stash list
   
   显示进度列表。此命令显然暗示了git stash 可以多次保存工作进度，并用在恢复时候选择。
   
   #### git stash drop `[<stash>]`
   
   删除一个存储的进度。默认删除最新的进度。
   
   #### git stash clear
   
   删除所有存储的进度。
   
   #### git stash branch `<branchname>` `<stash>`

   基于进度创建分支。

### git log

### git push 

把本地仓库的更新推到服务器仓库

  #### git push origin dev:dev
提交本地dev分支作为远程的dev分支

  #### git push origin :dev 
  删除远程dev分支

### git pull

### git update-index

   #### git update-index --assume-unchanged xxxx.md
   
   暂时忽略`xxxx.md`文件中的更改，不去跟踪它的修改
   
   #### git update-index --no-assume-unchanged xxxx.md
   
   取消暂时忽略`xxxx.md`文件中的更改，再次跟踪它的修改
   

