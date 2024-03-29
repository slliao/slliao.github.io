---
title: Branch of GitHub
categories: [Tools, Git]
tags: [Git, GitHub]
---

## Git

List all your branches:
```
$ git branch -a
```
Create a New Branch
```
git checkout -b new-branch-name
```
Or, checkout the branch you want to use:
```
$ git checkout <feature_branch> 
```

Confirm you are now working on that branch:
```
$ git branch 
```
If your local branch already exists on the remote, run this command:
```
git push
```
If your local branch does not exist on the remote, run either of these commands:
```
git push -u origin my-branch-name
```

### Merge a Branch
Check working tree is clean and see what branch you're on
```
git status
```
Check out the branch that you want to merge another branch into (changes will be merged into this branch, for example master).
```
git checkout master
```
Merge another branch into the current branch:
```
git merge my-branch-name
```

## Delete branch
```
git branch -d <feature_branch_name>
```




[Git: How to Handle Merge Conflicts](https://www.nobledesktop.com/learn/git/merge-conflicts)
