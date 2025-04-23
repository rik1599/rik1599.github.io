---
title: "Kubesuite - Kubernetes Testing Framework"
excerpt: "A framework for testing Kubernetes clusters and applications, developed C#"
collection: portfolio
---

The purpose of the project presented in this thesis is to build tools to support automated testing of Azure Functions running on Kubernetes, which resulted in the implementation of an integration text support library called Kubesuite and the description of a standard instruction sequence (pipeline) that executes the entire process on Azure DevOps.

Indeed, two unpleasant situations encountered during development were to be avoided:

- the lack of a structured container testing phase, which was limited to writing Azure Function tests to be executed locally and then observing their operation,

- the development team's use of an unsuitable Dockerfile template, which led to potential security issues, as it involved exposing user credentials in plain text.

Thesis (in Italian language) is available at [this link](/files/Tesi_Triennale___Belliato_Riccardo.pdf).

![Kubesuite Level 1 DFD](/images/portfolio/dfd-lv1.jpg)