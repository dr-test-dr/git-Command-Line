### Git操作
  * 集中式和分布式：  
    svn：集中式版本  版本库是集中存放在中央服务器的，而干活的时候，用的都是自己的电脑。  
    git：分布式版本  每个人电脑里都有完整的版本库，同时修改后相互比对。  
   
   
  * git三大分区：  
    工作区(working diretory) 用于修改文件  
    缓存区(stage) 是用来暂时存放工作区中修改的内容  
    提交历史（commit history） 提交代码的历史记录  
    
    
  * 创建版本库(repository)：    
     在指定文件夹下运行 git init -> 把这个目录变成Git可以管理的仓库。    
   
  * 把文件存放到版本库：  
      >  1. git add readme.txt       (把文件添加到仓库)  
         2. git commit -m "xxxx"     (把文件提交到仓库,xxx 为这次提交的注释)  
            git status               (查看仓库当前的状态，一般在commit前使用) 
                                      执行后： modified:   xxx.xxx -> 可以看到修改的文件或者 nothing to commit, working tree clean   
            git diff                 (查看修改的内容)  
            
  * 工作区和版本库：  
    > 工作区： 只的本地的文件区。  
      暂缓区： 属于版本库，git add 只是把文件提交的暂缓区。  
      版本库： git commit 把暂缓区的内容提交的当前分支。  
    
  * 撤销修改：  
    > git checkout -- file           (可以丢弃工作区的修改)  
      git reset HEAD <file>          (把暂存区的修改回退到工作区。用HEAD时，表示最新的版本)  
  
  * 克隆远程仓库：  
    > git clone https/ssh(仓库地址)  
    
  * 添加远程仓库：  
    > git remote add origin https/ssh(仓库地址)  
    
  * 本地库的内容推送到远程：  
    > git push                        (把当前分支master推送到远程)  
    
  * 创建分支：  
    > git checkout -b dev(分支名称)   ==>  git branch dev + git checkout dev  创建并切换分支    
      git branch                      (查看所有分支，* 为指向当前分支)  
      git merge dev                   (合并指定分支到当前分支)  
      git branch -d dev               (删除分支)
      
      git switch  <==> git checkout   (切换分支，推荐使用switch，比checkout要更容易理解)  
      

    
    
### 常用的git 命令   
    
    git add # 将工作区的修改提交到暂存区  
    git commit # 将暂存区的修改提交到当前分支  
    git reset # 回退到某一个版本  
    git stash # 保存某次修改  
    git pull # 从远程更新代码  
    git push # 将本地代码更新到远程分支上  
    git reflog # 查看历史命令  
    git status # 查看当前仓库的状态  
    git diff # 查看修改  
    git log # 查看提交历史  
    git revert # 回退某个修改  
  
