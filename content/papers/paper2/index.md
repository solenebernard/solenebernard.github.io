---
title: "Work in progress: Improving SMLM with LUSCo" 
date: 2023-12-01
tags: ["SMLM", "Deep Learning"]
author: ["Solène Bernard", "Benoît Lelandais", "Christophe Zimmer"]
description: "Work in progress from my PostDoc in Pasteur Institute" 
summary: "LUSCo is a computational approach to generate multicolour images from SMLM data of distinct molecular structures labeled with the same dye and imaged simultaneously." 
cover:
    image: "lusco_presentation.png"
    alt: "Image caption"
    relative: false
---
<!-- 
---

##### Download

+ [Paper](paper2.pdf)
+ [Online appendix](appendix2.pdf)
+ [Code and data](https://github.com/pmichaillat/unemployment-gap) -->

---

##### Abstract


Studying via Single Molecule Localization Microscopy (SMLM) the interactions between distinct molecular structures within cells requires the visualization of multiple molecular targets in the same sample. But simultaneous multicolour SMLM comes with technical difficulties. Here, we propose a computational approach to recolor SMLM images of distinct molecular structures labeled with the same dye and imaged simultaneously. We demonstrate the approach on composite image of five different structures.

% Main text max 1200


SMLM allows to probe intricate cellular structures at near molecular resolution. Studying the interactions between distinct molecular structures within cells requires the super-resolution visualization of multiple molecular targets in the same sample. Multicolour SMLM based on photoswitchable dyes typically employs fluorescent dyes with distinct spectra to label distinct molecular species. However this method is generally limited to 2-4 colours because of spectral overlaps and differences in blinking efficiencies, requires careful registration and is prone to chromatic aberrations. Sequential DNA-PAINT allows multicolour imaging of many different molecular species with the same dyes but necessitates washing steps in between imaging cycles and requires long acquisition times. 

To overcome those problems, we propose a computational approach to generate multicolour images from SMLM data of distinct molecular structures labeled with the same dye and imaged simultaneously. The central principle underpinning this study pertains to the deep learning model's ability to assimilate spatial patterns of distinct molecules, facilitating their discrimination. To achieve this, the model necessitates a training process using a dataset of both monochromatic and multichromatic images, such as the model learns to recolor monochromatic images thanks to the ground truth multicolor version of it. It is why we curated a synthetic dataset comprising superimposed, independently acquired SMLM images. The artificial superimposition of these images provides us with both monochromatic (obtained by summing the superimposed images) and multichromatic versions. Then we demonstrate the approach on bicolor images  data and show preliminary results on experimental data including microtubules and nuclear pores. Our approach provides an alternative route towards imaging many molecular structures in the same cells at high resolution with a single fluorescent dye.

The deep learning network works as the following. A 

---

##### Figure X: Figure caption

![](paper2.png)

---

##### Citation

Author 1 and Author 2. Year. "Title." *Journal* Volume (Issue): First page–Last page. https://doi.org/paper_doi.

```BibTeX
@article{AAYY,
author = {Author 1 and Author 2},
doi = {paper_doi},
journal = {Journal},
number = {Issue},
pages = {XXX--YYY},
title ={Title},
volume = {Volume},
year = {Year}}
```

---

##### Related material

+ [Presentation slides](presentation2.pdf)

