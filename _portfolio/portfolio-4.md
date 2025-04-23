---
title: "Election data warehouse in Friuli Venezia Giulia Region"
excerpt: "A data warehouse with election data in Friuli Venezia Giulia Region from 2008 to 2022, developed in Python"
collection: portfolio
---

Data Warehouse with election data in Friuli Venezia Giulia Region from 2008 to 2022.
In particular, the data of the elections are collected

- Political

- Regional

- European

- Municipal

This project consists of:

- a series of scripts that collect electoral data from institutional sites using Selenium for webscraping pages on JSON files,

- a script that takes the data in JSON, normalizes them and converts them into CSV and/or sqlite databases according to a defined DFM model,

- a script that through the [Atoti](https://www.atoti.io/) tool takes the previously created CSV files and builds two OLAP cubes and a web interface to navigate and query the cubes.

For further information and instructions (in Italian language), please refer to the [GitLab repository](https://gitlab.com/rik1599/dw-elezioni).