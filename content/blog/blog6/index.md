---
title: "Origins of colored photography" 
date: 2024-12-19
tags: ["vision","theory", "colors"]
author: ["Solène Bernard"]
description: "From photon to digital images" 
summary: "Because my thesis aims at hiding information in digital images, let's first dive into the origins of photography and then digital images." 
cover:
    image: "imagecolor.png"
    alt: "colored image"
    relative: false
showToc: true
disableAnchoredHeadings: false

---



## Introduction

### What is photography

Photography, which means etymologically “coloring with light” is the ambitious challenge to convert into an object the environment which created a physical sensation in a human.
This technique is more than standard today, as it is part of our daily lives as all of our smartphones can take pictures. However, until the last century, photography was not ordinary, requiring considerable technological and scientific progress.

Two dominant photographic sensors exist: CCD (Charge-Coupled Device) and CMOS (Complementary Metal Oxide Semiconductor) using the photoelectric effect. It quantifies the number of photons hitting a photographic cell array to translate it to numerical data. In order to reproduce coloured photography, researchers first looked for the biological composition of the human eye. It is in [1802 that Young discovered](https://www.jstor.org/stable/pdf/107113.pdf "The Bakerian Lecture: On the Theory of Light and Colours") that it exists three types of photoreceptors (now known as cone cells) in the human eye, each of which are sensitive to a particular range of visible light, named short, medium, or large given their size.

A few years later, Maxwell demonstrated theoretically in 1855 [9] that any monochromatic light stimulating three receptors should be able to be equally stimulated by a set of three different monochromatic lights. This would mean that a superposition of three colours could reproduce every sensation of colour, therefore called primary colours. Therefore, the first colour photography was produced by tak- ing pictures three times of the same scene with three coloured filters.

Today, the representation of colour digital images still relies on the superposition of three colour channels: red, green, and blue, so three types of sensors are used. Figure 1.1 shows both absorption spectrums of receptors in the eye and in a Nikon D700 camera look alike.
In order to take at one instant a picture with three kinds of pho- toreceptors, the most common solution is to use a colour filter array (CFA). It is a mosaic of tiny colour filters placed over the pixel sensors of an image sensor to capture colour information. Multiple subjective designs of the CFA exist. The most popular one is the Bayer Filter, plotted in Figure 1.2.

The raw image data captured by the image sensor is then converted to a full-colour image (with intensities of all three primary colours represented at each pixel) by a demosaicing algorithm which is tailored for each type of colour filter.
Gray scale images are coded only with one channel. It contains the luminance Y , which is equal to a linear combination of the three color channels R, G and B:

$Y = 0.299R + 0.587G + 0.114B$


### What is our perception of sound?

We can start by a straightforward observation: humans have the sensation of *sound frequency*. When we hear a music, we hear the pitch, which corresponds to a frequency: what we call a melody is a sequence of sounds with a pitch changing over time. Human created a music system by associating notes to specific range of frequencies, and designed music instrument to produce sound whose main harmonic matches a specific frequency.

The cochlea is the part in the inner ear that allows to analyzing sound frequency and sending it to the brain. It has a snail-like structure, and is covered by hair cells. The spatial arrangement of the membrane is called *tonotopy* (from Greek *tono* for frequency and *topos* for place). 

### Fourier transform

We already talked in a previous post about Fourier transform. We have mathematical definition for the Fourier representation of any temporal signal. But our cochlea is a biological tool that produced the Fourier transform! There is not such this as metameric sounds, and very distinct sound (in the range of hearing of course) will produce another feeling of sound.

## What if our ears would work as our eyes?

Let's imagine we would had three cones which each would be sensitive to a different spectrum of frequencies. Just like for our eyes, there would be different sounds which produce the same hearing feeling: there would be metameric sounds.

Would we be able to invent a melody, which under the assumption of cones in our ears, would give the same sound?

### Let's find the melody

Let's imagine we have three cones with each sensitivy $S_i(f)$. Two sounds $I_0$ and $I_1$ are metameric if $ \sum_f S_i(f)I_0(f) = \sum_f S_i(f)I_1(f)$. 


Let's find a sound signal $I(f, t)$, such that, $\forall t$:
+ $R_0 = \sum_f S_0(f)I(f, t) = $ constant
+ $R_1 = \sum_f S_1(f)I(f, t) = $ constant
+ $R_2 = \sum_f S_2(f)I(f, t) = $ constant





## Do we hear more than we see?

We can argue that we hear more than we see because of how is encoded information. The space of hearable signals is way bigger than the one of visible colors. 

But colors are not the only information given by our eyes. There are million of cone cells in our eyes that give us also *spacial information* about colors. Whereas we only have two ears that limits the spatial localization of our environment! 

To conclude, I would just say this less catchy phrase: we hear way more than we see colors :) 






