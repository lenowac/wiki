---
id: 20210328183346
keywords: [guide, automation, zettlr, git]
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