---
id: 20210328181358
created: 2021-03-28
title: "Automating Git push/pull with Batch"
keywords:
  - guide
  - automation
  - windows
  - batch
  - git

---
# Automating Git push/pull with Batch

when the actual meaning of the commit isn’t that important as long as the repo is in sync:

```bash
git pull
git checkout main
git add -a
git commit -am "sync"
git push
```
*note that github uses “main” by default where gitlab is using “master” as default branch!*

In case the .bat is usually called by another file and a paramter is passed, use this:

```bash
git pull
git checkout main
git add -a
git commit -am %1
git push
```

to manually pull, commit and push you simply cd into the dir and do `.\push.bat “yourmessage”`

## sources
https://stackoverflow.com/questions/1223721/in-windows-cmd-how-do-i-prompt-for-user-input-and-use-the-result-in-another-com

https://medium.com/@cibiaananth/how-to-add-commit-and-push-to-git-using-one-command-on-windows-25d756f444b7

