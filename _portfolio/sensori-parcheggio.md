---
title: "Sensori di parcheggio IoT"
excerpt: "Sistema IoT homemade per simulare dei sensori di parcheggio"
header:
  image: /assets/images/sensori-iot/app.png
  teaser: /assets/images/sensori-iot/app.png
sidebar:
  - title: "Anno di realizzazione"
    text: "2021"
  - title: "Committenti"
    text: "prof. Scagnetto Ivan"
  - title: "Tecnologie utilizzate"
    text: "Raspberry PI, ESP32, Docker, Motion, MQTT, React"
  - title: "Collaboratori"
    text: "Lena Emanuele, Dumitru Alexandru e Antonutti Davide"
  - title: "Repository"
    text: >-
        - [Sensori a ultrasuoni](https://github.com/rik1599/IoT2021_UltrasonicESP)

        - [Webcam](https://github.com/rik1599/motion-raspberry-docker)

        - [Interfaccia Web](https://github.com/emanuelena49/iot-parking-sensors-ui)

        - [Docker compose](https://github.com/alexandruparaschivdumitru/iot-parking-sensor-config)

        - [Buzzer](https://github.com/Antonutti99/iot-parking-app-buzzer)
  - title: "Altro materiale"
    text: >-
        [Relazione in pdf](/assets/docs/Relazione-1.pdf)

gallery:
  - url: /assets/images/sensori-iot/app.png
    image_path: assets/images/sensori-iot/app.png
    alt: "Mockup dell'applicazione web"
  - url: /assets/images/sensori-iot/architettura-v2.png
    image_path: assets/images/sensori-iot/architettura-v2.png
    alt: "Architettura del progetto"
  - url: /assets/images/sensori-iot/esp01-s.jpg
    image_path: assets/images/sensori-iot/esp01-s.jpg
    alt: "Circuito per il funzionamento del buzzer"
  - url: /assets/images/sensori-iot/esp32.jpg
    image_path: assets/images/sensori-iot/esp32.jpg
    alt: "Circuito per i sensori di posizione ad ultrasuoni"
---

L’obiettivo del progetto è quello di costruire un sistema di sensori di parcheggio che sfrutta le tecnologie IoT per fornire un servizio comparabile a quello dei sistemi in commercio.
Il sistema è costituito da:

- un ESP-32, che ha il compito di effettuare le misure delle distanze e gestire i sensori ad ultrasuoni,

- un ESP-01-S, che ascolta i cambiamenti delle distanze e pilota un buzzer per produrre il feedback sonoro,

- un Raspberry PI 3B+ che fa da hotspot wi-fi e fa girare una serie di componenti software,

- una videocamera USB collegata al Raspberry,

- Il protocollo MQTT per la gestione delle comunicazioni (con il relativo broker),

- Il protocollo HTTP per lo streaming video,

- un'interfaccia Web responsive scritta in React, accessibile quindi da una molteplicità di dispositivi e che non richiede l’installazione su ognuno di essi,

- Docker per il deployment dei vari componenti software.

{% include gallery caption=""%}