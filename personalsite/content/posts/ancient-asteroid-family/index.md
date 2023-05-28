---
title: Identification of 4.3 billion year old asteroid family and planetesimal population in the Inner Main Belt
date: 2023-05-22
author: Salvatore Ferrone
description: An inside look at the methods used to identify the family and the implications of the results.
toc: true
math: true
---


<!-- <style>
body {
    background-image: url('https://upload.wikimedia.org/wikipedia/commons/7/76/Ceres_-_RC3_-_Haulani_Crater_%2822381131691%29_%28cropped%29.jpg');
    background-repeat: no-repeat;
    background-size: 100 100%;
}
</style> -->





## Who, what, when, and where?
I am [Salvatore Ferrone](), a PhD student at l'Observatoire de Paris, the first author of the paper, and the author of this blog. This blog discusses a scientific paper about asteroids in the main belt of the solar system that is being published in te European journal [Astronomy & Astrophysics](). This work was initiated during a 2021 summer internship under professor Marco Delbo at the Observatoire de la Côte d'Azur in Nice, France. This was between first and second years of my master's degree. I continued this work for my master's project in the spring of 2022, and finalized it during a second contract between my masters and PhD in the summer of 2022. The paper was submitted to Astronomy and Astrophysics in the fall of 2022, and was accepted for publication on 22 May 2023 after peer review.

The co-authors of this paper are:
* [Marco Delbò](https://www.oca.eu/en/marco-delbo): 
    - My supervisor, and the person who initiated this project. He is a professor at the Observatoire de la Côte d'Azur in Nice, France. He is an expert in asteroid families, and has been working on them for over 20 years. 
* [Alessandro Morbidelli](https://www.oca.eu/en/alessandro-morbidelli)
    - Alessandro is a professor at the Observatoire de la Côte d'Azur in Nice, France. He is an expert in the formation and evolution of the solar system, and has been working on it for over 20 years.
* [Chrysa Avdellidou](https://www.oca.eu/en/chrysa-avdellidou) 
    - Chrysa is a post-doctoral researcher at the Observatoire de la Côte d'Azur in Nice, France. She is an expert in the formation and evolution of the solar system, and has been working on it for over 10 years.
* [Kevin Walsh](https://www.boulder.swri.edu/~kwalsh/cv.html)
    - Kevin is a senior scientist at the Southwest Research Institute in Boulder, Colorado, USA. He is an expert in the formation and evolution of the solar system, and has been working on it for over 20 years.
* [Rogerio Deienno](https://www.boulder.swri.edu/~rdeienno/)
    - Rogerio is a post-doctoral researcher at the Observatoire de la Côte d'Azur in Nice, France. He is an expert in the formation and evolution of the solar system, and has been working on it for over 10 years.
* [Robert Melikyan](https://www.lpl.arizona.edu/graduate/students/robert-melikyan)
    - PhD student at the University of Arizona in Tucson, Arizona, USA. Working in catestrophic disruption of asteroids and the subsequent formation of asteroid families.

### Why?
This blog is written in support of the publication submitted to Astronomy and Astrophysics. I wanted to add more detail to the paper and provide a more in-depth explanation of the methods used to identify the family, and make the work more understandable for someone unfamiliar with the literature. 

### How? 
This blog was written using Markdown, and the website was built using Hugo. The theme used is [Hugo Blog Awesome](https://hugo-blog-awesome.netlify.app/). The research was done with much dedication and time!


## Context

all images were taking from wikipedia unless otherwise specified 

### What is an asteroid?
* Cerres was the first asteroid discovered by a sicilian astronomer, Giuseppe Piazzi, in 1801.
* This is the only asteroid in the main belt to have reached hydrostatic equilibrium, meaning that it is the only one to have become spherical due to its own gravity. 
![ceres](https://upload.wikimedia.org/wikipedia/commons/7/76/Ceres_-_RC3_-_Haulani_Crater_%2822381131691%29_%28cropped%29.jpg)
Crredit: NASA.  Creative Commons Attribution 2.0 Generic license.

This images comapres the size of Ceres to the moon, which is much smaller, additionally, on the left we have the asteroid Vesta, which is the second largest asteroid in the main belt.

![vesta](https://upload.wikimedia.org/wikipedia/commons/f/f9/Ceres_and_Vesta%2C_Moon_size_comparison.jpg)
Crredit: Gregory H. Revera Ceres image: Justin Cowart Vesta image: NASA/JPL-Caltech/UCAL/MPS/DLR/IDA.  Creative Commons Attribution 2.0 Generic license.



If we take the 10 first discovered astetoids and compare it to the moon, we recieve this schematic 
![asteroid](https://upload.wikimedia.org/wikipedia/commons/0/0e/Moon_and_Asteroids_1_to_10.svg)
Credit: NASA.  Public Domain.

### What is the solar system and the asteroid belt ?
* What's the mass of the entire belt?
    - about 4.0% of the mass of the moon
    - all of the asteroids in the system are 1/3 of the moon's mass


<img src="https://upload.wikimedia.org/wikipedia/commons/f/f3/InnerSolarSystem-en.png"  width="100%" height="100%">
Credit: Alan Chamberlain, JPL/Caltech.  Public Domain.

How many asteroids are there? it depends when you stop counting! 
![SFD](https://upload.wikimedia.org/wikipedia/commons/6/63/Asteroids_by_size_and_number.svg)
Credit: Polytechnic University of Milan. Marco Colombo, DensityDesign Research Lab. CC BY-SA 4.0

The mean motion resonances with jupiter create gaps in the asteroid belt.
<body>
<div class=".div-1">
<img src="/kirkwoodgaps.jpeg"  width="100%" height="100%" >
</div>
</body>
Credit: Alan Chamberlain, JPL/Caltech.  Public Domain.


This phenomenon is also seen in the rings of saturn
![ringsSaturn](https://upload.wikimedia.org/wikipedia/commons/8/8a/Unraveling_Saturn%27s_Rings.jpg)
Credit: NASA/JPL. Public domain

there are some places where resonance features causes stability, such as the orbits of jupiter's moons. 

![jupitersmoons](https://upload.wikimedia.org/wikipedia/commons/e/e5/Galilean_moon_Laplace_resonance_animation_2.gif)

Credit: Public domain


### What is an asteroid family?
* collision between two asteroids

Credit: [Patrick Michel](https://lagrange.oca.eu/fr/patrick-michel/1582-michel-patrick), Observatoire de la Côte d'Azur, France

![patrick](https://lagrange.oca.eu/images/LAGRANGE/pages_perso/michelp/videos/Koronis3kmr20a0.gif)
![orbitalElements](https://upload.wikimedia.org/wikipedia/commons/e/eb/Orbit1.svg)

![osculting_versus_proper](https://upload.wikimedia.org/wikipedia/commons/9/9d/Asteroid_osculating_vs_proper_elements.png)


![inclination](https://upload.wikimedia.org/wikipedia/commons/a/ab/AsteroidIncAu.png)


### Why study asteroid families?
Proto-planetary disk
![Solar system formation](https://upload.wikimedia.org/wikipedia/commons/7/74/Protoplanetary_Disk_Simulated_Spiral_Arm_vs_Observational_Data.jpg)

![RadialSeparation](https://upload.wikimedia.org/wikipedia/commons/5/56/Soot-line1.jpg)


This simulation is a bit different from the asteroids brining us stuff because the smallest bodies simulated are about the same size as ceres, thus none are ceres sized or smaller. 
![RobertsAnimation](/Emsenhuber2022LPSC.gif)


[Emsenhuber et al](https://www.hou.usra.edu/meetings/lpsc2022/pdf/1815.pdf). A systematic survey of giant impacts over a wide range of parameters. 53rd Lunar and Planetary Science Conference (2022). The Woodlands, TX, USA.

THE FORMATION OF THE SOLAR SYSTEM. TALK ABOUT THE NICE MODEL. MAYBE SHOW A TIMELINE

https://en.wikipedia.org/wiki/Nice_model

try to find a video! discuss the planetary formation scenarios. Much more about the motivation of the work. 

Nice model
![Nice Model](https://upload.wikimedia.org/wikipedia/commons/0/0f/Lhborbits.png)
Gomes, R., Levison, H., Tsiganis, K. et al. Origin of the cataclysmic Late Heavy Bombardment period of the terrestrial planets. Nature 435, 466–469 (2005). https://doi.org/10.1038/nature03676




### How do we detect asteroid families? The Hierarchical Clustering Method

#### How does the HCM work?
The hierarchical clustering method (HCM) is a method use to identify clusters in a data space. It operates with using a similarity metric, when bodies are more similar to one another they will be groupped together. This metric can be made more restrictive or more permissive depending on the application. The HCM is a bottom up approach, meaning that it starts with each body as its own cluster and then merges them together. This differs from a divise approach, where all bodies initiate in one cluster and then the number of clusters are divided. Additionally, as the metric is increased, the HCM can merge two adjacent clusters. Once this is done, all bodies in the data set will be in one cluster. *Thus, the difficulty when applying the hierarchical clustering method is knowing when to stop*. 


What is the metric for the context of asteroids? It's is approximatly the $\delta v$ needed to go from one orbit to another. The analogy is I am making is to that of the [Hohmann transfer](https://en.wikipedia.org/wiki/Hohmann_transfer_orbit), where the $\delta v$ is the change in velocity required to change one orbit to another. This $\delta v$ is a proxy for the energy change in orbital energy required. On a more percise level, the $\delta v$ is computed as follows:

$$ 
\delta v = n'a' \sqrt{k_1 \left(\delta a / a' \right)^2+k_2 \left(\delta e\right)^2+k_3 \left(\delta i\right)^2},
$$ 

where *n* is the mean motion (2$\pi$ per orbital period), *a* is the semi-major axis, *e* is the eccentricity, and *i* is the inclination. The primes are present to indicate that these are the mean quantities between the two bodies. Additionally, coefficients were introduced to preserve the original assumption that the ejection velocities are isotropc (equally random in all directions). The authors used $k_1=5/4$, $k_2=2$, and $k_3=2$, and raise the claim that as long as the coefficients are order unity, the main results undergo no dramatic changes. (*although, in their article they do state that the coefficients over estimate the $\delta v$ of a isotropic break-up event by a factor of 2, this confused me*).

Below is an example of a stalactite graph, which plots the clustering as a function of the 
$\delta v$, as stated in the description. Interestingly, we can see clusters begining to merge with aroundthe red lines which indicate their potential stopping $\delta v's$. For instance, The (298) Baptistina is merged with (08) Flora at $\delta v=75$ m/s, and subsequently (4) Vesta at $\delta v=100$ m/s.

![stalactit](/masiero-2013.png)
Mesiero et al 2013. *Asteroid Family Identification Using the Hierarchical Clustering Method and WISE/NEOWISE Physical Properties* [DOI: 10.1088/0004-637X/770/1/7](10.1088/0004-637X/770/1/7)

#### How do we know when to stop?


![HCM](/zappala-quasi-random-noise.jpeg)
A modified version of Fig. 3 from Zappala et al 1990. *Asteroid families. I. Identification by Hierarchical Clustering and Reliability Assessment.* ([DOI](https://ui.adsabs.harvard.edu/abs/1990AJ....100.2030Z/abstract)) 

In essence, to create the background the clusters are ``disolved'' by two dimensionally binning the data in in proper element space, and shuffling the positions within each bin. This is done to preserve the large scale variations of the data but to remove the clustering. This was great for 1990, but how can we do now?

First, this method is limited in two ways 
- The size and width of the bins is arbitrary.
- The family members are still included in the new ``background''. Thus, the density is over estimated and the quais random level noise will be over estimated, which in turn under estimates the size of the family.


## What is the current state of the before this work?

![Nesvorny-2015-fig-1](/nesvorny-2015-fig-1.webp)
Figure 1 from Nesvorny et al 2015. *Identification and Dynamical Properties of Asteroid Families*.
[DOI: arXiv:1502.01628](https://doi.org/10.48550/arXiv.1502.01628).

## What has changed since 2015? 
    - More and more implementation of the Yarkovsky effect to characterize the families.

### What is the Yarkovsky effect?

![diurnalAndAnnual](http://www.scholarpedia.org/w/images/2/2e/Diurnal_seasonal_variants_V2.png)
Figure 1 from [Bottke et al 2005](https://doi.org/10.1016/j.icarus.2005.09.009). *The Yarkovsky and YORP Effects: Implications for Asteroid Dynamics*.

What does this force mean? it means that an asteroid's orbit will drift predominately depending on its spin axis. Also, interestingly enough, the Yarkovsky effect changes the semi-major axis of the asteroid in a way that is inversely proportional to its size. Thus, smaller asteroids are more affected by the Yarkovsky effect than larger asteroids. Here is a simulation of the Yarkovsky effect on a population of asteroids.
![yark](/yarkov-gif.gif)

Data taken from [Deienno et al 2021](https://doi.org/10.1016/j.icarus.2020.114218), *Efficiency characterization of the V-shape asteroid family detection method*. 

Previously, the Yarkovsky effect was used as an afterthought to calibrate the age of families, for instance:

![Nesvorny-2015-fig-6](/nesvorny-2015-fig-6.png)
Also taken from [Nesvorny et al 2015](https://doi.org/10.48550/arXiv.1502.01628). *Identification and Dynamical Properties of Asteroid Families*. Note that the force is linearly propertional to the diameter and but there is an exponential dependence if using magnitude, hence the curve in the v-shape. 

To me, I think the first time I saw this mentioned in the literature was [Walsh et al 2013](https://doi.org/10.1016/j.icarus.2013.03.005), *Introducing the Eulalia and new Polana asteroid families: Re-assessing primitive asteroid families in the inner Main Belt*. However, in this case it was not used a detection method but rather to calibrate the age of the family.

Shortly after it began to be used to detect families a former PhD student à l'observatoire de la côte d'azur [Bryce Bolin](https://www.bolinastro.com/), executed a thesis studying different techniques of the ``v-shape'' detection method. 

![Bolin-2017-fig-1](/bolin-2017-figure-1.png)

Figure 1 from [Bolin et al 2017](https://doi.org/10.1016/j.icarus.2017.05.004), *Yarkovsky V-shape identification of asteroid families*.


Here's a little animation that demonstrates how it works

![detectionmethod](/v-shape-detection.gif)
Again, synthetic data from [Deienno et al 2021](https://doi.org/10.1016/j.icarus.2020.114218). 

Quickly, this method was applied to discover new asteroid families:

![delbo-2017](/delbo-2017-figure-2.png)
From [Delbo et al 2017](10.1126/science.aam603)

The age of this family is XX

This also happened again in [Delbo et al 2019](https://doi.org/10.1051/0004-6361/201834745), *Ancient and primordial collisional families as the main sources of X-type asteroids of the inner main belt*. 

Two more families with the ages of XX and XX


## Methods

### Filtering the data set
![albedo_divider](/albedo_divider.png)
We only concern ourselves with high albedo asteroids that are within the inner main belt!

![proper-elements-all](/proper-elements-all.png)
This is that distribution of the proper elements of the asteroids in the inner main belt.



![proper-elements-notnesvorny](/proper-elements-notnesvorny.png)

### Removing the known families

First, instead of using the quasi-random level such as previous papers that use the HCM, we use the modeling of what we expect an asteroid belt to look like if there were no families in it given how we understand the motion of the planets today. This dataset is shown here:
![proper-elements-deienno](/proper-elements-deienno.png)

We want to scan for new families, but the older families get in the way. Thus, we remove them from the data set. But if we remove them using Nesvorny's catalog, we will still have contamination!

Contrary to what was shown in Maserio et al 2013, we only look at one family of interest at a time and do not apply the HCM to the entire belt. Also, we take its known v-shape characteristics from Nesvorny et al 2015. 
![ferrone-2023-fig-five](/ferrone-2023-fig-five.png)

If you do this for all the families, you get this result:

It's a gif because we tested seven different values of a free parameter.
![proper-elements-background](/proper-elements-background.gif)

### Detecting a new family

![detections-mean-stacking-horizontal](/detections-mean-stacking-horizontal.png)
- we also came up with a new way of probing members, which is looking at the bodies that are within the lobes. 

### Uncertainties
I am skipping over some details in the last image, but in essence we make this detection. 

![diameter-half.gif](/diameter-half.gif)

### Planetesimal population

![SFDs-corrected-vcomp.png](/SFDs-corrected-vcomp.png)

### A note on a correction 

![SFD-comp-demo.png](/SFD-comp-demo.png)
- the correction 1 and 2 are refering to two different ways of compensating for dynamical and collisional loss. 

## Conclusion?
- detection of an ancient family, near the limit of the age of the solar system
    -   however, difficult to say with such high uncertainty. 
- why do we only have a handful of ancient asteroid families, but many young families?
    - is this because of depleation biasing the detection of ancient families?
    - is this because of there being less ancient families?
    - Thus, did the belt form massive OR did the belt form nearly empty?
    - See [Deienno's abstract](https://www.hou.usra.edu/meetings/acm2023/pdf/2549.pdf) at un upcoming conference discussing the ``empty belt" scenario
- Paradigm shift percentage of bodies considered to be part of the background or part of families. 
    - previously about 75 percent of bodies were family lesss
    - now, about 25 percent of bodies are family less are 75 are assigned to families!
        - this makes more sense, because an asteroid can only be an original object OR a collisional fragment... Since collisions produce many many asteroids, finding planetesimals is like finding a needle in a haystack.


## Future work?
- Spectroscopic follow-up by Jules Bourdelle de Micas
- Performing this elimination style analysis in all parts of the belt
- reassessing the known families with this v-shape constrained HCM paradigm more rigorously
- Bayesian approach to probability of each body belonging to a family?
- A better way to compute the age of the family, with a more rigorous treatment of the Yarkovsky effect and uncertainties. 




