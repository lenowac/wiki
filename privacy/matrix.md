# Matrix [de]

*dieser guide ist grade stark in Arbeit, sag bescheid wenn dir etwas fehlt :)*

Inhalt:

- Warum Matrix
- Ersteinrichtung
- Öffentliche Server
- Verschlüsselung (Keys und Verifikation)
- Einrichtung auf Smartphones
  - Android
  - IOS
  - Kein Speicherplatz?

## Warum Matrix

#to-do

- sicher
- nicht an telefon oder tel-nummer gebunden
- föderiertes netzwerk

es ist einfacher zu erklären was an allen anderen scheiße ist. [Hier ein text dazu](https://blog.decided.to/25576/messengerdebatte)

<br/>

## Ersteinrichtung

Ich werde hier die schritte für element beschreiben. Es gibt aber auch andere gute clients, zB SchildiChat (basiert auf element) und FluffyChat (minimalistischer). 
WICHTIG: 
- matrix != element
- kein matrix.org account machen

- 1 [Element herunterladen](https://element.io/get-started) bzw [element web](https://app.element.io/?pk_vid=1624108555452221) öffnen
- 2 Account bei einem Homeserver erstellen der NICHT matrix.org ist

    2.1: Edit klicken
    ![2.1: Edit klicken](img/matrix-create_acc-edit.png)

    2.2: Homeserver URL Eintragen
    ![2.2: Homeserver URL Eintragen](img/matrix-create_acc-homeserver.png)
- 3 Keys einrichten (weitere Infos in bei [Verschlüsselung](#verschlüsselung))

Grundsätzlich würde ich von einem Matrix.org Account abraten, weil ein großer Vorteil von Matrix Dezentralisierung ist. Dein Account ist bei einem kleineren Server besser aufgehoben. 

Nun Fragst du dich vielleicht welchen Homeserver du statt matrix.org nehmen solltest. Hier habe ich mal einige aufgelistet, nimm einen der sich angenehm anfühlt. Die Software (synapse) die drauf läuft ist bei allen gleich.

<br/>

<br/>

### Öffentliche Server

- Infoseite | ```Homeserver URL``` # Notizen
- [fairydust.space](https://fairydust.space/) | ```fairydust.space``` # sehr [CCC](https://www.ccc.de) nah
- [envs](https://envs.net/) | ```envs.net``` # [CCC Dresden](https://c3d2.de/) und [FFDD](https://freifunk-dresden.de) nah
- [tchncs](https://tchncs.de/matrix) | ```tchncs.de``` # auch recht zuverlässig

#### Ungeprüft
Kriterien bei der recherche waren hohe uptime, eine aktuelle Version und kein oder ein großes upload limit. Ich habe aber kein Account hier. Probier die ruhig mal aus und sag bescheid wie die so sind:

- [asra.gr](https://wiki.asra.gr/en:start) | ```asra.gr``` # hackspaces.org nah, anarchie icon
- [privacytools](https://www.privacytools.io/services/chat/) | ```privacytools.io``` # etwas groß
- [nitrokey chat](https://www.nitrokey.com/products/nitrochat) | ```nitro.chat```
- [freifunk südholstein](https://freifunk-suedholstein.de/freitrix-freier-datenschutzfreundlicher-messenger/) | ```freitrix.de```

Keine Infos (uptime, version, upload limit) gefunden
- [halogen city](https://halogen.city/about/) | ```halogen.chat``` # sieht sehr solide aus
- [untanga riot](https://riot.untanga.org/) | ```untanga.org``` # run by a person from https://systerserver.net/
- [matrix.cccgoe.de](https://matrix.cccgoe.de) | ```matrix.cccgoe.de``` # CCC Goettingen
- [matrix.un-hack-bar.de](https://matrix.un-hack-bar.de) | ```matrix.un-hack-bar.de``` # CCC Unna (bei Dortmund)

### Tech Kollektive / Inis
Hier gibt's mehr als nur matrix mit einem account. Du musst oft bevor du matrix benutzen kannst ein generelles account erstellen.
- [feneas](https://chat.feneas.org/) | ```feneas.org``` # offen
- [activism.international](https://activism.international/#what-is-activisminternational) | ```activism.international``` # offen, incl. 10GB Nextcloud; [EG](https://www.ende-gelaende.org/) nah
- [systemli](https://www.systemli.org/en/service/matrix/) | ```systemli.org``` # invite oder freundlich fragen :)
- [systemausfall](https://systemausfall.org/dienste/matrix) | ```systemausfall.org``` # freundlich fragen :)
- [fff.chat](https://fff.chat) | ```fff.chat``` # Von FFF Deutschland. Lokale OG Admins Fragen :)

<br/>

<br/>

## Verschlüsselung

In matrix gibt es drei keys (master, user, gerät), praktischerweise musst du dich nur um einen kümmern. Das ist aber recht easy, außer wenn du deinen security key verschlampst und zusätzlich keine aktiven sessions mehr hast.

Das musst du machen:
- 1 Security key einrichten (beim ersten setup oder manuell in den Einstellungen/Sicherheit)
- 2 Diese SICHER (ohne dass andere rankommen, aber so, dass du immer rankommst) abspeichern, zB in einem sicheren Passwortmanager wie [Bitwarden](https://bitwarden.com)
- 3 KEYs NICHT VERLIEREN!

Idealerweise sollten deine Sicherheitseinstellungen in element etwa so aussehen:
![](./img/matrix-setting-cross_signing.png)
![](./img/matrix-setting-secure_backup.png)

Wenn der key fehlt, können alte (verschlüsselte) Nachichten nicht entschlüsselt werden.

![lost-keys](./img/matrix-lost_keys.png)

### Warum so kompliziert

Nachrichten werden lokal auf dem gerät verschlüsselt, aber andere geräte in deinem account brauchen diese keys damit sie die Nachichten deiner anderen geräte lesen können. Mit dem Security key machst du ein verschlüsseltes backup der geräte keys. Gleichzeitig muss ein gerät dieses backup auch lesen können, also muss es auch die keys erhalten.

Praktisch: So können leute die an deine account daten kommen nicht gleich alte nachichten entschlüsseln. Sollten angreifer versuchen den security key zurückzusetzen können die angreifende mit dem neuen key nicht die alten gerätekeys verwenden, weil sie ja mit dem alten security key verschlüsselt wurden. Deine nachichten sind also seeeehr sicher.

Für den fall dass du deinen key verschlampst (passiert den besten) solltest du von allen aktiven geräten die lokalen E2E keys als datei exportieren bevor du einen neuen security key generierst. Danach importierst du einfach die datei und die historie sollte wieder lesbar sein.

![](./img/matrix-setting-session.png)

Wenn du das nicht machst (zb wenn dein gerät weg ist) dann kannst du mit den alten keys verschlüsselte Nachichten nicht lesen.

Für den fall, dass ein gerät eingesackt wird kannst du die entsprechende session zb vom PC aus sperren.
![](./img/matrix-setting-devices.png)

Um auf das warum zurück zu kommen: damit, auch wenn dein account oder ein gerät teilweise geknackt wurde, der chatverlauf noch sicher ist.

### Sinnhaftigkeit von Verschlüsselung

Privatchats sollten immer verschlüsselt werden. Sensible, invite only Gruppenchats auch.

Öffentlich Gruppen zu verschlüsseln ist aber absoluter quatsch, denn (a) alle müssen für alle verschlüsseln, was ein heidenaufwand und riesiger keyaustausch ist und (b) in verschlüsselten chats funktionieren viele spaßige AppServices nicht (zB poll-bot oder die telegram-bridge).

### Verifikation

Du kannst mit anderen die Keys über emojis oder einen QR code scan abgleichen und so sicher sein, dass der account und seine keys auch wirklich zu der person gehört für die du sie hälst.

<br/>

<br/>

## Smartphones

...sind grundsätzlich das absolut unsicherste ÜBERHAUPT und sollten so gar nicht verwendet werden, grade mit dem neuen Abhörgesetz. Aber weil's halt einfach so praktisch ist:

### Android

Auch wenn F-Droid toll ist rate ich zur google play version. Wenn du sehr an Apps wie WhatsApp oder Telegram gewöhnt bist, schau dir mal [schildi chat](https://schildi.chat) an. Das ist element mit paar netten zusatz-features. Dabei aber drauf achten nicht einfach die F-Droid version zu nehmen, sondern vorher (wie auf der Website beschrieben) das repo hinzuzufügen, sonst fehlen push-benachichtigugnen!

FluffyChat gibts auch, finde ich persönlich auch super. Hat aber leider keine Widgets, was etwas unpraktisch ist.

### IOS

Element ist momentan etwas scheiße auf IOS. Wenn etwas nicht funktioniert, überprüfe ob dein matrix an einem SingleSignOn system hängt, bei Tech-Kollektiven ist das oft so. Mein letzter stand war, dass das die app nicht konnte.

Fluffychat kann aber SSO, auch auf IOS.

### Kein Speicherplatz?

Der Webclient [hydrogen](https://hydrogen.element.io/#/login) ist sehr leicht, immerhin ist Wasserstoff das leichteste element. Du musst aber bereits ein Account haben um ihn zu benutzen. Du kannst nur mit H (momentan) weder ein account erstellen noch chats erstellen, aber er ist in rapider Entwicklung.
Außerdem sollten SSOs vermieden werden.

Wenn alles läuft schau ob H push-benachichtigungen schicken kann und füge sie als Verknüpfung oder PWA zu deiner App Übersicht hinzu.

<br/>

<br/>

## Anmerkungen / Feedback / Input 
- bei Clouds wie FFF: Single-Sign-On (SSO) heißt da "Einmalanmeldung"

Fehler gefunden? Ergänzungen? Ideen? --> Ich freue mich über ein [Github issue](https://github.com/lenowac/wiki/issues) oder gleich eine [Pull Request](https://github.com/lenowac/wiki/pulls) ^^
