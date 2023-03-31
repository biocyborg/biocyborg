---
title: Git 使用介绍
---

## Git 简介

Git 是一个分布式版本控制系统，是由 Linux 之父 Linus Torvalds 开发的。它可以帮助开发者更好的管理代码的版本，协同开发，以及方便地回溯代码。

## Git 安装

在 Windows 上安装 Git，可以从 Git 官网下载安装程序进行安装。

## Git 常用命令

### 初始化仓库

在当前目录下初始化一个 Git 仓库：

```bash
git init
```

### GIT 配置

#### 全局配置

查看全局配置：

```bash
git config --global user.name
```

```bash
git config --global user.email
```

设置全局配置：

```bash
git config --global user.name 'you name'
```

```bash
git config --global user.email 'you email'
```

#### 局部配置

查看局部配置：

```bash
git config user.name
```

```bash
git config user.email
```

设置局部配置：

```bash
git config user.name 'you name'
```

```bash
git config user.email 'you email'
```

### 添加文件到暂存区

添加一个文件到暂存区：

```bash
git add filename
```

添加所有文件到暂存区：

```bash
git add .
```

### 链接远程分支

将本地分支链接到远程分支：

```bash
git remote add origin remote-url
```

### 查看仓库状态

查看当前仓库的状态：

```bash
git status
```

### 查看提交历史

查看提交历史：

```bash
git log
```

### 拉取代码

从远程仓库拉取代码：

```bash
git pull origin branch-name
```

### 推送代码

推送代码到远程仓库：

```bash
git push origin branch-name
```

### 创建分支

创建一个新的分支：

```bash
git branch branch-name
```

### 切换分支

切换到指定的分支：

```bash
git checkout branch-name
```

### 合并分支

将指定分支合并到当前正在使用的分支：

```bash
git merge branch-name
```

### 删除分支

删除指定分支：

```bash
git branch -d branch-name
```

删除本地仓库中已经不存在的远程分支：

```bash
git remote prune origin
```

清除本地仓库中已经合并到 master 分支的分支：

```bash
git branch --merged master | grep -v '^\* master$' | xargs git branch -d
```

删除当前分支外的所有本地分支：

```bash
git branch | grep -v "^\* " | xargs git branch -D
```

### Git 指令回退到上一个版本

回退到上一个版本：

```bash
git reset HEAD~1
```

## 总结

以上是 Git 的一些常用命令和其他命令，当然 Git 还有很多其他的功能和命令，需要开发者自己去学习和掌握。Git 帮助开发者更好地管理代码，协同开发，以及方便地回溯代码，是一个非常重要的工具。
