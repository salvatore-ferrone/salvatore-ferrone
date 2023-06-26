---
title: "Numerical methods"
date: 1996-06-15T17:29:22+02:00
draft: false
math: true
---

I believe the best way to discuss the methods used to in this numerical simulation is to introduce the concepts through the treatment of the uncertainties. 
## Treatment of the uncertainties 

Three main types of uncertainties:

1. Observational uncertainties 
2. Modeling uncertainties
3. Numerical uncertainties

Since we are trying to reproduce observations, we can define three levels of uncertainty. First, are the observational uncertainties on the globular cluster's that we are using as the starting point. Secondly, we have the modeling uncertainty, which is a bit different from the observational uncertainty in concept because the sensitivity of reproducing stellar streams to different models *are principal* results. Nonetheless, we discuss them here. Lastly, we have numerical uncertainty, these uncertainties are introduce from the choice of numerical methods from solving Newton's equations for the motions of our particles. 


### Observational uncertainties
Baumgardt et al have provided two catalogs that we use on a dedicated website. The have a [kinematic catalog](https://people.smp.uq.edu.au/HolgerBaumgardt/globular/orbits.html) of the globular clusters, as well as a catalog describing the [internal structure](https://people.smp.uq.edu.au/HolgerBaumgardt/globular/parameter.html) of the globular clusters. In our study, thus far, we need to know the six dimensional phase space information for as many of the galactic globular clusters possible, as well as a measure of their mass and size. Thus, we use eight quantities. Of these, we have uncertainties for 
- $V_{los}$: the line of sight velocities
- $D$: Distances
- $\mu_{\alpha}\cos\left(\delta\right), \mu_{\delta}$: the proper motions. Additionally, these uncertainties are often have a negligible correlation coefficient $\rho_{\mu_{\alpha},\mu_{\delta}}$. We take these correlations into account.

Regarding the remaining three, we do not have uncertainties on the Right Ascension (RA) nor the Declination (DEC) nor the half mass radii ($r_{hm}$). The uncertainties on the RA and DEC must be so much smaller than the other quantities that their treatment are not worth while (oui?). The half mass radii result from N-body fitting to the clusters and is discussed in Baumgardt 2017 and Baumgardt & Hiker 2018. Their methods return a best value without uncertainty? (pas compris encore pourquoi. je dois re-étudier ces articles. à verifier?). 


The the reported uncertainties, we sample the initial conditions monte-carlo style. These are shown in the plot below using N=20 iterations. To do so, we create a co-variance matrix. We assume gaussian uncertainties where the reported uncertainties are one sigma, thus the diagonal elements of this co-variance matrix are the uncertainties squared. Additionally, the only non-zero off-diagonal element in this matrix is the covariance term between the proper motions. The co-variance is related to the correlation coefficient by:

$$\sigma_{\mu_{\alpha},\mu_{\delta}}^2=\rho_{\mu_{\alpha},\mu_{\delta}}\sigma_{\mu_{\alpha}}\sigma_{\mu_{\delta}}$$

With this, we then use `numpy.random.multivariate_normal`, passing the best value's reported in the Baumgardt catalog's as the mean and the constructed co-variance matrix, to randomly generate initial conditions. After, we store the initial conditions for each iteration in `HDF5` files. To verify the generation of the initial conditions, we refer to the plot below.
![cornerplot](/lynga7cornerplot.png)
Credit: Ferrone. In this corner plot, we show the 20 generated initial conditions from the globular cluster Lynga 7. The reported uncertainties are used to color the circles/ellipse. The radii of each correspond to 2$\sigma$ of the respective uncertainty. The blue ellipse was colored different to demonstrate that the correlation between the proper motions was taken into account, where the green circles demonstrate that the quantities are assumed independent. Additionally, the mean value's are labeled with red x's. Thus, The ellipses and red x's highlight the initial conditions that are stored in one data file. On the other hand, the black dots are the generated initial conditions that are stored else where. Since they are centered about the mean and most points fall within 2-sigma of the mean, we know that the initial conditions were sampled from the distribution correctly. 

#### Transformation into galacto-centric coordaintes

To give a quick peak ahead and show what effect this sampling of the uncertainties can have, I present the following two plots, despite the fact that the integration methods nor modeling assumptions are yet to be presented. Below, we show 20 orbits of the Palomar 5 in the Pouliasis et al 2017 PII model. 
![Pal5Orbits](/Pal5_pouliasis2017pii_ts_Rs.png)
![Pal5Orbits](/Pal5_pouliasis2017pii_Rs_vRs.png)
Credit: Ferrone. The top plot shows the cylindrical radius versus time. Each unit of time is nearly a Giga-year, although the time is actually reported in units of kpc/km/s (which is about 0.97 Gyrs). The bottom plot shows two phase-space coordinates versus, the cylindrical radius versus the 2D radial velocity. Each plot includes a different amount of time. The top plot present the orbit for seven crossing time, while the bottom was truncated to three for clarity. The colors are presented to distinguish between the monte-carlo realizations. `matplotlib's` rainbow color palette was used, with red being given to the most distance cylindrical radius and blue assigned to the nearest cylindrical radius to the galactic center. 

### Modeling uncertainties
Testing different models to see how the resultant stellar streams change is the main motivator of this study. We have a series of different models as well as modeling assumptions that we will test. For now, we have the following classes:
1. Treatment of the galactic potential
    -   See the dedicated section
2. Treatment of the internal dynamics of the globular cluster
    -   See the dedicated section on this topic
3. The galactic reference frame
    - for now we use XX by XX. However, this is a changeable parameter in the code and we are able to change it to any other galactic reference frame.


#### Galactic potential models
    - Pouliasis et al. Model I (buldge, disk, halo)
    - Pouliasis et al. Model II (disk + disk + halo)
    - Pouliasis et al. Model II plus BAR ( disk + disk + halo + bar)


![pouliasis-2017-fig-6.png](/pouliasis-2017-fig-6.png)
![pouliasis2017pii](/pouliasis-2016-fig4.png)
![pouliasis-2017-fig-3.png](/pouliasis-2017-fig-3.png)
Credit: [Pouliasis et al. A&A 598 A66 (2017)](https://www.aanda.org/articles/aa/abs/2017/02/aa27346-15/aa27346-15.html). Three figures presenting different aspects of the galactic potential models we used in our analysis. The first shows the observational constraints, i.e. the rotations curves taken from two different analysis of motion in the Galaxy. Next, we see color maps of the stellar density and the potential. The last panel shows that the potentials are linear sums of different parts, disks, a bulge, and a halo


##### PII modified to include a stellar bar
So far, we have employed one model of the galactic environment with a time-varying component, a stellar bar. We create the bar, we modified the PII model by decreasing 30 percent of the thin+thick disk mass and allocating it to the bar. This bar uses a pattern speed of 38 km s$^{-1}$ kpc^{-1}, which is regarded as a slower speed. The potential of this bar uses a [Long and Murali (1992)](https://adsabs.harvard.edu/full/1992ApJ...397...44L) tri-axel model:

$$\Phi_{bar}(x,y,z) = \frac{GM_{bar}}{2a_{bar}}\ln\left(\frac{x-a_{bar}+T_{-}}{x+a_{bar}+T_{-}}\right),$$

where

$$ T_{\pm} = \left[ \left(a_{bar}\pm x\right)^2 +y^2 + \left(b_{bar} + \sqrt{c^2_{bar} + z^2} \right)^2 \right] $$

and $a_{bar}$, $b_{bar}$, and $c_{bar}$ are the characteristic lengths along the bar's principal axes. The advantage of using this model is that the Plummer model and the Miyamoto & Nagai can be recovered. 

The Miyamoto & Nagai potential is:

$$\Phi_{disk}(R,z) = \frac{GM_{disk}}{\left(R^2 + \left[a_{disk} + \sqrt{z^2+b_{disk}^2}\right]^2\right)^{1/2}}$$


The Plummer potential is this:
$$\Phi_{plummer}(r) = \frac{GM_{plummer}}{\left(r^2 + a_{plummer}^2\right)^{1/2}}$$


#### Internal dynamics 
The production of stellar streams is not only dependent on the gravitational field of the Galaxy, but also the host globular cluster from which the stars depart. The difficulty arising from treatment of the Globular Cluster internal dynamics is that the density is quite high on the inside, leading to a highly collisional environment. On the other hand, the density on the peripheries is quite low. We opt for a simple treatment of the Globular Cluster's internal dynamics to get a hand on the first order expectation of stellar streams originating from the Galactic Globular Clusters. Specifically, we model the globular clusters as iso-tropic plummer spheres. This means we use a spherical symmetric mass distribution, which is dependent on two parameters, the total mass and the scale length. Next, *isotropic* means that at any given position, there is no preference for the direction of the velocity vector. We generate these positions using inverse transform sampling. 



Internal dynamics summary:
    
    - Plummer sphere
    - Isotropic (no net rotation nor anisotropy)
    - 100,000 particles per cluster
    - massless particles

Future improvements:

Of course, we would like to add more accurate physics to improve  the internal dynamics. I envision improving this first exploring the parameter space horizontally and then pushing deeper by adding high order effects. The first step would be to try different potential models, such as an iso-crone, king model, etc. Then, we would try to implement anisotropies. After exhausting potential models, which is has $\mathcal{O}(n)$ computational complexity, we could move towards complex codes to properly treat the phenomena such as: *mass segregation*, *binary stars*, *black holes*, etc. 

    - Different potential models 
    - non-isotropic internal dynamics
    - collisional treatment of the interior. 


### Integration and Numerical error

To solve for the motion of our star particles, we integrator the equations of motion governed by Newtonian's mechanics. Thus, we do not have an analytical solution. Solving the equations numerical introduces numerical errors, and thus the subjects are intimately linked and discuss both here. 


To solve the equations of motion, we  use a Leap Frog schema. It's name is derived for the children's game in which child A squats while child B leaps over them, like a frog, and subsequently squats waiting for child A to leap over child B. The children subsequently alternate between squatting and jumping until they start doing something else. It is this alternation that provides the analogy to the children's game. In this integration schema, we solve for the motion in two steps. The first is to update the positions, then we compute the accelerations acting on the particles, after which we average the updated acceleration with the previous acceleration to then update the velocity. Schematically, the Leap Frog Schema looks like this. 

$$\vec{a}_i=F\left(\vec{x}_i\right)$$

$$ \vec{x_{i+1}}= \vec{x_{i}} + \vec{v_i}\delta t + \frac{1}{2}\vec{a_i}\delta t^2$$

$$\vec{a_{i+1}}=F\left(\vec{x}_{i+1}\right)$$

$$ \vec{v}_{i+1} =  \vec{v_i} + \frac{1}{2}\left(\vec{a_i}+\vec{a}_i \right)\delta t$$

*NOTE* error in markdown. Sometimes it won't register the subscripts correctly. Not sure why. The last equation should be $\frac{1}{2}\left(\vec{a_i}+\vec{a}_{i+1} \right)$. à verifier. Maybe there's a bug when using the vector hat. 

This sequence is then repeated for as many time steps required to arrive to the end. In more technical terms, it is said that the integrator is *sympletic* and ensures the conservation of energy. However, the numerical error is still present. We investigate the numerical error by testing different time steps compared to the a characteristic time of the particle of interest. For now, we are using the crossing time as this metric for both the particles within a globular cluster and the globular clusters within the galactic potential. We employ the following tests to gauge our numerical error:
1. $ \Delta t $ - The time step. 
    - For the system of globular clusters, we integrate the all clusters with the same $\Delta t$, which is the $\Delta t$ required to correctly resolve the shortest crossing time of the system. Choosing the shortest timescale ensures that the system is correctly resolved for all clusters. Additionally, we opted to not use an individual time step per system. Although this would be better for data storage, it would require a more complex code to manage each cluster with its own temporal grid. Additionally, the GC orbits are not the most intensive data quantity to store, the positions of the particles are. However, when choosing the $\Delta t$ for the system, we must be careful to not choose a $\Delta t$ that is too small. This would result in a large number of time steps and a large amount of data to store. Additionally, the computational time would be very large. Therefore, we test various quotients of the crossing time, $\Delta t \propto [1,2^{-1},5^{-1},10^{-1},50^{-1},100^{-1},150^{-1},200^{-1},300^{-1}] \tau_{cross}$. With this list in mind, we try a series of different tests. We test the following:
        - Conservation of energy of an isolated cluster
        - The number of particles that escape the cluster
    - Of course, in an isolated system, energy is conserved. Thus, viewing energy conservation is an excellent metric. We allow the system to evolve for each time step and view the total energy, kinetic, and potential energy of each particle (be it the Globular Clusters or the star-particles). We track the RMS of the energy per time step and plot $\Delta E / E$ versus each $\Delta t$. We expect that the energy conservation will be better for smaller $\Delta t$. we choose a time step that has the energy conservation within $10^{-5}$.


[Numerical Error Table](https://www.aanda.org/articles/aa/full_html/2023/05/aa44141-22/T4.html)


PLOT E/\<E\> VERSUS T FOR MANY GCS WITH ONE DT. SHOW A FEW VERSIONS OF THIS PLOT FOR DIFFERENT DTs

PLOT $\sigma_{E}/$\<E\> VERSUS DT FOR MANY GCS

PLOT E/\<E\> VERSUS T FOR MANY GCS WITH ONE DT. DO A DENSE AND A SPARSE CLUSTER

PLOT $\sigma_{E}/$\<E\> VERSUS DT FOR THE PARTICLES



## Numerical integration

- leap frog
    - sympletic integrator
        - this essentially means that the energy is conserved, which ensures the long term stability of the orbit. This is favorable to the use of a Runge-Kutta integrator, which is not sympletic and is not stable over long time scales.
- Fortran and f2py
    - And object oriented approach to the code
    - All data management is done in python
    - All numerical integration is done in Fortran
    - Optional forces for each particle
        - Static galaxy
            - multiple galactic potential models
        - Dynamic elements
            - NBODY
            - perturbers
            - Galactic bar