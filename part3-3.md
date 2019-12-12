# 分支管理    

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