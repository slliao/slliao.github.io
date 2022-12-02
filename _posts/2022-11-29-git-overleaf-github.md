---
layout: post
title: Overleaf + GitHub
categories: [Tools]
tags: [LaTeX, GitHub]
---

### Regular Workflow
1. Make some changes on Overleaf
2. On your computer (while in the local repo directory), run
```
git pull overleaf master
git push github master
```
<!-- more -->

Any changes you made on overleaf should now be on both your local repo and on Github!

If you want to make changes via your local repo, just push to both remote repos (after staging and committing locally):

```
git add .
git commit -m "Adding stuff from local repo"
git push overleaf master
git push github master
```
### Setup

#### Connect Overleaf and your local repo

1. Make a new project on [Overleaf](https://www.overleaf.com).
2. In the share menu, copy the link from "Clone with git"
3. On your computer:
    - use `cd` to navigate to where you want to put your project
    - type `mkdir` and then the name of the project
    - `cd` into that project
    - do `git init`
    - do `git remote add overleaf` with the link you copied
    - so overall this would like something like this

```
cd ~/Desktop
mkdir overleaf-project
cd overleaf-project
git init
git remote add overleaf https://git.overleaf.com/11205025wxdxfsqpxytc
git pull overleaf master
```
### Github token 
#### Using an Access Token for the first time

Follow the instructions on Github to [Create an Access Token in Github](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)

#### Configure Git to use the osxkeychain

By default, git credentials are not cached so you need to tell Git if you want to avoid having to provide them each time Github requires you to authenticate. On Mac, Git comes with an “osxkeychain” mode, which caches credentials in the secure keychain that’s attached to your system account.

You can tell Git you want to store credentials in the osxkeychain by running the following:-

```sh
git config --global credential.helper osxkeychain
```

#### Add your access token to the osxkeychain

Now issue a command to interract with Github which requires authentication, eg. `git clone` or `git pull`. When you are prompted to supply your _Password for 'https://username@github.com':_ you enter your access token instead. Your token should now get cached in the osxkeychain automatically.

```sh
$ git clone https://github.com/username/repo.git

Cloning into 'repo'...
Username for 'https://github.com': your_github_username
Password for 'https://username@github.com': your_access_token
```

---

### Connect your local repo and Github

1. Make a new repo on Github
2. Copy the git remote link
3. On your computer:

```
git remote add github https://github.com/jnaecker/overleaf-project.git
git commit -m "initial commit"
git push github master
```

### Regular Workflow

1. Make some changes on Overleaf
2. On your computer (while in the local repo directory), run

```
git pull overleaf master
git push github master
```

Any changes you made on overleaf should now be on both your local repo and on Github!

If you want to make changes via your local repo, just push to both remote repos (after staging and committing locally):

```
git add .
git commit -m "Adding stuff from local repo"
git push overleaf master
git push github master
```

You may also want to check out [this paper](https://www.overleaf.com/articles/git-and-overleaf-integration/qmdncpnqwfxx#.WcUSSNOGNE4) which explains how you get set up git to push to both Overleaf and Github with just one  `git push command`.

### Git ignore file
```
.DS_Store
*.log
*.gz
*.blg
*.lof
*.aux
*.lot
*.out
```
