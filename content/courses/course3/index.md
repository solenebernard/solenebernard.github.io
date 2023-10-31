---
title: "Synesthesia - When vision meets music"
date: 2022-03-10
tags: ["synesthesia", "algorithm"]
author: "Solène Bernard"
description: "Very basic introduction of steganography principle" 
summary: "Vizualization of music via rain drops" 
cover:
    image: "partitionkey.png"
    alt: "Figure caption"
    relative: false
showToc: true
disableAnchoredHeadings: false
editPost:
    URL: "https://youtube.com/playlist?list=PL5zEkRHvv2GxQlFbNf-YqSPMP6ePc3DQf"
    Text: "YouTube playlist"
# bibliography: biblio.bib

---

## The concept

**Synesthesia**, from greek *syn*, « with » and *aesthesis*, « sensation » is a neurologic phenomenom where two or more senses are associated. For example, some people picturing letters of the alphabet with a color experience the most common type of synesthesia. Even if it is a non-volontary and durable condition, I propose several visual illustrations of music via different algorithms analyzing sound signals in the rubric with the sententious name *Synesthesia*.  

## Rain drops : the mathematical modelization

2D vizualization of a drops

$$ S_{k,v, \phi}(r,t) = A_{k, v}(r,t) \times \cos \big(k(r+vt) + \phi\big) $$

with 

$$ A_{t_0, k, v}(r,t) = \begin{cases}
    e^{-\lambda_0 r}e^{-\lambda_1 t} & \text{if } t >= 0 + \frac{r}{kv}, \\ % & is your "\tab"-like command (it's a tab alignment character)
    0 & \text{otherwise.}
\end{cases} $$ 

where the different variables are defined as the following:
- $r \geq 0$ is the distance to the spatial origin of the drop
- $t$ is the duration of time elapsed since the drop hit the water
- $k > 0$ is the wavenumber
- $v > 0$ the velocity of the propagation of the wave in the water
- $\lambda_0>0$ is a scalar which controls the exponential decrease of amplitude with distance to the origin ($r$)
- $\lambda_1>0$ is a scalar which controls the exponential decrease of amplitude with time ($t$)

## Code snippets

```
def spatial_wave(xx, yy, t, t0, origin, k, speed, phase, A, l0, l1):
    '''
    Input : 
    - xx the x-coordinates
    - yy the y-coordinates
    - t the time value
    - t0 the time when the drops falls 
    - origin the spatial coordinates of the location of where the drop falls
    - k the wavenumber
    - speed the velocity of the propagation of the wave in the water
    - phase the initial phase
    - l0 the lambda_0 parameter which controls the exponential decrease of amplitude with distance to the origin
    - l1 the lambda_1 parameter which controls the exponential decrease of amplitude with time
    '''

    # Compute the vector r of distance to the spatial origin
    xy = np.stack((xx,yy),axis=-1)
    r = np.linalg.norm(xy-origin.reshape((1,)*len(xy.shape[:-1])+(2,)),axis=-1)

    # Compute amplitude
    t1 = t0 + r/(k*speed)
    a = np.zeros_like(r)
    delta_d = speed*k*2/(np.pi)*(t-t0)
    a[r<=delta_d] = A*(np.exp(-l0*r)*np.exp(-l1*(t-t0)))[r<=delta_d]

    # Signal
    s = a*np.cos(k*(r - speed*(t-t0))+phase)

    return(s)
```