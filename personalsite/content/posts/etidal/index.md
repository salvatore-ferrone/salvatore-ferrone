---
title: "Thesis Introduction"
date: 1996-06-15T17:29:22+02:00
draft: false
math: true
---



### The QR Code to this website
![QR-salvatore.ferrone.github.io](/QR-salvatore.ferrone.github.io.png)



## The Goal

<font size="20">**To model the mass loss of all Galactic Globular Clusters**</font>



## The basics
* What are globular clusters?
* What is the Galaxy?
* What do you mean by *mass loss*?

![NGC](https://www.nasa.gov/sites/default/files/thumbnails/image/heic1321a.jpg)
Image of the Milky Way Globular Cluster NGC 7028 (M15) Credit: Credits: NASA, ESA

![streams](https://upload.wikimedia.org/wikipedia/commons/9/95/Sig07-008.jpg)
Credit: NASA/JPL-Caltech/R. Hurt (SSC/Caltech)


### Fun facts
* There are about 160 globular clusters in the Milky Way
* Each globular cluster has about $10^4$ and $10^6$ stars
    * For context, the Milky Way has about $10^{11}$ stars
* From isochrones, we know that the stars in globular clusters are about 10 billion years old
    * making them some of the oldest objects in the Milky Way
* Stars in globular clusters are not very massive about 0.8 $M_{\odot}$
    - the spectrum of masses typically span less than an order of magnitude

* 0.8 $M_{\odot}$ 
quando hai una populazione vecchia le stelle lasciono la sequenza principale, il turn e quando cambiano da idrogenon. piu che il turn off e bassa piu che la popolazione e vecchia. tutte quelle stelle massice sono altrove, forse nel branch dei giganti o sono diventati delle stelle che hanno smesso di briuciare idrogeno.
so check with Misha about the turn off radius and average mass. 


### Animation demonstrating tidal foces

Here is a simulation of an isolated globular cluster. 
{{< youtube id="oIBfR6xnl4I" >}}
The white dots in these simulations are *star-particles*, which are massless points that represent stars. The exert no force on one another. Rather, all of these objects experience a central potential. 

{{< youtube id="Bxt-yz8ABIc" >}}
Here is a simulation of a globular cluster in a tidal field. The point of view is set from the center of the Galaxy. Star particles in this simulation feel a force from the Milky Way as well as the central potential of the globular cluster. This globular cluster that experiences tidal stripping gives rise to a stellar stream. 






## The motivation 
### Historical context

![oden](https://iopscience.iop.org/article/10.1086/378601/fulltext/fg2.h.gif?doi=10.1086/378601)
[Figure 2.](https://iopscience.iop.org/article/10.1086/378601/fulltext/203181.fg2.html?doi=10.1086/378601) Credit: Odenkirchen et al 2003. *THE EXTENDED TAILS OF PALOMAR 5: A 10° ARC OF GLOBULAR CLUSTER TIDAL DEBRIS*. The Astronomical Journal. 
![oden](https://iopscience.iop.org/article/10.1086/378601/fulltext/fg3.h.gif?doi=10.1086/378601)
[Figure 3.](https://iopscience.iop.org/article/10.1086/378601/fulltext/203181.fg3.html?doi=10.1086/378601) Credit: Odenkirchen et al 2003. *THE EXTENDED TAILS OF PALOMAR 5: A 10° ARC OF GLOBULAR CLUSTER TIDAL DEBRIS*. The Astronomical Journal. 

### Modern context: 
![IbataEtAl2021](https://cfn-live-content-bucket-iop-org.s3.amazonaws.com/journals/0004-637X/914/2/123/revision2/apjabfcc2f2_lr.jpg?AWSAccessKeyId=AKIAYDKQL6LTV7YY2HIK&Expires=1688033903&Signature=vEUuKpMjAGkMlzMdJl4jpSYQc8Y%3D) [Figure 2.](https://cfn-live-content-bucket-iop-org.s3.amazonaws.com/journals/0004-637X/914/2/123/revision2/apjabfcc2f2_lr.jpg?AWSAccessKeyId=AKIAYDKQL6LTV7YY2HIK&Expires=1688033903&Signature=vEUuKpMjAGkMlzMdJl4jpSYQc8Y%3D) Credit: Ibata et al 2021. *Charting the Galactic Acceleration Field. I. A Search for Stellar Streams with Gaia DR2 and EDR3 with Follow-up from ESPaDOnS and UVES.* The Astrophysical Journal, Volume 914, Issue 2, id.123, 22 pp.
![IbataEtAl2021](https://cfn-live-content-bucket-iop-org.s3.amazonaws.com/journals/0004-637X/914/2/123/revision2/apjabfcc2f3_lr.jpg?AWSAccessKeyId=AKIAYDKQL6LTV7YY2HIK&Expires=1688033903&Signature=ZBfa5aXWzwm8N6wu0VKgEdUhYOQ%3D) [Figure 3.](https://cfn-live-content-bucket-iop-org.s3.amazonaws.com/journals/0004-637X/914/2/123/revision2/apjabfcc2f3_lr.jpg?AWSAccessKeyId=AKIAYDKQL6LTV7YY2HIK&Expires=1688033903&Signature=ZBfa5aXWzwm8N6wu0VKgEdUhYOQ%3D) Credit: Ibata et al 2021. *Charting the Galactic Acceleration Field. I. A Search for Stellar Streams with Gaia DR2 and EDR3 with Follow-up from ESPaDOnS and UVES.* The Astrophysical Journal, Volume 914, Issue 2, id.123, 22 pp.


### How to interpret the stellar streams?

Are stellar streams good traces of GC orbits?
Fig. 1 and 3 from Montuori et al 2008

What about internal structure of the streams?
Clumpy streams in a smooth dark halo: the case of Palomar 5
FIG. 2 and 3 from Mastrobouno-Battisti et al 2018
Not a large difference with N body or not. 


### What are the use-cases for stellar streams?

There exists on going work of using stellar streams to extract information on the formation history of the Milky Way. One example, is the stream known as GD-1. This stream is observed to have *gaps*. It's thought that these gaps are due to the presence of dark matter sub-halos.


<font size="12"> Inference on the Galactic Potential </font>

We can look at the numerical simulation from Varghese et al 2011 as an example. 

Step (1) create a fiducial model using a self-consistent N-Body computation of a stellar stream in a series of different Galactic potentials.
![Varghese](https://oup.silverchair-cdn.com/oup/backfile/Content_public/Journal/mnras/417/1/10.1111/j.1365-2966.2011.19097.x/2/mnras0417-0198-f8.jpeg?Expires=1688037860&Signature=PxbelW8opZ7Z17jFuKTjmGwQ5nWSw2l0ao80blwkbjjwJY2Hc6kjMrBjx-q0wlMxibis9EMRzPmFhFBGd7RiHQGbWJpSaPVgR~TmJg1sLvTWMRmXkwe65WtjO2Wpybvh6pwLH8NplIu2ZKNmQvutoJ~wUHBbmmV0EIlplbaDvYmptxwOECVVGDnZ6cKTW5oI0fSpRxoZuC6pGesmkMuUNa0gIEwXTibOVYrD3a3MwAvUiY92w0Mv9sUCQP1RmMmYQ43yqBUGMZm3cjtupUNyq32-W~Bi3uh3URLPe-aaYvcyTNCWAUIlUIoyFJ8qW8JXv04rtU86WU3jGJh0WevCLA__&Key-Pair-Id=APKAIE5G5CRDK6RD3PGA)


Step (2) now reproduce the stream by following the progenitor orbit in the fiducial model, but using particle spray:
![VarhgeseFig9](https://oup.silverchair-cdn.com/oup/backfile/Content_public/Journal/mnras/417/1/10.1111/j.1365-2966.2011.19097.x/2/mnras0417-0198-f9.jpeg?Expires=1688037912&Signature=N1IEFwOUruwCozwu5UhtqMAWxga091NF4sbFsFXsPLHuuBCiRAtAP-s1Pk0C0rIPN73v4t7aeOPNCbOKCB1qYuIbPWMFhdKyurh3RKH9p2vFNH8ZAmbyFdOxJ5GTnpicbYH27DSPE7z0t-8qPw0JvfFVNA~RZgCBssbfIxchWrMRAkjHDgH8GFZ8B7FnuLtsf~R8juY8JFpATTpo2-bKu0ZuPbMT2x4X~cQlalaSQJTtoWFYbmdsLofuoWx5U2Sz7-BIRTK4-2pnm5uLfqr7D55bO6tL~GSChXi9lP2CWPpOmjK5ssdYD6C~kKTijfx9GzPQ0ZmkZ1t~K7sol3uYNA__&Key-Pair-Id=APKAIE5G5CRDK6RD3PGA)
Credit: [Varghese et al 2011](https://doi.org/10.1111/j.1365-2966.2011.19097.x) *Stellar streams as probes of dark halo mass and morphology: a Bayesian reconstruction*


Step (3) infer parameters of the potential
![VarhgeseFig9](https://oup.silverchair-cdn.com/oup/backfile/Content_public/Journal/mnras/417/1/10.1111/j.1365-2966.2011.19097.x/2/mnras0417-0198-f6.jpeg?Expires=1690462775&Signature=fKVGca-e4-4PrY0GavnJ10zn00fX3oQEcBlf8Zl0mM5OUUiDB8GJguMviS-Dx3zP99vucSU8Esi6641ELM0jKM6m80PWCirf2ll3KDV0gc5Javi9poS61s6f99-9tfP9KDrH3vx4EXMqdHfmfZ8t1tJGoek2vjwcGxzRHh4i70pa0UkqEx8iHMPGgMS1U2R0MVxqYf3Vx2ncdZpqdtc8f1bdL4pc0kutRN8kIUErURyeAPDszCAWI3NPPLeBGMcYKSsNC0VtfzgCEt-220u3nYtWpJF3crfzy-Ajj9~QumGNqk-LCbCeV7b-gNbzZOOCRLqgLUrUuASH7u1aZb1E6Q__&Key-Pair-Id=APKAIE5G5CRDK6RD3PGA
)





<font size="12"> Perturbations </font>

![Bonaca](https://cfn-live-content-bucket-iop-org.s3.amazonaws.com/journals/0004-637X/880/1/38/revision1/apjab2873f1_lr.jpg?AWSAccessKeyId=AKIAYDKQL6LTV7YY2HIK&Expires=1688042262&Signature=1WKmOlt5HZAR3gmOJ27w6VXvgvc%3D)
[Figure 1](https://cfn-live-content-bucket-iop-org.s3.amazonaws.com/journals/0004-637X/880/1/38/revision1/apjab2873f1_lr.jpg?AWSAccessKeyId=AKIAYDKQL6LTV7YY2HIK&Expires=1688042262&Signature=1WKmOlt5HZAR3gmOJ27w6VXvgvc%3D)
from [Ana Bonaca et al 2019 ApJ 880 38](https://iopscience.iop.org/article/10.3847/1538-4357/ab2873/meta)

<font size="12"> Accretion history of the Galaxy</font>


One example is from the work of Milhan et al 2019. The abstract states the following:

*Tidally disrupted globular cluster (GC) streams are usually observed, and therefore perceived, as narrow, linear, and one-dimensional structures in the 6D phase space. Here, we show that the GD-1 stellar stream, which is the tidal debris of a disrupted GC, possesses a secondary diffuse and extended stellar component (∼100 pc wide) around it, detected at the >5σ confidence level. Similar morphological properties are seen in synthetic streams that are produced from star clusters that are formed within dark matter sub-halos and then accrete onto a massive host galaxy. **This lends credence to the idea that the progenitor of the highly retrograde GD-1 stream was originally formed outside of the Milky Way in a now defunct dark satellite galaxy.** We deem that in future studies, this newly found cocoon component may serve as a structural hallmark to distinguish between the in situ and ex situ (accreted) formed GC streams.*


The authors highlights a series of different panels of the stars associated with the GD-1 stellar stream. The top panel shows the $L_z$ selection criteria used to eliminate false positives in the Gaia Data Release II catalogue. (b) shows the stars associated to the stream from their `STREAMFINDER` algorithm. (c) The same as (b) but now showing number density. (d) highlights some items of interest and the orbit of a neighboring stellar stream. 

![Malhan-2019](https://cfn-live-content-bucket-iop-org.s3.amazonaws.com/journals/0004-637X/881/2/106/revision1/apjab2e07f1_lr.jpg?AWSAccessKeyId=AKIAYDKQL6LTV7YY2HIK&Expires=1688040351&Signature=zLUc9%2FI9YX%2B3Z%2FnoPP%2FPg9AgRZg%3D)
[Figure 1.](https://cfn-live-content-bucket-iop-org.s3.amazonaws.com/journals/0004-637X/881/2/106/revision1/apjab2e07f1_lr.jpg?AWSAccessKeyId=AKIAYDKQL6LTV7YY2HIK&Expires=1688040351&Signature=zLUc9%2FI9YX%2B3Z%2FnoPP%2FPg9AgRZg%3D) Credit: Khyati Malhan et al 2019 ApJ 881 106. [DOI: 10.3847/1538-4357/ab2e07](https://iopscience.iop.org/article/10.3847/1538-4357/ab2e07)

Later in the article, the authors run some simulations of a globular cluster orbiting contained within a dark matter halo. The authors show that the stream is not only a linear feature, but also has a diffuse component.
![Malhan-2019](https://cfn-live-content-bucket-iop-org.s3.amazonaws.com/journals/0004-637X/881/2/106/revision1/apjab2e07f8_lr.jpg?AWSAccessKeyId=AKIAYDKQL6LTV7YY2HIK&Expires=1688040351&Signature=IiKACDlZCdNOptCOZOdLUknPduU%3D)
[Figure 1.](https://cfn-live-content-bucket-iop-org.s3.amazonaws.com/journals/0004-637X/881/2/106/revision1/apjab2e07f8_lr.jpg?AWSAccessKeyId=AKIAYDKQL6LTV7YY2HIK&Expires=1688040351&Signature=IiKACDlZCdNOptCOZOdLUknPduU%3D) Credit: Khyati Malhan et al 2019 ApJ 881 106. [DOI: 10.3847/1538-4357/ab2e07](https://iopscience.iop.org/article/10.3847/1538-4357/ab2e07)



## The project's goals
* To model the production of stellar streams from all Milky Way globular clusters
* Maybe we can discover more streams?

### Simulation showing many streams being made from many globular clusters
{{< youtube id="dvy6UapPvec" >}}

* This was published into an article in 2023.
    * The article is here: [Ferrone et al 2023. Astronomy and Astrophysics](https://www.aanda.org/articles/aa/full_html/2023/05/aa44141-22/aa44141-22.html)

## [Methods]({{< ref "/content/posts/Numerics/index.md" >}})


## Results
    Comparisons between different potentials
    Comparisons with different observations
    
## Propective 
    - how well does the stream match the orbit? 
    - which plots should we show?
    - more pertubers?



lo devo rendere molto accessibile senza degradare il messaggio e a EAS devo davvero sottolineare quello che avevo fatto e i nuovi risultati che ho ottenuto. 


[ok](https://www.aanda.org/articles/aa/full_html/2023/05/aa44141-22/F1.html)
### The QR Code to the data repository
![etidal-QR-code](/etidal-QR-code.png)

- advice make great propoganda for the use of the data
- website under construction, but it will be available soon
- add a jupyter notebook to show how to use the data
- open the data, show whats in there, and how to make some plots

