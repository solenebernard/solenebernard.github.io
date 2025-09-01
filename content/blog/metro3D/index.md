---
title: "3D cartography of the parisian metro" 
date: 2025-09-01
tags: ["3D", "map"]
author: ["Solène Bernard"]
description: "" 
summary: "An going project for 3D map of the parisian subway" 
cover:
    image: "overview.png"
    alt: "line_6"
    relative: false
showToc: true
disableAnchoredHeadings: false

---

I’ve always enjoyed noticing how, when we take a step back and observe people’s movements, our cities resemble a complex anthill. The data gathered by public transportation companies looks like a goldmine to me.

I was very happy when I discovered that the RATP (*Régie Autonome des Transports Parisiens*) published a lot of data, I started a project of a 3D cartography of the railway system. Would it not amazing to see how are organized the tunnels ? What's happening below the ground ? How deep is each line ? Is it related to the age of line ? Given that the lines have different age (the most ancient line 1 was built in 1900, and 3 more lines 15,16 and 17 will be finished in 2030), can we explain the trajectory and depth of each ?

They give the 2D coordinates of the stations and  pathways between them, but they don't give the altitude nor depth.

My costly solution is to count the steps of each station, to infer the height or depth of the platform of any station !

##### Live metro location
<!-- <iframe src="metro_map.html" width="8000" ></iframe> -->
[![Metro Map](metro_map.png)](metro_map.html)