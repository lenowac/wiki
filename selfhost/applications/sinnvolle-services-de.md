---
id: 20210328212259
created: 2021-03-28T00:00:00+01:00
keywords: [guide, redundant, selfhosting, linux]
modified: 2021-03-29T00:27:07+02:00
---

# Sinnvolle services

0ka = zero knowledge architecture

|         | Service     | Zweck                                                                  | Notizen                  |
| ------- | ----------- | ---------------------------------------------------------------------- | ------------------------ |
| P \_ A  | Orga (0ka)  | etebase: sync Kontakte, Kalender, To-Do und Notizen                    |                          |
| _ G _   | Chat        | Rocket.Chat, Mattermost                                                |                          |
| P G A   | Chat (0ka)  | Matrix (Synapse) + Element                                             |                          |
| _ G _   | Wiki        | Bookstack, Wiki.js                                                     | hinter rev-proxy auth!   |
| \_ G A  | Pad         | HedgeDoc, etherpad                                                     |                          |
| P \_ \_ | Send (0ka)  | (Firefox) Send: Dateien teilen                                         |                          |
| P G A   | Cloud       | Nextcloud: Google Drive alternative                                    | e2ee ordner: Cryptomator |
| \_ G A  | Cloud (0ka) | Crypad: Files, Pads (WYSIWYG & Markdown), Spreadsheets, Kanban & Polls | unausgereift             |

Das alles sollte in containern gut voneinander getrennt sein.

## Warum kein eMail?

Weil das scheiße aufwändig ist, schwer abzusichern, aufwändig zu betreuen und bei einem Domainumzug einfach nur noch komplett beschissen ist.
Hoste keine mails selber. Wirklich. Hol dir lieber Protonmail, Tutanota, Mailfence oder Posteo je nachdem was du für features möchtest. Ein guide zu eMail providern findest du [hier](../../privacy/secure-email.md)
