1.__git init__ 把当前目录变成Git可以管理的仓库

2.__git add__ <file> 把文件添加到仓库

3.__git commit -m "..."__ 把文件提交到仓库     可以add多个文件，然后commit一次即可
				add
		工作区----------》版本库（暂存区，分支）

		文件往Git版本库里添加的时候，是分两步执行的：
		第一步是用git add把文件添加进去，实际上就是把文件修改添加到暂存区；
		第二步是用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支


4.__git status__ 查看仓库当前状态

5.__git diff__ 查看修改内容

6.__git log__ 查看提交历史，以便确定要回退到哪个版本

7.__git reset --hard HEAD__ 退回当前版本        `git reset --hard HEAD^` 退回上一个版本          `git reset --hard HEAD^^` 退回上上个版本         `git reset --hard HEAD~100` 退回100个版本

8.__git reflog__ 查看命令历史，以便确定要回到未来的哪个版本


9.__git checkout --<file>__  把文件在工作区的修改撤销
				一种是自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
				一种是已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

10.__git reset HEAD file__ 可以把暂存区的修改撤销掉，重新放回工作区   add之后，还未commit

11.__git rm <file>__ 从版本库中删除文件，并且需要`git commit`


###远程仓库

12.__git remote add origin git@github.com:LucKkK/xxxx.git__  关联一个远程仓库

13.__git push -u origin master__ 第一次推送master分支的所有内容，此后，每次本地提交后，只要有必要，就可以使用命令 `git push origin master` 推送最新修改

14.__git clone git@github.com:LucKkK/xxxxx.git__  克隆一个远程仓库

###分支管理

15.__git checkout -b <name>__  创建并切换分支
        	相当于 git branch <name>  创建分支
        		  git checkout <name> 切换到分支

16.__git branch__ 查看当前所有分支

17.__git merge <name>__ 合并指定分支到当前分支

18.__git branch -d <name>__ 删除分支

19.__git log --graph__ 命令可以看到分支合并图

20.__git stash__ 隐藏工作区 

21.__git stash list__ 查看工作区

22.__git stash pop__ 恢复工作区

23.__git branch -D <name>__ 强行删除没有合并过的分支

24.__git remote -v__ 查看远程仓库详细信息

###标签管理
25.__git tag <name>__ 给分支打标签 `git tag -a <tagname> -m "blablabla..."`可以指定标签信息  `git tag -s <tagname> -m "blablabla..."`可以使用PGP签名标签


26.__git tag__ 查看所有标签

27.__git show <tagname>__ 查看标签信息

28.__git push origin <tagname>__ 推送一个本地标签

29.__git push origin --tags__ 推送全部未推送过的本地标签

30.__git tag -d <tagname>__ 删除一个本地标签

31.__git push origin :refs/tags/<tagname>__ 删除一个远程标签











