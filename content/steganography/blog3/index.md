---
title: "JPEG compression" 
date: 2022-11-01
tags: ["vision","theory", "colors"]
author: ["Solène Bernard"]
description: "From photon to digital images" 
summary: "Because my thesis aims at hiding information in digital images, let's first dive into the origins of photography and then digital images." 
cover:
    image: "DCTFilters.png"
    alt: "colored image"
    relative: false
showToc: true
disableAnchoredHeadings: false

---

The pioneering work of Joseph Fourier in the early 19th century on representing functions as sums of sinusoidal components (now formalized as the Fourier transform), has become a fundamental tool across scientific and engineering disciplines. Fourier analysis allows signals to be expressed in the frequency domain, facilitating efficient manipulation and interpretation of data. In digital image processing, this principle underpins compression algorithms such as JPEG, which rely on transforming spatial pixel data into frequency components to exploit redundancies and perceptual limitations of the human visual system. By isolating and quantifying the image’s frequency content, JPEG compression selectively reduces or eliminates high-frequency details that are less perceptible, achieving significant data reduction while maintaining visual fidelity. 

The most famous compression algorithm JPEG was motivated by the challenge of finding a new representation of images where the content of images can be represented in fewer features than the number of pixels in the image. It relies on the Discrete Cosinus Transform (DCT) proposed by Nasir Ahmed in 1972 which is derived from the Discrete Fourier Transform (DFT).


##### Visualization of the 64 DCT Filters F[i,j], where i is for the row and j for the column. Horizontal frequencies increase from left to right (with increasing j), and vertical frequencies increase from top to bottom (with increasing i). The constant-valued basis function at the upper left is often called the DC basis function, and the corresponding DCT coefficient d[0, 0], the DC coefficient.
<p align="center">
<img src="DCTFilters.png" width="500"/>
</p>


##### Vizualization of effect of image JPEG compression for three quality factors, f = 25, 50 and 100.
<p align="center">
<img src="effectQF.png" width="300"/>
</p>
