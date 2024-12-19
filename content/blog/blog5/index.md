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

## Fourier transform

We already talked in this post about Fourier transform. We have mathematical definition for the Fourier representation of any temporal signal. But our cochlea is a biological tool that produced the Fourier transform!

