# git安装及配置  

##  



### 将本地项目推送到远端
1. 初始化自己的项目放入缓存区  
```
 git init
 
 git add .
```
2. 提交项目到本地的仓库  
```
 git commit -m "本次提交的说明"
```
3. 创建一个远程分支  
```
 git remote add origin XXX(远程分支地址) 
```
4. 将本地仓库推送到远端  
```
 git push origin master 
```
5. 第4步可能报错
  * 报错1 :这个错误是说远端有你没有的东西
```
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://gitee.com/sridntk/spring-cloud-config.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
  * 报错2 :这个错误是说你推送的版本不是最新的
```
  ! [rejected]        master -> master (non-fast-forward)
 error: failed to push some refs to 'https://gitee.com/sridntk/spring-cloud-config.git'
 hint: Updates were rejected because the tip of your current branch is behind
 hint: its remote counterpart. Integrate the remote changes (e.g.
 hint: 'git pull ...') before pushing again.
 hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
所以需要将远程仓库最新版本pull到本地`git pull origin master` 
如果pull不成功
```
fatal: refusing to merge unrelated histories
```
则使用该命令`git pull origin master --allow-unrelated-histories`  
6. pull成功后解决冲突重新提交


#### git reset的时候提示  
>error: bad signature  
fatal: index file corrupt  

由于git的index文件出错.需要删除目标项目下的.git/index文件,重新运行git reset
