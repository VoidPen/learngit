# Learn Git

----

## 一. Git简介

----

## 二. 常用命令

### 配置

```Bash
# 列出当前所有配置
$ git config --list
# 列出当前Repository配置(文件路径: <repo>/.git/config)
$ git config --local --list
# 列出全局配置(文件路径: ~/.gitconfig)
$ git config --global --list
# 列出系统配置(文件路径: /etc/gitconfig)
$ git config --system --list

# 设置全局用户名和邮箱
$ git config --global user.name "firstname lastname"
$ git config --global user.email "email"
```

### 创建仓库

```Bash
# 创建一个新的本地仓库
$ git init

# 通过 SSH 复制一个已创建的仓库
$ git clone ssh://user@domain.com/repo.git

# 通过 HTTPS 复制一个已创建的仓库
$ git clone https://domain.com/user/repo.git
```

### 本地修改

##### 显示当前状态

```Bash
# 显示状态
$ git status
```

##### 显示改变

```Bash
# 显示变化
$ git diff
```

##### 添加到暂存区

```Bash
# 把当前所有修改添加到暂存区
$ git add .
$ git add <file>
```

##### 提交修改到仓库

```Bash
# 修改上次提交
$ git commit --amend
```

##### 显示日志

```Bash
# 显示日志
$ git log
$ git log --oneline
$ git log --pretty=oneline
```

##### 撤销

```Bash
# 放弃工作目录下的所有修改
$ git reset --hard HEAD
# 将HEAD重置到上一次提交的版本(HEAD^^: 上上次)
$ git reset --hard HEAD^
$ git reset --hard HEAD~n
$ git reset --hard <commit_hash>
# 将HEAD重置到指定的引用的版本(n由git reflog确定)
$ git reset --hard HEAD@{n}
```

##### 管理reflog

```Bash
# 默认显示历史引用记录
$ git reflog
```

##### 管理分支

```Bash
# 创建分支并切换分支dev
$ git checkout -b dev
$ git branch dev
$ git checkout dev
# 查看当前分支
$ git branch
# 合并分支
$ git merge dev
# 删除分支
$ git branch -b dev
$ git branch --




