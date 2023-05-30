---
title: PhD Checkpoint Num. 1
author: Salvatore Ferrone
date: 2023-05-30
description: My comité de suivi de thèse.
toc: true
math: true
---
the lingue officielle is franglais. 

## PhD Checkpoint #1

To Dr. Gary Mamon and Dr. Françoise Combes, thank you for taking your time out to check in my progress. I hope that you will find my work satisfactory and can cretique it freely in the aims of forming a better scientist. To Dr. Paola Di Matteo, thank you for directing me and providing me with an opprotunity to make a valid contribution in astronomy. To Dr. Marco Montouri, I look forward to working together more closely when I arrive in Rome. I would also like to thank other professors and professionals who have helped such as Nicolas Lecleric, Rodrigo Ibata, and Vanessa Hill, Clément Hottier, Owain Snaith, Sergy Kohpersnov, Misha Haywood, and David Vallas Gaubaund. Additionally, I would like to thank the other junior researchers within and outside of our group such as Gulia Pagnini, Valeria Cerqui, Andre Saccardi, Jessie Palmerio, Laia Casa, and Sofia Bisero, Eliot Stien, and Antoine Fort. Lastly, Herminia de Oliveira Amorim. 

## Les courants stellaires pour l'archéologie galactique et cosmique : quand la gravité rencontre la complexité
(Stellar streams for Galactic and cosmic archaeology: when gravity meets complexity)

### Problematique (problem statement)
Avec ce projet de thèse, nous souhaitons 1) modeliser les courants stellaires autour de tous les amas globulaires de la Galaxie, en utilisant une variété de potentiels galactiques, incluant ou non les perturbations dues à la barre, aux nuages moléculaires géants, aux autres amas globulaires passant à proximité, et aux sous-structures de matière noire ; 2) développer et utiliser un ensemble de méthodes statistiques pour comparer les différentes simulations, en quantifiant les différences et les similitudes entre les caractéristiques des courants formés dans différents potentiels. Le but du projet est de caracteriser les signatures que de differentes structures visibles et de matière noire laissent dans la morfologie et cinématique des courants stellaires, pour pouvoir interpreter la grande quantité de nouvelles decouvertes faites en analysant les données de la mission astrometrique Gaia. Qu'est-ce-que les courants stellaires autour des amas globulaires peuvent nous reveler sur la distribution de la matière baryonique et de la matière noire dans notre Galaxie et sur leur granularité ?

![NGC](https://www.nasa.gov/sites/default/files/thumbnails/image/heic1321a.jpg)
Image of the Milky Way Globular Cluster NGC 7028 (M15) Credit: Credits: NASA, ESA

![streams](https://upload.wikimedia.org/wikipedia/commons/9/95/Sig07-008.jpg)
Credit: NASA/JPL-Caltech/R. Hurt (SSC/Caltech)




### Thématique 
Among the variety of systems found in our Galaxy, there are some, very old, which have been capturing the attention of astronomers for more than a century. These systems, which are called globular clusters because of their round shape, are collections of hundreds of thousands up to millions of stars, bound together by gravity. Globular clusters can be as old as the Universe itself (about 13.7 billion years), and as such they have been orbiting the Galaxy for several billion years, keeping key information about Galactic evolution through cosmic times.


### Domaine
One of the main processes affecting the globular cluster population, its evolution in number, masses and sizes with time, is tidal stripping. The long-term effect of this process consists of stripping the system of its most loosely bound stars, which redistribute themselves onto orbits similar to that of their progenitor, forming so-called ``tidal tails'' or streams around it.

### Objectif
The objective of the thesis is to:

1. build comprehensive catalogues of simulated stellar currents around globular clusters in a variety of Galactic potentials, including and excluding perturbations due to the bar, giant molecular clouds, other nearby globular clusters, and dark matter substructures;
2. develop and use a set of statistical methods to compare the different catalogues, quantifying the differences and similarities between the characteristics of the recovered currents in different potentials and their statistical significance, also taking into account the uncertainties in the knowledge of the current positions and velocities of globular clusters in the Milky Way.

A complete census of these stellar currents is currently lacking. However, this is a fundamental step, both to support the search for new streams in the data, and to quantify the extent to which different assumptions in the way we model the distribution of visible and dark matter mass can affect the properties of the overall system of stellar streams.

### Contexte
The context of this project is the study of our Galaxy, in the context of the ESA Gaia astrometric mission and the complementary spectroscopic surveys that will soon be operational (WEAVE, MOONS).

### Méthodologie
The aim will be to develop a set of numerical simulations of the formation of stellar streams in different galactic potentials and to use/develop the most appropriate statistical methods for their analysis. The numerical code for stellar stream simulations is already available in our group. This PhD project will allow the student to acquire a wide range of scientific knowledge and technical skills: from galactic dynamics, stellar populations and cosmology at Galactic scales to statistical methods for astrophysics; from the complete chain of the design, initialization and execution of large numerical simulations on national supercomputers to the most efficient ways of processing and analysing these data sets. Finally, we plan to make the simulations developed during this PhD project available to the community on a dedicated website. All this should ensure that the student is trained in a number of scientific and technical skills, which will be an asset for his future.


## Une année après d'avoir déposé la candidature

### What have I done? 
Zero-ith-ly, I have created this website in recent days in an attempt to share my science faster, more easily, such that I can always demonstrate my work to someone as long as there is internet!

First, two birds one stone, to add more context to the thesis as well as demonstrate a deliverable, I have create many animations and mastered a process to make them easily. Previously, I was using `Matplotlib`'s animation package. This is penible. Now I use `ffmpeg` which is much faster and easier and allows for much more control.

#### A Globular Cluster in a snow globe 
{{< youtube id="oIBfR6xnl4I" >}}

#### A Globular Cluster That Orbits a Galaxy
This is a simulation of Palomar 5, in the aims to be a demonstration of the growth of tidal tails. 1000 particles were used. These particles experience the potential from the Milky Way and a time-static Plummer Potential, as explained in the paper.

{{< youtube id="Bxt-yz8ABIc" >}}

#### Most of the Globular Clusters in the Milky Way
One globular cluster is pleasent, The same one in the Galaxy is cool, what about using about 100 globular clusters? This animation shows just that. It uses 1000 particles per GC, compared to 100,000 particles as in our paper. The POV is from the sun's position today. The center of the screen points towards the galactic center, the sides are behind us. Thus, this is galaxtic coordiantes. There is an element of depth in this presentation since I scaled the size particles by their distance from the sun. 

{{< youtube id="dvy6UapPvec" >}}


### Deliverables

#### Presentations and Publications

For a complete list, see this [page]({{< relref "/pages/Publications.md" >}}). 

Here is a table summarizing my presentation's since being accepted into the PhD:
   Title | Location   | Host | date
--------|------ |----- | -----
Simulating tidal debris production from all Galactic Globular Clusters | EAS Valencia, Spain | EAS | June 2022 
'' | l'observatoire de la côte d'azur | Vanessa Hill | 14 September 2022
'' | l'observatoire de Strasbourg | Rodrigo Ibata | 22 November 2022 
'' | Institute d'Astrophysique de Paris | Elbereth | 29 March 2023
[Detection of 4.3 Gyr Asteroid Family]({{< relref "/posts/ancient-asteroid-family/index.md" >}}) | l'observatoire de la côte d'azur | Benoît Carry | 25 May 2023


Regarding the publications, since begining the PhD I have published **two first authors papers and one co-author paper**. The co-author paper was an analysis of a recently discovered open cluster and was directed by the first author, Dr. Laia Casmiquela who is a part of the GEPI reserach team. I contributed our dynamical evolution models to explain how the tidal forces deformed the open cluster. The simulations are consistent with the observations. Some future papers are expected to be written, on which I will be a co-author. One of the work of Dr. Jules Boudelles De Micas, a former observatoire de paris PhD student and current post-doc, who is completing a spectroscopic analysis of the ancient asteroid family which was discovered and reported in my most recent paper. Next, senior researcher Dr. Rodrigo Ibata has invited Paola and I to contribute to his work on inferring the Galactic potential from orbits determined by recently discovered stellar streams. A precursor to this work can be seen in a previous article published by his team in 2011. They simulated inferring flattening parameters of Galactic dark matter halo's using stellar streams.

Step (1) create a fiducial model using a self-consistent nbody computation
![Varghese](https://oup.silverchair-cdn.com/oup/backfile/Content_public/Journal/mnras/417/1/10.1111/j.1365-2966.2011.19097.x/2/mnras0417-0198-f8.jpeg?Expires=1688037860&Signature=PxbelW8opZ7Z17jFuKTjmGwQ5nWSw2l0ao80blwkbjjwJY2Hc6kjMrBjx-q0wlMxibis9EMRzPmFhFBGd7RiHQGbWJpSaPVgR~TmJg1sLvTWMRmXkwe65WtjO2Wpybvh6pwLH8NplIu2ZKNmQvutoJ~wUHBbmmV0EIlplbaDvYmptxwOECVVGDnZ6cKTW5oI0fSpRxoZuC6pGesmkMuUNa0gIEwXTibOVYrD3a3MwAvUiY92w0Mv9sUCQP1RmMmYQ43yqBUGMZm3cjtupUNyq32-W~Bi3uh3URLPe-aaYvcyTNCWAUIlUIoyFJ8qW8JXv04rtU86WU3jGJh0WevCLA__&Key-Pair-Id=APKAIE5G5CRDK6RD3PGA)

Credit: [Varghese et al 2011](https://doi.org/10.1111/j.1365-2966.2011.19097.x) *Stellar streams as probes of dark halo mass and morphology: a Bayesian reconstruction*

Step (2) now reproduce the stream by following the progenitor orbit in the fiducial model, but using particle spray:
![VarhgeseFig9](https://oup.silverchair-cdn.com/oup/backfile/Content_public/Journal/mnras/417/1/10.1111/j.1365-2966.2011.19097.x/2/mnras0417-0198-f9.jpeg?Expires=1688037912&Signature=N1IEFwOUruwCozwu5UhtqMAWxga091NF4sbFsFXsPLHuuBCiRAtAP-s1Pk0C0rIPN73v4t7aeOPNCbOKCB1qYuIbPWMFhdKyurh3RKH9p2vFNH8ZAmbyFdOxJ5GTnpicbYH27DSPE7z0t-8qPw0JvfFVNA~RZgCBssbfIxchWrMRAkjHDgH8GFZ8B7FnuLtsf~R8juY8JFpATTpo2-bKu0ZuPbMT2x4X~cQlalaSQJTtoWFYbmdsLofuoWx5U2Sz7-BIRTK4-2pnm5uLfqr7D55bO6tL~GSChXi9lP2CWPpOmjK5ssdYD6C~kKTijfx9GzPQ0ZmkZ1t~K7sol3uYNA__&Key-Pair-Id=APKAIE5G5CRDK6RD3PGA)
Credit: [Varghese et al 2011](https://doi.org/10.1111/j.1365-2966.2011.19097.x) *Stellar streams as probes of dark halo mass and morphology: a Bayesian reconstruction*




### Our team's public data repository
*We are building a website from which anyone can download our simulations results*. The site is currently online at this domain: [https://etidal-project.obspm.fr/](https://etidal-project.obspm.fr/). However, it is not yet operational. We have a [https://etidal-dev.obspm.fr/](https://etidal-dev.obspm.fr/) that shows the intended functionality. It is only available if connected to the observatory's servers and if you have the correct credentials.

### MINI-PROJECTS
I want to make blogs of my work! There are three principal motivators: 
1. reading articles is difficult for me due to jargon and a lack of context. Annual or decade reviews help. But as a reader I would often times love someone to explain the literature in more details besides one sentence and a quick reference. So, I want to provide that with my work such that it's easier for a novice or a non-expert. 
2. I want these blogs to serve as the basis for my thesis. If I can start writing content now, and people can look at it, critize it, and I can improve it, then I will be in a better position to write my thesis.
3. Sometimes I learn things, and then I forget them. How easy would it be to relearn something if I had my own blog teaching my how to do something?

Here are some preliminary blogs that I have written that are currently in Jupyter notebooks:
- [Unit analysis](https://gitlab.obspm.fr/sferrone/integrate-plummer/-/blob/main/notebooks/units.ipynb). I had a hard time understanding galactic units. I couldn't understand why the masses in our paper were set to $2.32\times10^{7}$ solar masses. I didn't like this. I wanted to know why. So I wrote a blog about it.
- [Generating Plummer Initial Conditions](https://gitlab.obspm.fr/sferrone/integrate-plummer/-/blob/main/notebooks/generateInitCond.ipynb). I would like to run simulations of globular clusters that have a non-zero spin. While doing so, I realized that I didn't know how to generate the initial velocities of the particles on a deep level. I used this blog to work with the masters student and show him how its done as well. 

- [Failed block time-steps](https://gitlab.obspm.fr/sferrone/gc-tidal-loss/-/blob/development/simulations/analytic-GC-tidal-loss/notebooks/failedblock.ipynb). Here's an idea I had for reducing the number of computations necessary to simulate a globular cluster. I wanted to use a block time-step method. i.e. how can I integrate the inner particles with sufficient temporale resolution without wasting computation time on the outer particles? Briefly, block time-stepping is to give a class of particles the same time-step based on their dynamical times. The blocks $\delta t$'s need to be both multilpes of one another and factors of the total number of steps. In general, this leads to about a factor of four less computations. However, it was slower in the case of 100 particles with a speed up of 0.7. It was faster when using about 500 particles by a factor of 1.3. The program crashes when using a thousand particles. This showed me I have much to learn about high performance computing. I have left this on the side for a moment to not waste time over-optomizing the code if not necessary.

- **Using Galpy**. Upon publishing the paper on arkix, I got a message from someone suggesting me to use Galpy, a python library for galactic dynamics. I had never heard of it before. I was curious. Learning new code always requires a project and a deliverable. I wanted to see if I could reproduce the methods of varghese et al 2011. Namly, I wanted to use Galpy to do particle spray. This did not work. I still have issues. I limited it to some potential bugs, but I abandonded because it did not look fruitful. I summarized the functions that I needed in this [notebook](https://gitlab.obspm.fr/sferrone/stream-orbit-tracing/-/blob/main/report/galpy-ref.ipynb). The failed attempts to reconstruct the orbits using particle spray and Galpy can be found [here](https://gitlab.obspm.fr/sferrone/stream-orbit-tracing/-/blob/main/code/notebooks/reproduce-stream.ipynb). [Here is another one.](https://gitlab.obspm.fr/sferrone/stream-orbit-tracing/-/blob/main/code/notebooks/spray-scrap3.ipynb)


- [Stream-orbit systematic offset](https://gitlab.obspm.fr/sferrone/stream-orbit-tracing). This project for now is also a bit of a null result. We wanted to see if there were any systematic predictors of the mis-match between the stream and the orbit.  


## La Boule de Crystal: What does the future have in store?

### Future Presentations

   Title | Location   | Host | date
--------|------ |----- | -----

FILL IN TABLE OF SESTO, SPAIN, AND CRACOVIE

### Projects leading towards first author publication
Here are some porjects aiming towards publication 

1. MORE PERTURBATIONS
* overview of [code](https://gitlab.obspm.fr/sferrone/gc-tidal-loss)
- Currently re-writing the code to be more adaptable to different potentials and perturbations.

2. SIMULATING IMAGING OF THE STREAMS






## INTENDED FUTURE PROJECTED

- Adding context to infering progenitor orbits from streams
      - to do that, I looked to [Varghese et al 2010](https://doi.org/10.1111/j.1365-2966.2011.19097.x) as a guide and tried to reproduce their results.

Varghese's method for quick computational inference




## LOGISTICS

### COMPLETED COURSES (xx hr /total)

quelle est la volume horaire pour moi ! et aussi pour les autres étudiants parce que je suis 

   Title            | Professor | hours   | start date | end date
--------            |------     |----- |----- | -----
Bayesian Statistics | Benjamin wandelt      |  30  | 13 Mar 2023 | 11 May 2023
FLE B2 pour doctorants | Pauline Selinger   |  32  | 27 Oct 2022 | 16 Dec 2022
ethics | | | 
seasonal school? | | | 

combian des heures il me manque? combien des heures il me reste? est-ce qu'il y a des cous obligatoire pendents l'hiver ou l'été? est-ce que je peux le faire en italie? 

### CONTRIBUTIONS TO THE COMMUNITY 
AJOUTER DES PARTICIPATION à L'ESTABLISHMENT 
vie d'etablisement 
- Table Round en juin  
   - method pedagogique 
- Table round PSL en septembre 
   - PSL
- journal club 400000 persone par zoom viennent 
- journée de la science 

### FUTURE SUMMER SCHOOLS
- Maybe NASA's [Science Mission Design School](https://www.jpl.nasa.gov/edu/intern/apply/nasa-science-mission-design-schools/) for next year?
   - I wrote in my letters that I am supposed to bridge the gap between europe and the US, perhaps its time to start aiming towards that? I also like the idea of a career in mission design, I think I can handle the stress. 




