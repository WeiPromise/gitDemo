1. 远程仓库相关命令

命令 | 说明| 备注 |
--- | --- | --- |
git clone [git url] | 检出仓库 | |
git clone [git remote url] -b [remote branch name] | 检出远端仓库的指定分支 | |
git remote -v | 查看远程仓库 | |
git remote add [name][url] | 添加远程仓库 |  |
git remote set-url --push [name][newUrl] | 修改远程仓库 | |
git pull [remoteName][localBranchName] | 拉取远程仓库 |
git push [remoteName][localBranchName] | 推送远程仓库 |

2. 分支操作相关命令

命令 | 说明 | 备注 |
--- | --- | --- |
git branch | 查看本地分支 |
git branch -r | 查看远程分支 |
git branch [name] | 创建本地分支 | 创建之后并不会自动切换到新创建的分支
git checkout [name] | 切换分支
git checkout -b [name] | 创建新的分支并立即切换到新分支 |
git branch -d [name] | 删除分支 | -d 选项只能删除已经参与合并的分支，对于未参与合并的分支是无法删除的。如果要强制删除一个分支，可以使用 -D 选项
git merge [name] | 合并分支 | 将名称为 [name] 的分支与当前分支合并
git push origin [name] | 创建远程分支（本地分支 push 到远程）|
git push origin :heads/[name] | 删除远程分支 |

3. 若想把本地的某个分支 test 提交到远程仓库，并作为远程仓库的 master 分支，或者作为另外一个名叫 test 的分支，可以这么做

命令 | 说明 | 备注
--- | --- | --- |
git push origin test:master | 提交本地 test 分支作为远程的 master 分支 | 
git push origin test:test | 提交本地 test 分支作为远程的 test 分支 | 


### git 创建仓库并提交代码（首次）/拉取远程代码（首次）

1. 配置信息
- git config --global user.name "***"
- git config --global user.email "***"

2. 创建仓库并提交代码
- git init
- git remote add origin https://\*\*\*/***.git
- git add -A 
- git commit - m "xxx"
- git push -u origin master

3. 拉取远程代码
- git clone https://\*\*\*/\***.git
- cd ***
- git add -A
- git commit -m "xxx"
- git push -u origin master


 