#远程仓库
+ 登陆GitHub创建仓库或使用已有的仓库     

+ `git remote add origin 仓库地址`       
  将本地仓库与远程仓库关联
+ `git push -u origin master`     
  将本地库的所有内容推送到远程库
> 由于远程库是空的，第一次推送master分支时，加上-u参数，git不但会把本地的master分支内容推送的远程新的master分支，还会把本地master分支和远程的master关联起来，在以后的推送或者拉取时就可以简化命令          

+ `git push origin master `        
  将本地master分支的最新修改推送至GitHub     


![alt center](https://img-blog.csdnimg.cn/20191209131453484.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ljZWJlcmdfc3Nz,size_16,color_FFFFFF,t_70)      

> 已使用`git remote add origin 仓库地址`命令关联远程仓库


+ ` git clone 仓库地址 `  克隆整个仓库
> 仓库地址可用HTTPS或者ssh，通过ssh支持的原生git协议速度更快    

+ `git pull <远程主机名><远程分支名>:<本地分支名>`    
  拉取远程主机某个分支的更新，再与本地的指定分支合并        
> 要取回origin主机的next分支，与本地的master分支合并      

    git pull origin next:master