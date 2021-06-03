---
id: 20210328202849
title: "Setup SSH logins"
created: 2021-01-14
keywords:
  - selfhosting
  - linux
---

# Setup secure SSH logins

Dont use ssh-copy-id cause its actually quite messy

## Client side

Genereate local SSH key pair

> $ ssh-keygen -t rsa -b 4096

Optional: Give it a **memorable** password

Upload public key, name it something useful

> $ scp ~/.ssh/id_rsa.pub [USER]@161.82.126.102:/home/[USER]/.ssh/[KEYNAME].pub

bsp: $ scp ~/.ssh/id_rsa.pub tobias@161.82.126.102:/home/guenter/.ssh/name-wsl.pub

## Server side

Append key to authorized keys file

> $ cat [KEYNAME].pub >> authorized_keys

Set correct permissions on server:

> $ chmod 700 ~/.ssh/
> $ chmod 600 ~/.ssh/\*

### In case of a local server you may need to to this:

Check if the service is working and if the firewall is configured properly

> $ sudo service ssh status
> $ sudo ufw allow ssh

Check if the service is enabled after a restart, if not run no2 as well

> $ sudo systemctl list-unit-files | grep enabled | grep ssh
> $ sudo systemctl enable ssh

## Deactivate password only auth

Make a backup of the config

> $ sudo cp /atc/ssh/sshd_config cp /atc/ssh/sshd_config.bak

Change config

> $ sudo nano cp /atc/ssh/sshd_config

There uncomment the line "PasswordAuthentication yes" and change it to no.

Restart the ssh service

> $ sudo service ssh restart
