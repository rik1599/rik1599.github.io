---
title: "Data Warehouse elezioni in Friuli Venezia-Giulia"
excerpt: "Data warehouse con i dati delle elezioni in Friuli Venezia Giulia dal 2008 al 2022"
header:
  image: https://gitlab.com/rik1599/dw-elezioni/-/raw/master/diagrams/dfm.drawio.svg
  teaser: https://gitlab.com/rik1599/dw-elezioni/-/raw/master/diagrams/dfm.drawio.svg
sidebar:
  - title: "Anno di realizzazione"
    text: "2023"
  - title: "Committenti"
    text: "prof. Coppola Paolo"
  - title: "Tecnologie utilizzate"
    text: "Python, Selenium, Pandas, Atoti, Docker"
  - title: "Repository"
    text: "[https://gitlab.com/rik1599/dw-elezioni](https://gitlab.com/rik1599/dw-elezioni)"
---
Data Warehouse con i dati delle elezioni in Friuli Venezia Giulia dal 2008 al 2022.
In particolare vengono raccolti i dati delle elezioni

- Politiche

- Regionali

- Europee

- Comunali

Questo progetto consiste in:

- una serie di script che raccolgono i dati elettorali dai siti istituzionali utilizzando Selenium per il webscraping delle pagine su file JSON,

- uno script che prende i dati in JSON, li normalizza e li converte in CSV e/o database sqlite secondo un modello DFM definito,

- uno script che tramite il tool [Atoti](https://www.atoti.io/) prende i file CSV creati in precedenza costruisce due cubi OLAP e un'interfaccia web per navigare e interrogare i cubi.

Per ulteriori informazioni si rimanda al file README del repository.