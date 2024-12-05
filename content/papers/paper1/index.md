---
title: "Optimizing Additive Approximations of Non-Additive Distortion Functions" 
date: 2020-06-01
tags: ["Steganography","Steganalysis","Game theory"]
author: "Solène Bernard, Patrick Bas, John Klein, Tomas Pevny"
description: "Published in IEEE Transactions on Information Forensics and Security, 2020." 
summary: "How to improve sequentially steganography and steganalysis." 
cover:
    image: "cat_and_mouse.png"
    alt: "Sequential game between steganography and steganalysis"
    relative: false
editPost:
    URL: "https://doi.org/10.1257/aer.102.4.1721"
    Text: "Journal Name"

---

---

##### Download

+ [Paper](paper1.pdf)
+ [Online appendix](appendix1.pdf)
+ [Code and data](https://github.com/pmichaillat/job-rationing)

---

##### Abstract

This paper proposes an algorithm which allows Alice to simulate the game played between her and Eve. Under the condition that the set of detectors that Alice assumes Eve to have is sufficiently rich (e.g. CNNs), and that she has an algorithm enabling to avoid detection by a single classifier (e.g adversarial embedding, gibbs sampler, dynamic STCs), the proposed algorithm converges to an efficient steganographic algorithm. This is possible by using a $\min\max$ strategy which consists at each iteration in selecting the least detectable stego image for the best classifier among the set of Eve's learned classifiers. The algorithm is extensively evaluated and compared to prior arts and results show the potential to increase the practical security of classical steganographic methods. For example the error probability $P_{err}$ of SRNet on detecting stego images with payload of 0.4 bpnzAC embedded by J-Uniward and QF 75 starts at 7.1\% and is increased by +13.6\% to reach 20.7\% after eight iterations. For the same embedding rate and for QF 95, undetectability by XU-Net with J-Uniward embedding is 23.4\%, and it jumps by +25.8\% to reach 49.2\% at iteration 3.

---

##### Figure X: Figure caption

![](paper1.png)

---

$ \mathcal{Z}{0} $ initial stego base, $\mathcal{X} =\left\lbrace \mathbf{x}_{(1)},..,\mathbf{x}_{(N)} \right\rbrace$ cover base, set of detector $\mathcal{F}^0 = \left\lbrace f^0 \right\rbrace$, $k_{\max}$
 $k \leftarrow 1$\;
 \While{$k \leq k_{\max}$}{
  Obtain adversarial base $\mathcal{Z}{k}=\left\lbrace \mathbf{z}^k_{(1)},..,\mathbf{z}^k_{(N)} \right\rbrace$ where $\mathbf{z}^k_{(n)}=\text{ADV-EMB}\left(\mathbf{x}_{(n)},f_{k-1}\right)$\;
  Create stego base $\xstegos{k}= \left\lbrace \mathbf{y}^k_{(1)},..,\mathbf{y}^k_{(N)} \right\rbrace$ to be least detectable with respect to detectors in  $\fset^{k-1}$, $\mathbf{y}^k_{(n)} = \underset{\mathbf{z} \in \lbrace \mathbf{z}^0_{(n)},..,\mathbf{z}^k_{(n)}\rbrace}{\arg\min}\underset{f \in \fset^{k-1}}{\max}f\left( \mathbf{z}\right)$ \;
  Train a new classifier $f^k$ to discriminate $\xcover$ from $\xstegos{k}$ \;
  $\fset^k = \fset^{k-1} \cup \{\fdet^k\}.$\;
  $k \leftarrow k+1$\;
 }
 Return stego base $\xstegos{k_{\max}}$


##### Citation

Solène Bernard, Patrick Bas, John Klein, Tomas Pevny. 2020. "Explicit Optimization of min max Steganographic Game." *IEEE Transactions on Information Forensics and Security* Volume (16): 812 - 823. https://doi.org/10.1109/TIFS.2020.3021913

```BibTeX
@article{bernard2020explicit,
  title={Explicit optimization of min max steganographic game},
  author={Bernard, Sol{\`e}ne and Bas, Patrick and Klein, John and Pevny, Tomas},
  journal={IEEE Transactions on Information Forensics and Security},
  volume={16},
  pages={812--823},
  year={2020},
  publisher={IEEE}
}
```

---

##### Related material

+ [Presentation slides](presentation1.pdf)
+ [Dissertation title](https://escholarship.org/uc/item/7jr3m96r) – PhD dissertation on which this paper is based.
+ [Column title](https://cep.lse.ac.uk/pubs/download/cp365.pdf) – Nontechnical column describing the paper.

