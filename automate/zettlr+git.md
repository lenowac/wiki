---
id: 20210328183346
created: 2021-03-28T00:00:00+01:00
title: "Automating my Zettelbox and Wiki"
keywords: [guide, automation, zettlr, git]
modified: 2021-03-28T18:53:51+02:00

---

# Automating my Zettelbox and Wiki

extending the basics of automating git push/pull with batch (see [[win git pull push]] respectivly [[20210328181358]] Automating Git push/pull with Batch) on windows:

```bash
echo "the cwd is %CD%"

echo "pulling changes"
cd "zettelkasten"
git pull
git checkout master

cd "..\wiki"
git pull
git checkout main


echo "starting zettlr"
start "" /wait "C:\Program Files\Zettlr\Zettlr.exe"


::push in \wiki
push "zettlr close"
cd "..\zettelkasten"
::push in \zettelkasten
push "zettlr close"


exit
```

ill probably add linux and macOS when I boot into the respective system.