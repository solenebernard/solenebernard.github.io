---
title: "Backpack: A Backpropagable Adversarial Embedding Scheme" 
date: 2022-09-14
tags: ["Steganography","Steganalysis","Game theory"]
author: "Solène Bernard, Patrick Bas, John Klein, Tomas Pevny"
description: "Published in IEEE Transactions on Information Forensics and Security, 2022." 
summary: "How to improve sequentially steganography and steganalysis." 
cover:
    image: "cat_and_mouse.png"
    alt: "Sequential game between steganography and steganalysis"
    relative: false
editPost:
    URL: "https://ieeexplore.ieee.org/document/9891839"
    Text: "IEEE Transactions on Information Forensics and Security"

---

---

##### Download

+ [Paper](backpack.pdf)
<!-- + [Online appendix](appendix1.pdf) -->
+ [Code and data](https://gitlab.univ-lille.fr/solene.bernard/backpack)

---

##### Abstract

A minmax protocol offers a general method to automatically optimize steganographic algorithm against a wide class of steganalytic detectors. The quality of the resulting steganograhic algorithm depends on the ability to find an “adversarial” stego image undetectable by a set of detectors while communicating a given message. Despite minmax protocol instantiated with ADV-EMB scheme leading to unexpectedly good results, we show it suffers a significant flaw and we present a theoretically sound solution called Backpack. Extensive experimental verification of minmax protocol with Backpack shows superior performance to ADV-EMB, the generality of the tool by targeting a new JPEG QF100 compatibility attack and further improves the security of steganographic algorithms.

---

## Min-max iterative protocol

#### Pseudo code for the proposed procedure

![](pseudocode.png)

---

## Backpack: BACKPropagable attACK

See on the Figure below the different function $b_{\tau}$ for different $\tau$. For a given value of triplet $g = (g^{−1}, g^{0}, g^{+1})$ (where $g^j ∼ G(0, 1)$ are independently drawn from Gumbel standard distribution), the value of the modification $\tilde{b}_{\tau} = SG(p, g)$ is plotted the z-axis for all possible triplets of probabilities $p = (p^{−1}, p^{0}, g^{+1})$, and for 4 values of $\tau$ . The triplets are plotted in the trilinear coordinate system.
##### Softmax Gumbel function 

![](ternarychanges_softmaxgumbel.png)


---

##### Citation

Solène Bernard, Patrick Bas, John Klein, Tomas Pevny. 2022. "Backpack: A Backpropagable Adversarial Embedding Scheme." *IEEE Transactions on Information Forensics and Security* Volume (17): 3539 - 3554. https://doi.org/10.1109/TIFS.2022.3204218

```BibTeX
@ARTICLE{9891839,
  author={Bernard, Solène and Bas, Patrick and Klein, John and Pevný, Tomáš},
  journal={IEEE Transactions on Information Forensics and Security}, 
  title={Backpack: A Backpropagable Adversarial Embedding Scheme}, 
  year={2022},
  volume={17},
  number={},
  pages={3539-3554},
  keywords={Protocols;Detectors;Games;Costs;Steganography;Security;Distortion;Steganography;steganalysis;distortion function;adversarial attacks},
  doi={10.1109/TIFS.2022.3204218}}
```

## Results

For example the error probability $P_{err}$ of SRNet on detecting stego images with payload of 0.4 bpnzAC embedded by J-Uniward and QF 75 starts at 7.1\% and is increased by +13.6\% to reach 20.7\% after eight iterations. For the same embedding rate and for QF 95, undetectability by XU-Net with J-Uniward embedding is 23.4\%, and it jumps by +25.8\% to reach 49.2\% at iteration 3.

<!-- 
---

##### Related material

+ [Presentation slides](presentation1.pdf)
+ [Dissertation title](https://escholarship.org/uc/item/7jr3m96r) – PhD dissertation on which this paper is based.
+ [Column title](https://cep.lse.ac.uk/pubs/download/cp365.pdf) – Nontechnical column describing the paper. -->

