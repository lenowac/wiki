---
modified: 2021-06-03T02:45:18+02:00
---

# Containers: LXD

---
id: 20210328203320
created: 2021-01-14
keywords:
  - selfhosting
  - linux
  - containers
---

::::warning
This is very work in progress and needs improvement
::::

_System containers with LXC using LXD_
For docker application containers, goto [[container-apps-docker]]

## Setup

#to-do

## Config

All default,
Remote hosts:

- yunohost / public / https://devbaseimgs.yunohost.org

## YunoHost Dev

Bridge name: lxdbr0 10.156.218.1/24 | fd42:c76a:9381:7448::1/64
Loop device dize: 30GB

in ~/development/ynh-dev do

> $ ./ynh-dev start
> $ ./ynh-dev attach
