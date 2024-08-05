---
title: Multiple accounts on GitHub
categories: [Tools, Git]
tags: [Git, GitHub]
---

1. Set up SSH keys
```
ssh-keygen -t rsa -b 4096 -C "work.emailid"
```
```
Enter file in which to save the key (/Users/mark/.ssh/id_rsa): ./id_rsa_freecafe
```
2. Add the SSH (public) key to your Github account.

3. Config SSH configuration file (~/.ssh/config) to manage the two separate keys.
```
# workid account
Host workid-github.com
    HostName github.com
    User workid
    IdentityFile folder/id_rsa_workid
```

4.
```
 git clone git@freecafe-github.com:free-cafe/free-cafe.github.io.git 
```

Check the config
```
git config --list
```


[How to manage multiple Github accounts from a single machine](https://www.educative.io/answers/how-to-manage-multiple-github-accounts-from-a-single-machine)\
[Work With Multiple Github Accounts on a single Machine](https://gist.github.com/rahularity/86da20fe3858e6b311de068201d279e3)\
[8 Easy Steps to Set Up Multiple GitHub Accounts](https://blog.gitguardian.com/8-easy-steps-to-set-up-multiple-git-accounts/)\
[Git: How to Handle Merge Conflicts](https://www.nobledesktop.com/learn/git/merge-conflicts)
