---
title: "Integration testing e DevOps"
subtitle: "sviluppo e implementazione della libreria Kubesuite"
excerpt: "Tesi di laurea triennale"
header:
  image: /assets/images/kubesuite/dfd-lv0.jpg
  teaser: /assets/images/kubesuite/dfd-lv0.jpg
sidebar:
  - title: "Anno di realizzazione"
    text: "2021"
  - title: "Committente"
    text: "Beantech s.r.l."
  - title: "Relatori"
    text: "prof. Carlo Tasso e Rosario Maione"
  - title: "Tecnologie utilizzate"
    text: "C#, xUnit, Azure Functions, Azure DevOps CI/CD, Docker, Kubernetes"
  - title: "Altro materiale"
    text: >-
        [Tesi in pdf](/assets/docs/Tesi_Triennale___Belliato_Riccardo.pdf)
gallery:
  - url: /assets/images/kubesuite/use_case.png
    image_path: assets/images/kubesuite/use_case.png
    alt: "Diagramma dei casi del sistema"
  - url: /assets/images/kubesuite/dfd-lv1.jpg
    image_path: assets/images/kubesuite/dfd-lv1.jpg
    alt: "Data flow diagram di livello 1 del sistema"
  - url: /assets/images/kubesuite/kubesuite_sequence.png
    image_path: assets/images/kubesuite/kubesuite_sequence.png
    alt: "Diagramma di sequenza test con Kubesuite"
  - url: /assets/images/kubesuite/pipeline.jpg
    image_path: assets/images/kubesuite/pipeline.jpg
    alt: "Pipeline di CI"
  - url: /assets/images/kubesuite/quartznet_class.png
    image_path: assets/images/kubesuite/quartznet_class.png
    alt: "Diagramma di classi test con Kubesuite"
---

Lo scopo del progetto presentato in questa tesi è quello di realizzare degli strumenti di supporto al testing automatico delle Azure Functions in esecuzione su Kubernetes, che si sono concretizzate nell'implementazione di una libreria di supporto ai testi di integrazione chiamata Kubesuite e la descrizione di una sequenza di istruzioni (pipeline) standard che esegue l'intero processo su Azure DevOps.

Si volevano infatti evitare due spiacevoli situazioni incontrate durante lo sviluppo:

- la mancanza di una fase strutturata di testing dei container, la quale si limitava allo scrivere delle Azure Function di test da eseguire in locale e osservarne poi il funzionamento,

- l'utilizzo da parte del team di sviluppo di un modello di Dockerfile non adatto, che portava a potenziali problemi di sicurezza, in quanto prevedeva di esporre in chiaro credenziali utente.

{% include gallery caption=""%}