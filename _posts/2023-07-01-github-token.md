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

Generate token
1. Access Settings: Click on your profile picture in the top right corner, then select "Settings" from the dropdown menu.
2. Developer Settings: Scroll down the sidebar on the left side of the screen and click on "Developer settings".
3. Personal Access Tokens: In the Developer settings, select "Personal Access Tokens".
4. Generate New Token: Click on the "Generate new token" button.

