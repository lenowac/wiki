---
id: 20210328203150
title: "Improve system security"
created: 2021-01-14
keywords:
  - selfhosting
  - linux
  - security

---

# Systemsicherheit [de]
*Don't be a fucking idiot and then some* 

important: read [[setup-ssh]]!

## Fail2ban
*Prevent spam, DDoS or Brute Force attacks*
> $ sudo apt install fail2ban
> $ sudo systemctl enable fail2ban
> $ sudo systemctl start fail2ban

## UFW Firewall
*Essential commands*

* ufw allow
* ufw deny
* ufw status
* ufw enable
* ufw default deny incoming
* ufw default allow outgoing
* ufw limit 

Personally, I **allow:**
* 22/tcp SSH
* 25 SMTP
* 143 IMAP
* 420 SSH
* 443/tcp HTTPS


and **deny**
* 80/tcp HTTP <-- insecure

and set the **standard**: deny incoming, allow outgoing

## Docker 
is a special kind of fun and can be found here: [[container-apps-docker]]