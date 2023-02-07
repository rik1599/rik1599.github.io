---
title: "ScegliMeglio"
excerpt: "Sistema online per le scelte sociali sviluppato secondo metodologia SCRUM"
header:
  image: /assets/images/sceglimeglio.png
  teaser: /assets/images/sceglimeglio.png
sidebar:
  - title: "Anno di realizzazione"
    text: "2023-in corso"
  - title: "Committenti"
    text: "prof. Coppola Paolo"
  - title: "Tecnologie utilizzate"
    text: "Python, Django, Bootstrap, Azure DevOps, SCRUM"
  - title: "Collaboratori"
    text: "Tomada Simone, Travasci Stefano, Zamolo Riccardo"
  - title: "Repository"
    text: "[https://dev.azure.com/ingsw2223-heavyware/PollAtMe](https://dev.azure.com/ingsw2223-heavyware/PollAtMe)"
---

Si richiede di costruire una web app che permetta di definire sondaggi a scelta multipla e raccogliere le
preferenze dei votanti.
Il sistema deve permettere di registrarsi e di avere uno spazio personale in cui gestire i sondaggi. I
sondaggi devono poter essere creati, avviati, chiusi, cancellati. I risultati devono poter essere visualizzati
e scaricati in formato csv.
L’interfaccia deve essere responsive.
Il sistema deve permettere ai votanti dei sondaggi di poter esprimere le proprie preferenze accedendo
tramite link o codice. I votanti devono avere la possibilità di accedere ad un’area riservata in cui poter
trovare tutti i sondaggi a cui possono partecipare e quelli a cui hanno partecipato.
I sondaggi devono poter essere di 3 tipi:

- A preferenza singola: il votante deve poter scegliere solo una delle opzioni. L’ordine finale delle opzioni è dato dalla somma delle singole preferenze.

- Metodo Schulze: il votante deve poter ordinare le opzioni.

- Metodo del giudizio maggioritario: il votante esprime un giudizio su una scala a 5 o 7 valori che vanno da Ottimo a Pessimo, per ognuna delle opzioni.

Il sistema viene sviluppato seguendo i dettami della metodologia SCRUM.

Il portale è visitabile al sito [https://sceglimeglio.azurewebsites.net/](https://sceglimeglio.azurewebsites.net/)