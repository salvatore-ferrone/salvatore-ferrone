---
title: "Numerics"
date: 1996-06-15T17:29:22+02:00
draft: false
math: true
---

## Generation of the initial conditions


Inverse transform sampling 

## Treatment of the uncertainties 

Three main types of uncertainties:

1. Observational uncertainties 
2. Modeling uncertainties
3. Numerical uncertainties

### Observational uncertainties
From the Baumgart catalog, we have the following uncertainties:
- Line of sight velocities
- Distances
- Proper motions $\mu_{\alpha}$ and $\mu_{\delta}$
    - correlations between the proper motions
- Total mass

We also have quantities without reported uncertainties:
- RA
- DEC
- Half mass radius

MAKE AND SHOW THE CORNER PLOT FOR A COUPLE GCs
### Modeling uncertainties
Testing different models to see how the resultant stellar streams change is the main motivator of this study. We have a series of different models as well as modeling assumptions that we will test. For now, we have the following classes:
1. Treatment of the galactic potential
    -   See the dedicated section
2. Treatment of the internal dynamics of the globular cluster
    -   See the dedicated section on this topic
3. The galactic reference frame
    - for now we use XX by XX. However, this is a changeable parameter in the code and we are able to change it to any other galactic reference frame.

### Numerical error
The numerical error is the error that is introduced by the numerical integration of the equations of motion. We use a leap frog schema, that is sympletic and ensures the conservation of energy. However, the numerical error is still present. We investigate the numerical error by testing different time steps compared to the a characteristic time of the particle of interest. For now, we are using the crossing time as this metric for both the particles within a globular cluster and the globular clusters within the galactic potential. We employ the following tests to gauge our numerical error:
1. $ \Delta t $ - The time step. 
    - For the system of globular clusters, we integrate the all clusters with the same $\Delta t$, which is the $\Delta t$ required to correctly resolve the shortest crossing time of the system. Choosing the shortest timescale ensures that the system is correctly resolved for all clusters. Additionally, we opted to not use an individual time step per system. Although this would be better for data storage, it would require a more complex code to manage each cluster with its own temporal grid. Additionally, the GC orbits are not the most intensive data quantity to store, the positions of the particles are. However, when choosing the $\Delta t$ for the system, we must be careful to not choose a $\Delta t$ that is too small. This would result in a large number of time steps and a large amount of data to store. Additionally, the computational time would be very large. Therefore, we test various quotients of the crossing time, $\Delta t \propto [1,2^{-1},5^{-1},10^{-1},50^{-1},100^{-1},150^{-1},200^{-1},300^{-1}] \tau_{cross}$. With this list in mind, we try a series of different tests. We test the following:
        - Conservation of energy of an isolated cluster
        - The number of particles that escape the cluster
    - Of course, in an isolated system, energy is conserved. Thus, viewing energy conservation is an excellent metric. We allow the system to evolve for each time step and view the total energy, kinetic, and potential energy of each particle (be it the Globular Clusters or the star-particles). We track the RMS of the energy per time step and plot $\Delta E / E$ versus each $\Delta t$. We expect that the energy conservation will be better for smaller $\Delta t$. we choose a time step that has the energy conservation within $10^{-5}$.

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