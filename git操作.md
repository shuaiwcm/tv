# git仓库基础操作
## 仓库基本管理
初始化一个git仓库
`git init`    #初始化当前文件夹为一个git仓库
## 将文件添加到git的暂存区
`git add "readme.txi"`
注：使用`git add -A`或`git add .`，可以提交当前仓库的所有改动
## 查看仓库当前文件提交状态
`git status -s`
## 从git的暂存区提交版本到仓库，参数`-m`后为当次提交的备注信息
`git commit -m "1.0.0"`
## 将本地仓库信息推送上传到服务器
`git push https://giteee.com/***/test.git`
如果是克隆下来的仓库，可以省去链接
直接`git push`会提示输入用户名密码，可以配置TOKEN后，能过SSH克隆，再上传时不用输入密码。
# 远程仓库管理
## 修改仓库名
一般来讲，默认情况下，在执行克隆操作时，仓库名者是origin如果说多们想给它改名为wang，可以使用以下命令
`git remote rename origin wang`
## 添加一个仓库
在不执行克隆操作时，如果想将一个远程仓库添加到本地仓库中，可以执行
`git remote add origin "https://"`
注意：`origin`是你仓库的别名，可以随便改，但请务必不要与已有的仓库别名冲突，仓库地址一般来讲支持`http/https/ssh/git`等协议，其他协议地址请勿添加
## 查看当前仓库对应的远程仓库地址
`git remote -v`
这条命令能显示你当前仓库中已经添加了的倒库名和对应的仓库地址，通常来讲，会有两条一模一样的记录，分别是fetch和push，其中fetch是用来从远程同步，push是用来推送到远程。
## 修改仓库对应的远程仓库地址
`git remote set-url origin "https://`
