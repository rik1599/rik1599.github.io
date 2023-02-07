---
title: "NimC"
excerpt: "Gioco del Nim in C"
sidebar:
  - title: "Anno di realizzazione"
    text: "2020"
  - title: "Committenti"
    text: "Gigante Nicola e prof. Scagnetto Ivan"
  - title: "Tecnologie utilizzate"
    text: "C, UNIX socket"
  - title: "Collaboratori"
    text: "Dumitru Alexandru e Merlo Filippo"
  - title: "Repository"
    text: "[https://github.com/rik1599/NimC](https://github.com/rik1599/NimC)"
gallery:
  - url: /assets/images/nimc/nimserver.png
    image_path: assets/images/nimc/nimserver.png
    alt: "Diagramma di flusso per nimserver"
  - url: /assets/images/nimc/nimclient.png
    image_path: assets/images/nimc/nimclient.png
---

Il progetto consiste nell’implementazione di una versione client/server del gioco chiamato Nim. Il gioco, che si svolge tra due giocatori, prevede due pile di pedine di lunghezza arbitraria. A turno ogni giocatore sceglie una delle due pile e un numero arbitrario di pedine da rimuovere dalla pila scelta. Alla fine, vince il giocatore che si trova a rimuovere l’ultima pedina. Il progetto sarà diviso in un programma nimserver che si occupa di gestire la partita, e un programma nimclient che fornisce l’interfaccia di gioco:

-	nimserver resta in ascolto di connessioni da parte dei client su un socket locale di dominio UNIX,

-	ogni singolo giocatore si collega al server utilizzando nimclient,

-	alla connessione del primo client, nimserver aspetta che se ne connetta un secondo. Dopodiché, fa cominciare la partita gestendo la connessione con i due client su un thread separato, tornando nel thread principale ad aspettare altre connessioni per, eventualmente, gestire altre partite,

-	all’inizio della partita, nimserver sceglie casualmente il numero di pedine presenti nelle due pile, e comunica i due valori ai due client, assieme all’informazione di quale dei due giocatori deve muovere per primo (scelto in modo arbitrario, ad es. il primo ad essersi connesso),

-	ad ogni turno, il server chiede di muovere al client a cui spetta il turno, informandolo sul conteggio attuale di pedine rimaste nelle due pile,

-	quando la mossa di uno dei due giocatori fa terminare le pedine in entrambe le pile, il server informa entrambi i client del fatto che la partita è terminata, informando di chi ha vinto. I client riportano questa informazione all’utente.

Entrambi i programmi devono essere il più robusti possibile: eventuali errori di comunicazione (ad esempio se al server non si collega il client giusto) non devono risultare in crash del programma o in comportamenti bizzarri. Bensì, nimserver deve gentilmente chiudere la comunicazione con un client che comunichi in modo non valido, continuando a gestire correttamente eventuali altre partite in corso. In ogni caso, se un client si disconnette per questo motivo o di sua spontanea volontà, il server non deve subire interruzioni e il client dell’avversario deve accorgersi della chiusura della partita informando l’utente dell’accaduto. Non deve essere possibile per un client assicurarsi la vittoria in modo fraudolento.

{% include gallery caption="Diagrammi di flusso dei due programmi" %}