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
        git checkout -- <filename> 把文件在工作区的修改全部撤销掉；如果在版本库中已保存文件，文件删除后可使用该指令恢复
        如果往上100个版本，写成HEAD~100。
        git reset --hard <commit前几位> 回到未来的某个版本
        git reflog  记录每一次命令
        git rm <filename> 删除指定文件  -->  git commit -m "xxx" 提交说明
Git提交过程：工作区 -> git add -> 暂存区 -> git commit -> 版本库  
场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。

场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD <file>，就回到了场景1，第二步按场景1操作。

场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。
Git提交到github：git push origin master
Git分支:
        git switch -c sight_0401   创建分支并切换到sight课程第四阶段一班
        git branch <name>  创建分支
        git switch master 切换到主线
        git checkout <name>  切换分支
        注意：切换支线修改文件后如果不使用合并，切换到主线以后文件内容不会更改。
        git merge sight_0401 合并指定分支到当前分支
        git branch 查看分支