---
title: "Esame di Programmazione su Architetture Parallele"
excerpt: "Implementazione del metodo del simplesso in CUDA"
header:
  image: https://raw.githubusercontent.com/rik1599/SimplexOnCuda/master/relazione/img/tableau.png
  teaser: https://raw.githubusercontent.com/rik1599/SimplexOnCuda/master/relazione/img/tableau.png
sidebar:
  - title: "Anno di realizzazione"
    text: "2022"
  - title: "Committenti"
    text: "prof. Formisano Andrea"
  - title: "Tecnologie utilizzate"
    text: "C, C++, CUDA, R"
  - title: "Collaboratori"
    text: "Tomada Simone"
  - title: "Repository"
    text: "[https://github.com/rik1599/SimplexOnCuda](https://github.com/rik1599/SimplexOnCuda)"
  - title: "Altro materiale"
    text: >-
        [Relazione in pdf](https://raw.githubusercontent.com/rik1599/SimplexOnCuda/master/relazione/relazione.pdf)
---

In questo progetto si propone una implementazione del metodo del simplesso a due fasi
in CUDA per la risoluzione dei problemi di programmazione lineare in forma canonica.
Questa classe di problemi permette di modellare un gran numero di situazioni reali in molteplici ambiti (ottimizzazione dei costi, creazione di orari, *etc.*), oltre che alcuni problemi NP-hard come il Knapsack o il Vertex Cover.
Il software R è stato utilizzato per analizzare i tempi di esecuzione dell’algoritmo e valutarne performance e scalabilità.