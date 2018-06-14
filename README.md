# TensorFlow
This Repository is myself Study and Notes
``` #----------------------------基本文件操作------------------------#
git　init #初始化本地仓库，一般只要执行一次就可以了
"""
	＃１．未跟踪的文件，就是直接建立的文件,工作区，如：mkdir filename
    ＃２．未提交文件,暂存区,经过下面的add的添加
    ＃３．入档文件,本地仓库(就是记录在点按之中，下一步直接提交到github)，经过commit文件的提交
    ＃４．上传文件，通过push之后上传到网络之上
"""
git add --name #添加文件到本地索引,	
git commit -m --name #添加到本地仓库,同时那么的名字是str格式,加以说明
git remote add origin --adress#添加远程库地址保存在ｏｒｉｇｉｎ里面
git remote rm origin #删除链接的远程库
git push origin --TensorFlow #上传到ＴｅｎｓｏｒＦｌｏｗ这个
git checkout -- test.text #利用暂存区覆盖工作区
git rm --cached test.text #脱离Git的控制,也就是删除暂存和入档状态
#------------------------------分支操作--=-----------------------#
git branch --name 	#建立分支
git branch 			#查看分支信息，带＊的为当前操作分支
git checkout --name #修改操作分支
git branch -D --name #删除分支
#------------------------------
git clone --adress #克隆网上的项目
git remote add origin <address> #关联一个github远程库
git merge --branch_name #合并某分支到当前分支
git push origin :--branch_name #删除远程的分支
git remote rm origin #删除关联库
git tag 1.0.0 1b2e1d63ff #在软件发布时创建标签，是被推荐的,可以执行如下命令以创建一个叫做 1.0.0 的标签.1b2e1d63ff 是你想要标记的提交 ID 的前 10 位字符
git log #查看ID
git log --pretty=oneline #ID查看的更清晰
#-------------------------------HEAD-------------------------#
git rev-parse HEAD #获取最新的头指针
git reset HEAD test.text #用当前版本覆盖暂存区
'''回到上一个版本有两种方式'''
git reset --hard HEAD~1 #HEAD~number,代表上几次版本
git reset --hard 65b88a34150e77b3ba6122238fd1e6b4609f0e85 #后面的ID代表版本号
git log --pretty=oneline #查看版本号
#-------------------------------Tag--------------------------#
'''
	tag的目的是为修改的文件打上版本信息,因为Git直接控制版本没有版本的信息,查看起来不太方便
'''
git reset --hard HEAD~1  #首先回到某个版本,如果是当前版本提交不需要这一步骤
git tag 1.0.0 ab2e1d63ff #打标签
git pull origin 1.0.0 #推送到服务器
