---
title: Prior Sampling
layout: default
---

How can you use [machine learning](/research/machinelearning.html) to solve [inverse problems](/research/inversetheory.md)? Prior sampling offers one solution: generate many candidate models (sampling from the prior); run a simulation for each to predict the corresponding observations; and then assimilate all this information using some kind of machine learning algorithm that can then be applied predictively to real data.

### Contents

- [Background](#background)
- [Applications](#applications)
    - [Earthquake early warning](#earthquake-early-warning)
    - [Earth's radial seismic structure](#earths-radial-seismic-structure)
    - [Global geodynamics](#global-geodynamics)
    - [Mineral physics](#mineral-physics)

[<i class="fas fa-square-caret-left" /> Back to research overview](/research.html)


### Background

There is a long history of studies that have sought to apply machine learning to (geophysical) inverse problems. Early milestones include the works of [Roth & Tarantola](https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/93JB01563) in 1994, and [Devilee, Curtis & Roy Chowdhury](https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/1999JB900273) in 1999. Then in 2007, [Meier, Curtis & Trampert](https://academic.oup.com/gji/article/169/2/706/2012014) demonstrated geophysical inversion using a Mixture Density Network (MDN) -- a framework proposed by [Bishop](https://global.oup.com/academic/product/neural-networks-for-pattern-recognition-9780198538646) where the outputs of a simple neural network are treated as the parameters for a Gaussian mixture model (GMM): in effect, the network outputs an entire probability density function. 

<center>
<img src="/images/gmm.png" alt="Gaussian Mixture Model" width="500"/>
</center>
*A three-component Gaussian mixture model.*

In Meier et al.'s formulation, observed data are input to the neural network and an approximate posterior marginal distribution for each model parameter comes out. We picked up this work, exploring a number of different [applications](#applications), and seeking to better-understand its theoretical basis. This is set out in detail in [a paper](/files/Kaufl2016.pdf) written by Paul Käufl, which shows that the MDN-learned posteriors are exact in the limit of an exhaustive training set and infinite-capacity neural network.[^1]

I wrote a Fortran(!) package implementating the MDN framework, which is [available here](https://github.com/valentineap/mixture-density-network).

[<i class="fas fa-square-caret-up" /> Contents](#contents)<br/>

---

### Applications

We have applied the MDN approach to a variety of problems:

#### Earthquake early warning

<center>
<img src="/images/chino_hills_wavefield.png" alt="Chino Hills wavefield" width="500"/>
</center>

Paul Käufl's [PhD thesis](https://dspace.library.uu.nl/bitstream/handle/1874/321502/kaufl.pdf) focussed on the potential of MDNs for rapid earthquake location and characterisation. We started with a comparatively simple class of data, and added complexity as we gained experience:
1. [Static displacement observations](/files/Kaufl2014.pdf) -- two-component vectors at each site.[^2]
2. [Simple waveforms](/files/Kaufl2015.pdf) within a 1D earth model.[^3]
3. [Physically-complete waveforms](/files/Kaufl2016a.pdf) using [SPECFEM3D](https://github.com/SPECFEM/specfem3d) and a [complex crustal model](https://www.science.org/doi/10.1126/science.1175298) for Southern California.[^4]

The last of these provides a convincing proof-of-concept for the feasibility of real-time earthquake early warning using physically-complete (computationally very expensive!) numerical modelling.

#### Earth's radial seismic structure

Ralph de Wit's [PhD thesis](https://dspace.library.uu.nl/bitstream/handle/1874/315583/dewit.pdf) focussed on a different seismological application: performing inference for the physical properties of the Earth as a function of depth. Again, we explored performance across different data sets:
1. [Travel times](/files/Wit2013.pdf) for body waves.[^5]
2. [Eigenfrequencies](/files/Wit2014.pdf) for specific normal modes of the Earth.[^6]

#### Global geodynamics

Suzanne Atkin's [PhD thesis](http://dspace.library.uu.nl/bitstream/handle/1874/349108/Atkins.pdf) looked at geodynamics, and whether MDNs could be used to infer thermochemical properties of the Earth from tomographic images. This is a challenging problem, with substantial computational difficulties, but we had [some success](/files/Atkins2016.pdf).[^7]

#### Mineral physics

Ashim Rijal has used the MDN framework to [model equations of state] for lower mantle minerals.[^8]



[<i class="fas fa-square-caret-up" /> Contents](#contents)<br/>
[<i class="fas fa-square-caret-left" /> Back to research overview](/research.html)

---

### References
[^1]: Käufl, Valentine, de Wit & Trampert, 2016. Solving probabilistic inverse problems rapidly with prior samples. [doi:10.1093/gji/ggw108](https://doi.org/10.1093/gji/ggw108)
[^2]: Käufl, Valentine, O'Toole & Trampert, 2014. A framework for fast probabilistic centroid&ndash;moment-tensor determination &mdash; Inversion of regional static displacement measurements. [doi:10.1093/gji/ggt473](https://doi.org/10.1093/gji/ggt473)
[^3]: Käufl, Valentine, de Wit & Trampert, 2015. Robust and fast probabilistic source parameter estimation from near-field displacement waveforms using pattern recognition. [doi:10.1785/0120150010](https://doi.org/0.1785/0120150010)
[^4]: Käufl, Valentine & Trampert, 2016. Probabilistic point source inversion of strong-motion data in 3D media using pattern recognition: A case study for the 2008 Mw5.4 Chino Hills earthquake. [doi:10.1002/2016GL069887](https://doi.org/10.1002/2016GL069887)
[^5]: de Wit, Valentine & Trampert, 2014. Bayesian inference of Earth's radial seismic structure from body wave travel times using neural networks. [doi:10.1093/gji/ggt220](https://doi.org/10.1093/gji/ggt220)
[^6]: de Wit, Käufl, Valentine & Trampert, 2015. Bayesian inversion of free oscillations for Earth's radial (an)elastic structure. [doi:10.1016/j.pepi.2014.09.004](https://doi.org/10.1016/j.pepi.2014.09.004)
[^7]: Atkins, Valentine, Tackley & Trampert, 2016. Using pattern recognition to infer parameters governing mantle convection. [doi:10.1016/j.pepi.2016.05.016](https://doi.org/10.1016/j.pepi.2016.05.016)
[^8]: Rijal, Cobden, Trampert, Jackson & Valentine, 2021. Inferring material properties of the lower mantle minerals using mixture density networks. [doi:10.1016/j.pepi.2021.106784](https://doi.org/10.1016/j.pepi.2021.106784)