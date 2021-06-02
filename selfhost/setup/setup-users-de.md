---
id: 20210328202918
title: "Setup users and root permissions"
created: 2021-01-14
keywords:
  - selfhosting
  - linux
---

# Users

- root user hat keine admin rechte
- es gibt ein sudo account, jedoch nicht unter root/admin/klarnamen

Warum? Vermeidung von brute force: es muss nun username und passwort geknackt werden.

## root : whats in the folders

ideally nothing.

## \_ : whats in the folders

~/configuration
_(git repo with all config files, subfolders symlink to respective locations)_

~/development
_(for testing out stuff, e.g.: LXC containers)_
/ynh-dev --> YunoHost Container Files

~/Download
_(if needed, curl stuff here)_

Achte auf groß/kleinschreibung! Bei linux sind die Userordner (Documents, Downloads, Pictures, etc) immer groß geschrieben. Alles andere kann ja kleingeschrieben werden, aber das sollte beachtet werden.
