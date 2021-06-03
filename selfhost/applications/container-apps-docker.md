---
id: 20210328203541
title: 'Container: Docker'
created: 2021-01-14T00:00:00+01:00
keywords: [selfhosting, linux]
modified: 2021-06-03T02:42:21+02:00
---

Random linux server tips, this time:
_Application containers with Docker_

Install: https://docs.docker.com/engine/install/ubuntu/
DO NOT INSTALL FROM PACKAGE OR SCRIPT

Test: docker --version

## Post Install

add to systemd autostart:

> $ sudo systemctl enable docker.service

add docker compose: https://docs.docker.com/compose/install/#install-compose

> $ sudo curl -L "https://github.com/docker/compose/releases/download/1.28.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
> $ sudo chmod +x /usr/local/bin/docker-compose

test docker compose:

> $ docker-compose --version

## Docker Security

20210328203831
Be sure to check out [[system-security]] for basic tips on that.

- General: https://docs.docker.com/engine/security/
- Docker daemon socket: https://docs.docker.com/engine/security/https/
- Dockerfile best practices: https://sysdig.com/blog/dockerfile-best-practices/
- Docker Security cheat sheet: https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html
