---
title: "SSLDashboard"
excerpt: "Portale per la gestione e la generazione di certificati SSL per Nohup s.r.l."
header:
  image: /assets/images/ssldashboard.png
  teaser: /assets/images/ssldashboard.png
sidebar:
  - title: "Anno di realizzazione"
    text: "2016"
  - title: "Committente"
    text: "Nohup s.r.l."
  - title: "Tecnologie utilizzate"
    text: "PHP, Symfony, MySQL, HTML, CSS, Let's Encrypt"
  - title: "Materiale aggiuntivo"
    text: "[Relazione finale](/assets/docs/Relazione_ASL_Belliato_Riccardo.pdf)"
gallery:
  - url: /assets/images/ssl-dashboard/login.png
    image_path: assets/images/ssl-dashboard/login.png
    alt: "Schermata di login"
  - url: /assets/images/ssl-dashboard/homepage.png
    image_path: assets/images/ssl-dashboard/homepage.png
    alt: "Homepage"
  - url: /assets/images/ssl-dashboard/db.png
    image_path: assets/images/ssl-dashboard/db.png
    alt: "Schema entità-relazioni"
---

La ditta Nohup s.r.l. di San Giorgio di Nogaro sviluppa siti web e uno dei problemi che avevano era quella di avvisare i clienti della scadenza dei certificati SSL per i siti che utilizzano HTTPS.
Grazie a questo portale l'utente può vedere i suoi certificati SSL validi, quelli scaduti e quelli in scadenza. In caso di certificato in scadenza è possibile generare un nuovo csr (certificate signing request) dal portale da inviare a una Certificate Authority. Sarà compito poi dell'utente caricare sul portale il file crt (il certificato vero e proprio) con la nuova data di scadenza.

{% include gallery caption="Alcuni screenshot dal portale" %}