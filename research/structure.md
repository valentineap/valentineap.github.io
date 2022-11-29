---
title: Earth structure, properties and processes
layout: default
---

Much of my work has focussed on the Earth's large-scale structure and processes: what's happening inside the planet, and what drives the Earth system?

### Contents

- [Seismic tomography and earth structure](#seismic-tomography-and-earth-structure)
- [Earth materials](#earth-materials)
- [Geomorphology](#geomorphology)
- [Mantle convection](#mantle-convection)
- [Dynamic topography](#dynamic-topography)

[<i class="fas fa-square-caret-left" /> Back to research overview](/research.html)

---

### Seismic tomography and earth structure

My early work was focussed on seismic tomography: [understanding the tradeoffs](/files/Valentine2010a.pdf) between source and structure determination,[^1] and [proposing](/files/Valentine2010a.pdf) a new approach to data selection.[^2] It is notable that tomographic models produced by different research groups don't agree particularly well, and [I explored](/files/Valentine2016.pdf) how much of this could be attributed to the various arbitrary choices that tomographers must make when setting up their inversions.[^3] 

One of the major controversies about the Earth's interior is the question of whether observed heterogeneity is primarily due to compositional variations, or thermal variations. One route to addressing this lies in robustly imaging Earth's 3D density structure -- but this is difficult as it has only weak influence on surface observables. The most promising route is through analysis of normal mode splitting: the impact of earth structure on the eigenfrequencies of the planet. However, the computations required to do this are difficult, and we were able to [demonstrate](/files/Akbarashrafi2018.pdf) that the approaches being used in existing studies lacked sufficient numerical accuracy.[^4] 

Other work on earth structure includes [contributions](/files/Hejrani2020.pdf) to [Geoscience Australia's efforts](https://www.eftf.ga.gov.au/) to image the Australian continent,[^5] and exploration of machine learning for earth imaging, using [travel time](/files/Wit2013.pdf)[^6] and [normal mode](/files/Wit2014.pdf)[^7] datasets.

[<i class="fas fa-square-caret-up" /> Contents](#contents)<br/>

---

### Earth materials

![](/images/imelt_structure.png)

Temperatures and pressures inside the Earth far exceed anything that we can create in a laboratory setting. As a result, it is impossible to directly observe how materials behave under these conditions, and so we need to infer their properties from a combination of physical and chemical understanding, and whatever experimental information we *can* obtain. We have looked at how machine learning can contribute to this inference task. With Charles Le Losq, I attempted to [model the viscosity and other properties](/files/LeLosq2021.pdf) of molten glass[^8] -- you can explore some of the results using [this](https://share.streamlit.io/charlesll/i-melt/imelt_streamlit.py) online tool -- and we also worked on modeling [equations of state](/files/Rijal2021.pdf) for mantle minerals.[^9]

[<i class="fas fa-square-caret-up" /> Contents](#contents)<br/>

---

### Geomorphology

Earth surface processes are often driven (partly or wholly) by processes within the Earth, and so can provide useful constraints. However, cataloguing and analysing features is a time-consuming and tedious task. I developed a [machine-learning-based approach](/files/Valentine2013.pdf) that uses an autoencoder to assimilate the characteristics of the feature of interest -- in our case, seamounts, or underwater volcanoes.[^10] 

I also wrote a [brief introduction](/files/Valentine2016a.pdf) to machine learning, targetted at geomorphologists.[^11]

[<i class="fas fa-square-caret-up" /> Contents](#contents)<br/>

---

### Mantle convection

The present-day heterogeneity we image using tomography is the result of 4.5 billion years of processes occurring in the Earth's interior -- including mantle convection, or flow on long time-scales. We [explored](/files/Atkins2016.pdf) whether present-day tomographic images could help us constrain the history and time-dependent properties of convection.[^12]

[<i class="fas fa-square-caret-up" /> Contents](#contents)<br/>

---

### Dynamic topography
![](/images/map_high_accuracy_spot.png)

Few aspects of mantle convection are directly observable -- flow is far too slow to be imaged. One feature that can be observed is 'dynamic topography' -- uplift or downwelling of the Earth's surface caused by the forces imparted by flow. A number of studies had sought to analyse the available observations and determine the power spectrum of dynamic topography, which can then serve as a proxy for the power spectrum of the flow processes themselves. However, results were inconsistent and controversial, with many of the issues stemming from questions about regularisation. We were able to [address this](/files/Davies2019.pdf)[^13] using new [automatic regularisation](/files/Valentine2018.pdf)[^14] algorithms that I had developed. 

However, the automatic regularisation does not perform well for small datasets, which prevented us from analysing the data as completely as we hoped. To address this, I developed [a new strategy] based on Gaussian processes.[^14] We also wrote [a book chapter] summarising the state of the field.[^15]

[<i class="fas fa-square-caret-up" /> Contents](#contents)<br/>

---


### References

[^1]: Valentine & Woodhouse, 2010. Reducing errors in seismic tomography: Combined inversion for sources and structure. [doi:10.1111/j.1365-246X.2009.04452.x](https://doi.org/10.1111/j.1365-246X.2009.04452.x).
[^2]: Valentine & Woodhouse, 2010. Approaches to automatic data selection for global seismic tomography. [doi:10.1111/j.1365-246X.2010.04658.x](https://doi.org/10.1111/j.1365-246X.2010.04658.x)
[^3]: Valentine & Trampert, 2016. The impact of approximations and arbitrary choices on geophysical images. [doi:10.1093/gji/ggv440](https://doi.org/10.1093/gji/ggv440).
[^4]: Akbarashrafi, Al-Attar, Deuss, Trampert & Valentine, 2018. Exact free oscillation spectra, splitting functions and the resolvability of Earth's density structure. [doi:10.1093/gji/ggx539](https://doi.org/10.1093/gji/ggx539)
[^5]: Hejrani et al. 2020. Ambient noise tomography of Australia: application to AusArray deployment. [doi:10.11636/135130](https://doi.org/10.11636/135130)
[^6]: de Wit, Valentine & Trampert, 2014. Bayesian inference of Earth's radial seismic structure from body wave travel times using neural networks. [doi:10.1093/gji/ggt220](https://doi.org/10.1093/gji/ggt220)
[^7]: de Wit, Käufl, Valentine & Trampert, 2015. Bayesian inversion of free oscillations for Earth's radial (an)elastic structure. [doi:10.1016/j.pepi.2014.09.004](https://doi.org/10.1016/j.pepi.2014.09.004)
[^8]: Le Losq, Valentine, Mysen & Neuville, 2021. Structure and properties of alkali aluminosilicate glasses and melts: insights from deep learning. [doi:10.1016/j.gca.2021.08.023](10.1016/j.gca.2021.08.023)
[^9]: Rijal, Cobden, Trampert, Jackson & Valentine, 2021. Inferring material properties of the lower mantle minerals using mixture density networks. [doi:10.1016/j.pepi.2021.106784](https://doi.org/10.1016/j.pepi.2021.106784)
[^10]: Valentine, Kalnins & Trampert, 2013. Discovery and analysis of topographic features using learning algorithms: A seamount case-study. [doi:10.1002/grl.50615](https://doi.org/10.1002/grl.50615)
[^11]: Valentine & Kalnins, 2016. An introduction to learning algorithms and potential applications in geomorphometry and earth surface dynamics. [doi:10.5194/esurf-4-445-2016](https://doi.org/10.5194/esurf-4-445-2016)
[^12]: Atkins, Valentine, Tackley & Trampert, 2016. Using pattern recognition to infer parameters governing mantle convection. [doi:10.1016/j.pepi.2016.05.016](https://doi.org/10.1016/j.pepi.2016.05.016)
[^13]: Davies et al., 2019. Earth's multi-scale topographic response to global mantle flow. [doi:10.1038/s41561-019-0441-4](https://doi.org/10.1038/s41561-019-0441-4)
[^14]: Valentine & Sambridge, 2018. Optimal regularisation for a class of linear inverse problem. [doi:10.1093/gji/ggy303](https://doi.org/10.1093/gji/ggy303).
[^15]: Valentine & Davies, 2020. Global models from sparse data: A robust estimate of Earth's residual topography spectrum. [doi:10.1029/2020GC009240](https://doi.org/10.1029/2020GC009240)
[^16]: Davies, Ghelichkhan, Hoggard, Valentine & Richards, *in press*. Observations and models of dynamic topography: Current status and future directions.
[^17]: Enemark et al., 2019. Hydrogeological Bayesian hypothesis testing through trans-dimensional sampling of a stochastic water balance model. [doi:10.3390/w11071463](https://doi.org/10.3390/w11071463)
