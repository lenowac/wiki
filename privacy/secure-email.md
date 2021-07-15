---
id: 20210328173248
created: 2021-01-31
keywords:
  - review
  - privacy
  - communication
  - eMail
---

# Privacy focused eMail

TL,DR: eMail is shit, even encrypted one. Use [[matrix]] if you can.    
If you have to use eMail, be careful: even "secure" providers like protonmail may be legally forced to corrupt your security.   

--> Look for a local tech collective like systemli or riseup.

### Basic terms

You should know what those are:

- e2ee -> end to end encryption
- ZKA -> zero-knowledge-architecture
- IMAP/SMTP -> protocols used to recieve and send mail with mail clients
- mail client (eg: thunderbird, Postbox, FairEmail) -> email program
- prices are per month with a monthly billing cycle

## Classic Freemail

e.g.: Google Mail, Microsoft Outlook, Apple iCloud, yahoo-mail

DO NOT USE **ANY** OF THOSE!
There are many explanaitions online why you shouldnt.

## Selfhosted

### Own server, own domain

- A fucking PAIN in the ass to maintain
- usually a security nightmare
- domain can be easily linked to you
- will be IP blocked by most spam filters

--> DONT DO IT, unless you know 200% what you are doing

### Included with webhosting

- hosting websites =/= hosting mail -> still not very secure
- domain is still tied to you
- pgp is always possible
- imap is always possible

but overall still better than freemail

## Posteo

No free tier.
Paid tier: 1€

- Storage: 2gb (more: 0.25€/GB)
- Security: 2FA,
- Additions: Calendar, Contacts
- uses green energy

Domains: posteo.[lots of tlds]

Notes:

- payment info is not linked to your mail (!!!)
- optional: encryption at rest (but the keys are generated and stored on the posteo server)

Payment Methods: Bank transfer, Credit Card, PayPal, CASH!

## Tech Collectives

Systemli, riseup, etc

- payment is not linked to you
- no logs and full disk encryption
- IMAP and PGP works
- not always 2FA

BUT:

- no zero knowledge architechture
- very limited space
- may be IP blocked by some spam filters

## Mailfence

Free tier:

- Storage: 500mb,
- Security: 2FA,
- Additions: Calendar, Contacts

Paid tier:

- More Storage,
- aliases,
- IMAP/SMTP, ActiveSync,
- Own Domains

Notes:

- no true zero knowledge architecture!

Payment Methods: Visa, Mastercard, PayPal, Bitcoin, Litecoin

## Tutanota

Free tier:

- Storage: 1gb,
- Security: 2FA,
- Additions: 1 Calendar,
- Add. restrictions: search only past 4 weeks

Paid tiers:

- More Storage,
- aliases,
- Own Domains
- multiple users: 12€ each

Available domains:

- tutanota.com
- tutanota.de
- tutamail.com
- tuta.io
- keemail.me

Notes:

- NO IMAP because of its zero-knowledge-architecture
- NO PGP built in! You have to use something like mailvelope
- uses green energy

Payment Methods: Credit Card, PayPal, (soon: monero)

## Protonmail

Free tier:

- Storage: 500mb,
- Security: 2FA,
- Additions: Calendar, Contacts
- Add. Restrictions:
  - 150 Messages per day,
  - only 3 Folders / Labels
  - no autoresponder
  - no custom filters

Paid tiers:

- more messages per day
- More Storage,
- more aliases,
- Own Domains
- IMAP/SMTP
- multiple users: 8€ each

Available domains:

- protonmail.com
- protonmail.ch
- pm.me

Notes:

- IMAP/SMTP is possible with a bridge (linux, macOS, windows), maintaining the zero-knowledge-architecture

Payment Methods: Credit Card, PayPal, Bitcoin, CASH!
