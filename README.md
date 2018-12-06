# pro-git
git 实操


### 本地分支远程分支关联

git branch dev-branch-1

do something... && commit

git push origin dev-branch-1 // 在origin，新建会新建同名分支，但不关联本地分支。

do some other thing... && commit

git push origin dev-branch-1:dev-branch-1-remote // 可以将改动推动到另外一个远程分支。 此时，origin/dev-branch-1-remote 上的内容比 origin/dev-branch-1 上多。 

git branch --set-upstream-to=origin/dev-branch-1-remote // 将本地的分支跟远程某一个已经存在的分支做关联。

git branch -vv 查看本地分支关联的远程分支。

git push origin HEAD:dev-branch-1-remote // fatal: The upstream branch of your current branch does not match the name of your current branch.  To push to the upstream branch on the remote, use 'git push origin HEAD:dev-branch-1-remote' To push to the branch of the same name on the remote, use 'git push origin dev-branch-1'

### 本地远程分支回滚

git reset commit-id // 本地分支回滚到某次提交

git push --force // 强制远程分支回滚