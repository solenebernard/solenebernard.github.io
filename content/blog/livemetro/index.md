---
title: "Parisian metro" 
date: 2025-07-15
tags: ["hearing","theory", "frequency", "Fourier", "cochlea"]
author: ["Solène Bernard"]
description: "" 
summary: "Using RATP open data for live visualisation  (*in progress*)" 
cover:
    image: "presentation.png"
    alt: "sound signal"
    relative: false
showToc: true
disableAnchoredHeadings: false

---

RATP, the parisian transportation company gives in [open data](https://data.iledefrance-mobilites.fr/) details about live traffic, including at what time arrives the next train at each station.

Because there is no exact localisation of the metro, we could infer the exact position of each metro by:
- computing the average duration and distance between each pair of consecutive stations
- infer from the next train arrival time and destination where is located the train in the tunnel.

For now, the location of metros is approximated by the position of the next station it's coming to.

##### Live metro location
<!-- <iframe src="metro_map.html" width="8000" ></iframe> -->
[![Metro Map](metro_map.png)](metro_map.html)