---
title: Update GitHub Token
categories: [Tools, Git]
tags: [Git, GitHub]
---

Show current origin
```
git remote -v
```
Remove your current, expired, remote URL:
```
git remote remove origin
```

Add a new remote with your updated GitHub personal access token:
```
git remote add origin https://[PERSONALACCESSTOKEN]@github.com/[USERNAME]/[REPO].git
```

To push the current branch and set the remote as upstream, use
```
   git push --set-upstream origin main
```

