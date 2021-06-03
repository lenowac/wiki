---
id: 20210328203541
title: "Random linux server tips"
created: 2021-01-14
keywords:
  - selfhosting
  - linux
---
# Docker
*Application containers* 

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
system security: [[20210328203150]] in [[system-security]]
* General: https://docs.docker.com/engine/security/
* Docker daemon socket: https://docs.docker.com/engine/security/https/
* Dockerfile best practices: https://sysdig.com/blog/dockerfile-best-practices/
* Docker Security cheat sheet: https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html