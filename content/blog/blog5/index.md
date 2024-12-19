---
title: "After vision, what about hearing? (*in progress*)" 
date: 2024-12-19
tags: ["hearing","theory", "frequency", "Fourier", "cochlea"]
author: ["Solène Bernard"]
description: "We're hearing more than we're seeing." 
summary: "After diving into color perception in the previous blog post, I got interested into understanding more another sensor that mammals have: hearing. Light is a electromagnetic wave, where sound is a mechanical one, but the comparison is relevant because both sound and light signals can be described as a spectrum of wavelenght." 
cover:
    image: "presentation.png"
    alt: "sound signal"
    relative: false
showToc: true
disableAnchoredHeadings: false

---



## Introduction

### What is sound?

Sound is a progressive mechanical wave, meaning it propagates in a transmission medium (like air or water). 

### What is our perception of sound?

We can start by a straightforward observation: humans have the sensation of *sound frequency*. When we hear a music, we hear the pitch, which corresponds to a frequency: what we call a melody is a sequence of sounds with a pitch changing over time. Human created a music system by associating notes to specific range of frequencies, and designed music instrument to produce sound whose main harmonic matches a specific frequency.

The cochlea is the part in the inner ear that allows to analyzing sound frequency and sending it to the brain. It has a snail-like structure, and is covered by hair cells. The spatial arrangement of the membrane is called *tonotopy* (from Greek *tono* for frequency and *topos* for place). 

### Fourier transform

We already talked in this post about Fourier transform. We have mathematical definition for the Fourier representation of any temporal signal. But our cochlea is a biological tool that produced the Fourier transform! There is not such this as metameric sounds, and very distinct sound (in the range of hearing of course) will produce another feeling of sound.

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






