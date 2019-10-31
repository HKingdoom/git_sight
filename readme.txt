Git is a version control system.
Git is free software.
Git指令：
        git add <filename>   添加文件到仓库
        git status   随时掌握工作状态 
        git diff <filename>  查看具体修改什么内容
        git commit -m "xxx" 告诉git将文件添加到仓库并且给出提交说明
        git log   查看版本历史记录
        git reset --hard HEAD^ 回退到上一个版本
        git reset --hard HEAD^^ 回退到上上一个版本
        git reset HEAD <filename>  把暂存区的修改撤销掉，重新放回工作区
        git checkout -- <filename> 把文件在工作区的修改全部撤销掉
        如果往上100个版本，写成HEAD~100。
        git reset --hard <commit前几位> 回到未来的某个版本
        git reflog  记录每一次命令
Git提交过程：工作区 -> git add -> 暂存区 -> git commit -> 版本库  
