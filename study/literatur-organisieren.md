---
id: 20210603120618
---

# Literatur Organisieren

[Download](https://www.zotero.org/download/)// [Fixe Biblographie](https://zbib.org/#)

**Tutorial's:**

* die [TU Dresden](https://www.youtube.com/watch?v=PqQp_oUUY5w) zeigt die Vorteile und Arbeit gut, auch group libraries werden erwähnt
* die [UB Berlin](https://www.youtube.com/watch?v=rqpRQhK9Al0) zeigt die Recherche gut
* es gibt ein praktisches [Sync tutorial](https://www.youtube.com/watch?v=5UV6Ce3evUY)

### Praktisch

* nur wenn der Rechner über die VPN im Uni Netz ist zieht sich Zotero auch die volle PDF (wenn verfügbar)
* notizen werden auch synchronisiert und zählen nicht mit in den zotero sync speicherplatz.
* mit Zotero sync können[ geteilte Literaturlisten](https://www.zotero.org/groups/) incl Notizen erstellt werden

### Sync

die gesamte Bibliothek und Anhänge können über Geräte hinweg [synchronisiert werden](https://www.zotero.org/support/preferences/sync#file_syncing). #Backup

* es gibt einen [storage space von zotero](https://www.zotero.org/support/sync#zotero_file_storage) der viele Vorteile für Metadaten bietet, aber für PDFs teuer ist.
* nextcloud hat eine komatible lösung, webdav. Einige unis haben eine, zb:
  * [Berlin](https://tubcloud.tu-berlin.de/login)
  * [Chemnitz](https://tuc.cloud)
  * [Landau](https://cloud.uni-landau.de/index.php/login)

Das tolle: beide können verwendet werden. --> Für die Bibliothek Zotero sync nehmen, für die Attachments (PDFs) WebDAV, in meinem fall über die [TUC Cloud](https://tuc.cloud)). 
Dabei musst du folgende Dinge eintragen:

```
url: tuc.cloud/remote.php/dav/files/NUTZERNAME@tu-chemnitz.de
username: NUTZERNAME@tu-chemnitz.de
password: app password
```

Wo "NUTZERNAME" steht muss dein Benutzername (Chemnitz: URZ Kürzel) hin. Das **Passwort** muss in Nextcloud unter "Einstellungen/Sicherheit/Neues App Passwort erstellen" generiert werden, weil die tuc.cloud am SingSignOn (SSO) System der TU hängt. Bei einer (anderen) Instanz ohne SSO reichen die normalen Login-Daten.

Mit dem Zotfile plugin können Attachments auch separat an einem beliebigen Ort gespeichert werden, mit mountainduck kann dieser dann auch wieder eine beliebige cloud sein. Ich persönlich würde jedoch immer den nativen Weg bevorzugen.

Wenn du dich fragst wo das eingetragen werden soll, schau dir das oben verlinkte sync tutorial an oder [lies die Zotero Docs](https://www.zotero.org/support/preferences/sync#file_syncing).

### Nice Addons

* [QuickLook](https://github.com/mronkko/ZoteroQuickLook) (braucht [QuickLook ](https://github.com/QL-Win/QuickLook/releases)für Windows)
* [PDF OCR](https://github.com/UB-Mannheim/zotero-ocr) (braucht [Tesseract](https://github.com/UB-Mannheim/tesseract/wiki) und [Poppler](https://github.com/UB-Mannheim/zotero-ocr/wiki/Install-pdftoppm))
* [SciHub PDF Download](https://github.com/ethanwillis/zotero-scihub)
* [Export Notes as Markdown ](https://github.com/argenos/zotero-mdnotes)(braucht [Zotfile](http://zotfile.com/) und [Better BibTeX (LaTeX und Markdown](https://github.com/retorquere/zotero-better-bibtex))

## Darkmode (Windows)
* download [the file](https://github.com/Rosmaninho/Zotero-Dark-Theme)
* press win + r
* enter "%AppData%\Zotero\Zotero\Profiles\7yz0knbh.default"
* create /chrome folder
* copy "./chrome/userChrome.css" to the respective folder