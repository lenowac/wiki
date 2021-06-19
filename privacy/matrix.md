# Matrix [de]

## Wieso weshalb warum?

- sicher
- nicht an telefon oder tel-nummer gebunden
- föderiertes netzwerk

</br>

## Ersteinrichtung

Ich werde hier die schritte für element beschreiben. Es gibt aber auch andere gute clients, zB SchildiChat (basiert auf element) und Fluffychat (minimalistischer). 
WICHTIG: matrix != element

1. [Element herunterladen](https://element.io/get-started) bzw [element web](https://app.element.io/?pk_vid=1624108555452221) öffnen
2. Account bei einem homeserver erstellen der NICHT matrix.org ist

    2.1: Edit klicken
    ![2.1: Edit klicken](img/matrix-create_acc-edit.png)

    2.2: Homeserver URL Eintragen
    ![2.2: Homeserver URL Eintragen](img/matrix-create_acc-homeserver.png)
3. Keys einrichten (weitere infos in bei [Verschlüsselung](#verschlüsselung))

Nun fragst du dich villeicht welchen homeserver du statt matrix.org nehmen solltest.

</br>

### Öffentliche Server

- infoseite | homeserver URL # notizen
- [fairydust.space](https://fairydust.space/) | ```fairydust.space``` # CCC nah
- [envs.net](https://envs.net/) | ```envs.net``` # ccc dresden nah
- [tchncs.de/matrix](https://tchncs.de/matrix) | ```tchncs.de``` # sehr zuverlässig
- [privacytools.io](https://www.privacytools.io/services/chat/) | ```privacytools.io``` # etwas groß

#### Tech Kollektive / Inis

- [feneas.org](https://chat.feneas.org/) | ```feneas.org```
- [activism.international](https://activism.international/#what-is-activisminternational) | ```activism.international``` # erst [SSO Account](https://cloud.activism.international/apps/registration/) erstellen, dann im matrix client anmelden
- [systemli.org](https://www.systemli.org/en/service/matrix/) | ```systemli.org``` # freundlich fragen :)
- [systemausfall.org](https://systemausfall.org/dienste/matrix) | ```systemausfall.org``` # freundlich fragen :)
- [fff.chat]() | ```fff.chat```

#### Ungeprüft

Einzige kriterien sind 100% uptime, eine aktuelle version und kein oder ein großes upload limit. Ich habe aber kein account hier. Probiert sie aber mal aus und sagt bescheid ob die gut sind:

- [nitrokey chat](https://www.nitrokey.com/products/nitrochat) | ```nitro.chat```
- [asra.gr](https://wiki.asra.gr/en:start) | ```asra.gr```
- [freifunk südholstein](https://freifunk-suedholstein.de/freitrix-freier-datenschutzfreundlicher-messenger/) | ```freitrix.de```

Keine Infos (uptime, version, upload limit) gefunden
- [riot.untanga.org](https://riot.untanga.org/) | ```untanga.org``` # run by a person from https://systerserver.net/

</br>

## Verschlüsselung

1. Security key einrichten
2. SICHER (ohne dass andere rankommen, aber so, dass du IMMER rankommst) abspeichern, zb in einem sicheren passwortmanager wie bitwarden
3. KEY NICHT VERLIEREN!

Wenn der key fehlt, können alte (verschlüsselte) Nachichten nicht entschlüsselt werden.

![lost-keys](./img/matrix-lost_keys.png)

### Sinnhaftigkeit von Verschlüsselung

Privatchats sollten immer verschlüsselt werden. Sensible, invite only Gruppenchats auch.
Öffentlich Gruppen zu verschlüsseln ist absoluter quatsch. In verschlüsselten chats funktionieren viele appservices nicht (zB poll-bot oder die telegram-bridge).

</br>

</br>

## Feedback / Input
- verschlüsselung, keys, verifizieren, WTF
- FFF: sso = einmalanmeldung
