# how to ammend last commit

1. make changes in code
2. ```git add <whatever changed>``` (staging area in gewünschte Zustand bringen)
3. ```git commit --amend```
4. ```git push origin HEAD:refs/for/develop``` (finally push changes to Gerrit)

# how to pull multiple repositories at once

(https://dev.to/rmpato/git-pull-multiple-repositories-at-once-4l68)

```
alias multipull="find . -mindepth 1 -maxdepth 1 -type d -print -exec git -C {} pull \;"
```

# find orphaned branches

```
git branch -r | xargs -L1 git --no-pager show -s --pretty=format:'%(authorname)'
git branch -r | xargs -L1 git --no-pager show -s --pretty=format:' %aN'
git branch -r | xargs -L1 git --no-pager show -s --pretty=format:'%aN ; %D %n' >> orphaned_branches.txt
```
