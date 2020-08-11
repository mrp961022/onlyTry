# onlyTry
## 一些常用的 非git中的命令
* echo aasss >> aa.txt 生成aa.txt 并写入内容 aasss
* touch 文件名 创建文件
* vi 文件名 修改文件   进去后按i；退出按esc，然后输入:wq

## git命令（进入Git文件夹）
> .gitignore 设置忽略目录(是一个文件)  //包裹的文件夹   *.txt文件 写法如下
```
/node_modules // 文件夹
aa.txt // 文件
```
* git init 上传第一步 
* git add 1.txt 把1.txt添加到缓存区
* git commit -m "14:15"  把缓存区的文件添加到历史记录区并添加备注14:15
* git status  查看状态
* git reflog  查看历史记录
* git log   查看用户名，邮箱及操作时间
* git log --pretty=oneline 查看版本信息 会省略很多无用信息
* git reset --hard fcfe3a7  切换到id为fcfe3a7的记录 id就是那一长串文本的前7位
* git push -f 提交 注意切换指定版本的时候push要加上-f
* git rm 1.txt 删除1.txt -------------------------
* git reset HEAD 撤销                             |恢复删除的内容
* git checkout -- 1.txt 暂存区恢复到工作区---------
* git checkout -b dev 创建子分支dev并切换到dev
git push --set-upstream origin dev 在远程仓库创建dev分支
* git branch  查看本地分支
* git branch -r 查看远程分支
* git branch -a 查看所有分支
* git checkout master  切换到master分支
* git merge dev  合并子分支dev
* git branch -d dev 删除dev分支（失败了就大写-d试试）
* git push origin --delete dev 删除远程dev分支
* git tag v1.0   给当前添加标签
* git tag v2.0 cc170be  给某个id的添加标签
* git tag        查看标签
* git show v2.0  查看指定标签
* git tag -d v2.0 删除指定标签
* git push --tags 提交所有的标签
* git push origin [tagnames] 提交指定标签
* git push origin -v1.0  上传到github
* git push origin:refs/tags/v1.0 删除远程标签
* git diff  查看差异

-------------------------------------------------------------------
## Git上传步骤
* 1.github 新建工程项目，并复制项目地址
* 2.Git上git clone 地址
* 3.git bare init
* 4.把你要上传的东西放在clone后生成的目录下
* 5.切换到clone生成后的目录
* 6.设置忽略项
* 7.git add .  git commit -m '备注'
* 8.git push -u origin 分支名

_______________________________________________________________________

## git 拉取步骤
* 1.先新建一个目录
* 2.git config --global uer.name "你的github名字"  git config --global uer.email "你的邮箱"
* 3.ssh-keygen -t rsa -C "你的邮箱"  输入文件名 输入密码
* 4.git clone github上的地址
