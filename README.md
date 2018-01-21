1,如果上传本地文件夹到github上面
http://blog.csdn.net/jerryhanjj/article/details/72777618

2，如何在本地编译程序后上传github
http://blog.sciencenet.cn/blog-255662-890909.html

 将master分支推送到github服务器后， 每一次在本地进行修改时，如修整了软件的一个bug， 一般流程如下

（1） 新建一个分支 如 herblabel_dev 命令如下 git checkout -b herblabel_dev

（2） 修改代码， fix the bug

（3） 回到master分支 git checkout master

（4） 将herblabel_dev所做的修改合并到master中: git merge herblabel_dev

（5） 提交所做的修改 git add *

（6） 记录所做的修改 git commit -m "XX bug fixed"

（7） 提交所做的修改到github服务器,输入命令行 git push 


########################################

####### 本地使用分支 Branch ################

6.  创建一个新的分支（branch），将其作为活动分支（checkout），然后就可以编辑、载入和提交新的快照。

## 创建新的分支herblabel_dev

git branch herblabel_dev



7. ## 将herblabel_dev分支作为工作分支

git checkout herblabel_dev



8. ## 继续编辑源代码，git会将改动自动记录到herblabel_dev分支下



9. ## 查看状态

git status



10.  ## 将进行的修改做详细的记录， 并做记录

git commit -m 'Fix Bug A'



11. ## 转换到master分支， git会自动显示哪些地方做了更改。

$ git checkout master



12. ## 将改动的信息保存到git数据库中， 用log 消息记录

$ git commit -a -m 'change files'



13. ### 将 herblabel_dev分支上的改动，合并到当前分支

git merge herblabel_dev



14. ### 删除这个分支

git branch -d herblabel_dev





如果在本地删除了某文件， 而同时希望在github上删除， 则应该先commit

git commit -a -m "A file was deleted"

之后push

git push



###########################

放弃本地所做的所有修改比如master分支：

git reset --hard origin/master
