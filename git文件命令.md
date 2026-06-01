以下是Git的常用命令分类整理，涵盖日常开发的核心操作：

## **仓库初始化与克隆**
bash
git init              # 初始化本地仓库
git clone <URL>       # 克隆远程仓库


## **基础操作**
bash
git status            # 查看工作区状态
git add <file>        # 添加文件到暂存区
git add .             # 添加所有变更文件
git commit -m "msg"   # 提交暂存区内容
git commit -am "msg"  # 跳过暂存直接提交所有跟踪文件


git add README.md

git remote add origin https://github.com/clarkyqp/README.git
git remote set-url origin https://github.com/clarkyqp/README.git

git push -u origin main
git remote -v


git config --global http.proxy http://127.0.0.1:7890
git config --global https.proxy http://127.0.0.1:7890  #代理设置


## **分支管理**
bash
git branch            # 列出本地分支
git branch <name>     # 创建分支
git checkout <name>   # 切换分支
git checkout -b <name> # 创建并切换分支
git merge <branch>    # 合并分支到当前分支
git branch -d <name>  # 删除分支


## **远程操作**
bash
git remote -v         # 查看远程仓库
git fetch             # 拉取远程更新但不合并
git pull              # 拉取并合并远程分支
git push              # 推送到远程仓库
git push -u origin <branch> # 推送并设置上游


## **查看历史**
bash
git log               # 查看提交历史
git log --oneline     # 简洁格式
git log --graph       # 图形化显示
git diff              # 查看工作区与暂存区的差异
git diff HEAD         # 与最新提交的差异


## **撤销与重置**
bash
git restore <file>    # 撤销工作区修改
git restore --staged <file> # 撤销暂存
git reset HEAD^       # 撤销上一次提交（保留修改）
git reset --hard HEAD # 重置到最新提交（丢弃修改）
git reset --hard <commit> # 回退到指定提交


## **标签管理**
bash
git tag               # 列出所有标签
git tag <name>        # 创建轻量标签
git tag -a <name> -m "msg" # 创建附注标签
git push origin --tags # 推送所有标签


## **暂存与清理**
bash
git stash             # 暂存当前修改
git stash pop         # 恢复暂存并删除记录
git stash list        # 查看暂存列表
git clean -fd         # 清理未跟踪的文件和目录


## **配置**
bash
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
git config --global core.editor "code --wait"  # 设置VS Code为编辑器


## **查看帮助**
bash
git --help            # 查看所有命令
git <cmd> --help      # 查看具体命令帮助


