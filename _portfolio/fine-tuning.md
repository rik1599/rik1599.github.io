---
title: "Fine-tuning Large Language Models for Gamified Urban Mobility Recommendations"
excerpt: "Development of Recommendation Systems for gamified applications using Large Language Models"
header:
    image: /assets/images/finetuning/logo.png
    teaser: /assets/images/finetuning/logo.png
sidebar:
  - title: "Anno di realizzazione"
    text: "2023-2024"
  - title: "Committente"
    text: "[MoDiS Research Unit](https://modis.fbk.eu/)"
  - title: "Relatori e tutor"
    text: >-
        prof. Kevin Roitero,
        dott. Antonio Bucchiarone,
        dott.sa Annapaola Marconi,
        dott. Federico Bonetti
  - title: "Tecnologie utilizzate"
    text: "Python, PyTorch, HF Transformers, Pandas, Scikit-learn"
  - title: "Altro materiale"
    text: >-
        [Tesi in pdf](/assets/docs/Finetuning_Large_Language_Models_for_Gamified_Urban_Mobility_Recommendations.pdf)

gallery:
  - url: /assets/images/finetuning/process.png
    image_path: assets/images/finetuning/process.png
    alt: "Sperimental workflow from raw data to metrics evaluation. We used two methods of cross-validation"
  - url: /assets/images/finetuning/rq1.png
    image_path: assets/images/finetuning/rq1.png
    alt: "Effectiveness metrics, derived by calculating the mean and maximum scores across each fold in the two proposed cross-validation methods: time series split and k-fold"
  - url: /assets/images/finetuning/rq2.png
    image_path: assets/images/finetuning/rq2.png
    alt: "Effectiveness metrics computed over folds for all models. Box plots are ordered by maximum value."
  - url: /assets/images/finetuning/rq3.png
    image_path: assets/images/finetuning/rq3.png
    alt: "Trends of effectiveness metrics computer over folds for all models."
  - url: /assets/images/finetuning/inference1.png
    image_path: assets/images/finetuning/inference1.png
    alt: "Confusion matrices of T5 computed at fold 4 (time-split)"
  - url: /assets/images/finetuning/inference2.png
    image_path: assets/images/finetuning/inference2.png
    alt: "Metrics computed at fold 4 (time-split) grouping dataset by various features. Barplots (E) and (F) represent metrics grouped by type and duration of the candidate challenge. Violinplots in the second row represent the metrics calculated for each user in the dataset. Violinplots (G) represents the accuracy, precision, recall and F1-Score calculated for each user. Plot (H) are the metrics calculated by grouping by week."
---
(In the process of being published)

In response to the growing global emphasis on sustainable living and smart cities, multiple initiatives leveraging cutting-edge technologies like Artificial Intelligence and Social Computing have been introduced by governments and corporations.

Within this framework, the MoDiS Research Unit at the Fondazione Bruno Kessler in Trento has developed ‘Play&Go’, an innovative and automated system designed to set sustainable mobility goals for users.

This thesis presents the development and implementation of a recommendation model powered by
a custom adaptation of a pre-trained Large Language Model (LLM). We leverage the data from the
‘Play&Go’ database into textual prompts to perform an ad-hoc finetuning of the LLM, by setting the model’s objective to predict the likelihood of users accomplishing a set of sustainability goals based on their history of achieving previous objectives. Our approach has been evaluated against other state-of-the-art models in various scenarios. Results show that LLMs are effective in performing effective recommendations in a gamified urban mobility setting.

{% include gallery caption=""%}