#git进行代码管理   
+ git概念
> git是分布式版本控制系统      

##git基本操作

+ 创建版本库   
  首先cd进入想要存放该版本库的位置，输入命令`mkdir XXX（版本库名称）`，即创建版本库       
   
![alt center](https://img-blog.csdnimg.cn/20191208230122865.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ljZWJlcmdfc3Nz,size_16,color_FFFFFF,t_70)        

> pwd显示当前目录                      

+ `git init` 将该目录变成git可管理的仓库    			            

+ `git add XXX（文件名)`将文件添加到暂存区      
     
+ `git commit -m “XXXX”`（提交的注释）将文件提交到仓库    
      
+ `git status `查看是否有文件未提交   
     
 ![alt center](https://img-blog.csdnimg.cn/20191208235251859.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ljZWJlcmdfc3Nz,size_16,color_FFFFFF,t_70)        
           

+ `git diff test.md` 查看文件修改的内容         
> 文件修改后提交仓库时要重复上述步骤                                        

![alt center](https://img-blog.csdnimg.cn/20191208234709375.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ljZWJlcmdfc3Nz,size_16,color_FFFFFF,t_70)       

+ `git log` 查看历史记录         
     
+ `git reset --hard HEAD^`  版本退回      
>上一版本为HEAD^   
>上上版本为HEAD^^ 以此类推    
>版本过多则HEAD~n(n为退回的版本次号）                 

![alt center](https://img-blog.csdnimg.cn/20191208234654250.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ljZWJlcmdfc3Nz,size_16,color_FFFFFF,t_70)        

![alt center](https://img-blog.csdnimg.cn/20191208234646489.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ljZWJlcmdfc3Nz,size_16,color_FFFFFF,t_70)            

+ `cat test.md` 查看内容        
  
+ `git reflog` 可查看退回的版本号
+ `git reset --hard` 版本号  恢复至该版本       

![alt center](https://img-blog.csdnimg.cn/20191208234638749.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ljZWJlcmdfc3Nz,size_16,color_FFFFFF,t_70)         

+ `rm test.md`  删除工作区文件              
+ `git rm test.md`  删除版本库中文件      
     
+ `git checkout --test.md` 恢复文件
+ `git restore test.md` 恢复文件
> `git checkout`与`git restore`都为恢复文件的命令，其实就是用版本库里的版本替代工作区。未被添加到版本库的文件，删除之后无法通过该命令恢复。git rm（文件名）命令直接从版本库中删除文件，删除后也无法恢复。   

![alt center](https://img-blog.csdnimg.cn/20191209105623947.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ljZWJlcmdfc3Nz,size_16,color_FFFFFF,t_70)

##远程仓库
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


## 分支管理    

+ `git branch` 查看分支
+ `git branch <name>` 创建分支
+ `git checkout <name>` 切换分支    
+ `git switch <name>` 切换分支
+ `git checkout -b <name>` 创建+切换分支
+ `git switch -c <name>` 创建+切换分支
+ `git merge <name>` 合并到某分支到当前分支
+ `git branch -d <name>` 删除分支  

> master分支指向提交，HEAD指向当前分支
  在dev分支上修改gittest.md不会改变master分支上gittest.md的内容，只有将dev分支合并到master分支上，才可以看到gittest.md文档发生改变。        

![alt center](https://img-blog.csdnimg.cn/20191209225146514.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ljZWJlcmdfc3Nz,size_16,color_FFFFFF,t_70)      

![alt center](https://img-blog.csdnimg.cn/20191209225156328.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ljZWJlcmdfc3Nz,size_16,color_FFFFFF,t_70)           

+ 参考个人博客
<https://blog.csdn.net/iceberg_sss/article/details/103481765>

 


