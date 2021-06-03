<<<<<<< HEAD
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
=======
---
id: 20210328203150
title: "Improve system security"
created: 2021-01-14
keywords:
  - selfhosting
  - linux
  - security
---

# Improve your system security

_Don't be a fucking idiot and then some_

make sure you [set up your ssh correctly](./setup-ssh.md)

## Fail2ban

20210328203159

_Prevent spam, DDoS or Brute Force attacks_

> $ sudo apt install fail2ban
> $ sudo systemctl enable fail2ban
> $ sudo systemctl start fail2ban

## UFW Firewall

20210328204340

### Management

- ufw allow
- ufw deny
- ufw status
- ufw enable
- ufw default deny incoming
- ufw default allow outgoing
- ufw limit

### Explizit Zugelassen

- 22/tcp SSH
- 25 SMTP
- 143 IMAP
- 420 SSH
- 443/tcp HTTPS

### Explizit Verboten (außer temporär zu dev-zwecken)

- 80/tcp http <-- unsicher

Standard: deny incoming, allow outgoing

## Docker Security

can be found here:[[20210328203831]] in [container-apps-docker.md]
>>>>>>> c3844e51df31ca5e0408531eb7becc86db2130ab
