# Learn Git

----
## 一. Git简介

----
## 二. 常用命令

### 配置
```
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
```
# 创建一个新的本地仓库
$ git init

# 通过 SSH 复制一个已创建的仓库
$ git clone ssh://user@domain.com/repo.git

# 通过 HTTPS 复制一个已创建的仓库
$ git clone https://domain.com/user/repo.git
```

### 本地修改

##### 显示当前状态
```
$ git status
```

##### 显示改变
```
$ git diff
```

##### 添加到暂存区
```
# 把当前所有修改添加到暂存区
$ git add .
$ git add <file>
```

##### 提交修改到仓库
```
# 修改上次提交
$ git commit --amend
```

##### 显示日志
```
$ git log
$ git log --oneline
$ git log --pretty=oneline
```

##### 撤销
```
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
```
# 默认显示历史引用记录
$ git reflog
```