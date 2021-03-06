# Git codes

Quick links:

- [Refresh branch list](https://github.com/tolgayolal/storage/blob/main/code-lib/git/README.md#refresh-branch-list)

## Refresh branch list
This code refresh all branches. Delete closed branches, add new branches etc..
```cmd
git remote update origin --prune
```
Ref : https://devconnected.com/how-to-clean-up-git-branches/


## Clear local branch list
This code remove all merged branches exclude master branch. 
```cmd
git branch --merged | egrep -v "(^\*|master)" | xargs git branch -d
```
Ref : https://devconnected.com/how-to-clean-up-git-branches/

## Mixed usage for clear all branches
```bash
git remote update origin --prune && git branch --merged | egrep -v "(^\*|master)" | xargs git branch -d
```


## Remove local commit
This code remove all commits on local 
```bash
git reset --hard origin/<branch_name>
```
