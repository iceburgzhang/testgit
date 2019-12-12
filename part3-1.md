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


     


 


