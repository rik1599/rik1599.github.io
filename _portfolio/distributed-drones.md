---
title: "Esame di Sistemi Distribuiti"
excerpt: "Sistema di coordinamento di una flotta di droni per le consegne"
header:
  image: /assets/images/drones.jpg
  teaser: /assets/images/drones.jpg
sidebar:
  - title: "Anno di realizzazione"
    text: "2022"
  - title: "Committenti"
    text: "prof. Miculan Marino"
  - title: "Tecnologie utilizzate"
    text: "C#, xUnit, Akka.NET"
  - title: "Collaboratori"
    text: "Lena Emanuele"
  - title: "Repository"
    text: "[https://github.com/rik1599/DistributedSystemsExam](https://github.com/rik1599/DistributedSystemsExam)"
  - title: "Altro materiale"
    text: >-
        [Relazione in pdf](/assets/docs/Sistemi_distribuiti.pdf)

gallery:
  - url: /assets/images/drones.jpg
    image_path: assets/images/drones.jpg
  - url: https://raw.githubusercontent.com/rik1599/DistributedSystemsExam/master/diagrams/Others/node-state-diagram.jpg
    image_path: https://raw.githubusercontent.com/rik1599/DistributedSystemsExam/master/diagrams/Others/node-state-diagram.jpg
  - url: https://raw.githubusercontent.com/rik1599/DistributedSystemsExam/master/diagrams/Others/negotiate-state-diagram.jpg
    image_path: https://raw.githubusercontent.com/rik1599/DistributedSystemsExam/master/diagrams/Others/negotiate-state-diagram.jpg
---

Il progetto ha come scopo la realizzazione di una soluzione che permetta ad una flotta di droni (simulata) di coordinare i propri spostamenti in uno spazio aereo, al fine di evitare le collisioni.
Essendo questo un progetto didattico per un esame, quello che si riporta qui è solo un prototipo di una situazione simulata (cioè senza droni fisici). Ciò che però è stato implementato sono gli aspetti di comunicazione legati ai Sistemi Distribuiti.
In pratica, il prototipo realizzato è già pensato per essere eseguito in un ambiente distribuito, dove i processi dei droni sono dispiegati in macchine diverse (oppure sulla stessa macchina, ma in processi separati che comunicano in rete tramite porte diverse).
In breve, l'idea è la seguente:

- si immagina i droni siano dispositivi molto semplici, privi di sensoristica e capaci solo di volare ad un’altezza fissa (uguale per tutti), velocità costante e in linea retta da un punto A ad un punto B. Non si prevede quindi che il drone sia capace di fare cose complesse come cambiare direzione, fermarsi, "vedere" gli altri droni con dei sensori, ecc.

- ad ogni missione corrisponde un attore (un processo eseguito direttamente sul drone), che comunica con gli altri tramite scambio di messaggi,

- quando un drone vuole decollare per portare a termine una missione, prima di partire esegue un algoritmo distribuito che gli permette di:

    -	conoscere tutte le altre missioni attive nello spazio aereo;

    -	contrattare con gli altri droni in attesa per schedulare le partenze in modo da evitare collisioni.

Il tutto è stato implementato nel linguaggio C# (.NET 6), facendo largo uso del framework AKKA.NET per gestire la comunicazione tramite messaggi.

{% include gallery caption=""%}