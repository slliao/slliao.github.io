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

## This method is not secure. This will keep the token visible.
Add a new remote with your updated GitHub personal access token:
```
git remote add origin https://[PERSONALACCESSTOKEN]@github.com/[USERNAME]/[REPO].git

```

## Updating the Access Token

If you need to regenerate the Access Token (maybe you got a new Mac and didn't make a note of your existing token) then follow the procedure before in your Github account settings to generate a new token.

Then, on your local Mac you can either use the Keychain Access app to delete the old token (search for Github.com in the App), or, use the following command.

```bash
git credential-osxkeychain erase
```

Now, the next time you do a `clone/pull/push` etc Github should prompt you for your new token on the command line and entering the new token should also add it to youe local Key Chain.

To push the current branch and set the remote as upstream, use
```
   git push --set-upstream origin main
```

Generate token
1. Access Settings: Click on your profile picture in the top right corner, then select "Settings" from the dropdown menu.
2. Developer Settings: Scroll down the sidebar on the left side of the screen and click on "Developer settings".
3. Personal Access Tokens: In the Developer settings, select "Personal Access Tokens".
4. Generate New Token: Click on the "Generate new token" button.

