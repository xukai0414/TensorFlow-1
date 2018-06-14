> __这不是一篇教程,这是学习过程的一个记录,初次使用GitHub的小白请移步文章末尾的参考链接,__
>
> 1. 先了解Git是什么东西
> 2. Git的工作流程
> 3. 操作Git
> 4. 练习使用
> 5. 边用边学

```python
#----------------------------基本文件操作------------------------#
git　init #初始化本地仓库，一般只要执行一次就可以了
"""
	＃１．未跟踪的文件，就是直接建立的文件,工作区，如：mkdir filename
    ＃２．未提交文件,暂存区,经过下面的add的添加
    ＃３．入档文件,本地仓库(就是记录在点按之中，下一步直接提交到github)，经过commit文件的提交
    ＃４．上传文件，通过push之后上传到网络之上
"""
git add --name #添加文件到本地索引,	
git commit -m --name #添加到本地仓库,同时name的名字是str格式,加以说明
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
git remote -v #查看关联的项目
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
```



![img](https://img-blog.csdn.net/20170713092225478?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvdTAxMzAwNTc5MQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast) 

参考:

[非常好的初级教程](http://www.bootcss.com/p/git-guide/)

[官方文档](https://git-scm.com/book/zh/v2/Git-%E5%9F%BA%E7%A1%80-%E8%AE%B0%E5%BD%95%E6%AF%8F%E6%AC%A1%E6%9B%B4%E6%96%B0%E5%88%B0%E4%BB%93%E5%BA%93)

[Git实例分析一](https://blog.csdn.net/itgungnir/article/details/53031905)

[Git实例分析二](https://blog.csdn.net/u013005791/article/details/75043443)

[Git实例教程三](https://www.jianshu.com/p/715417b93991)



