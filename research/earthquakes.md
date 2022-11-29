---
title: Earthquakes
layout: default
---

To many people, 'seismology' means 'earthquakes'. Quite a bit of my work has focussed on how we can use seismic observables to obtain information about earthquakes, particularly in real-time settings for early warning.

### Contents

- [Centroid&ndash;moment-tensor inversion](#centroid–moment-tensor-inversion)
- [GPS seismology](#gps-seismology)
- [Earthquake Early Warning](#earthquake-early-warning)

[<i class="fas fa-square-caret-left" /> Back to research overview](/research.html)

---

### Centroid&ndash;moment-tensor inversion

In global seismology, earthquake mechanisms are usually described by a centroid&ndash;moment-tensor (CMT) representation, which assigns the earthquake to a single point in space and time, and provides information about the focal mechanism. CMT solutions are routinely calculated by (e.g.) the [Global CMT project](https://www.globalcmt.org), using a method based on the work of [Dziewonski, Chou and Woodhouse](https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/JB086iB04p02825). 

![](/images/cmt_mislocation.png)

In order to determine CMT solutions, one needs to know something about earth structure. However, in order to make models of earth structure, we must use CMT solutions as inputs for seismic simulations. This circularity can be problematic, and my [first paper](/files/Valentine2010.pdf) demonstrated that there is potential for tomographic models to acquire an imprint of the structure that was used to obtain the CMT solutions.[^1] Addressing this is not too difficult conceptually -- it requires simultaneous inversion for structure and all source information -- but implementing this is harder. I was able to develop efficient algorithms that embed an implicit source update within the structural inversion, at comparatively low cost. I also made [an attempt](/files/Valentine2012a.pdf) to quantify the true uncertainities on catalogue CMT parameters, taking the incompletely-known earth structure into account.[^2]

[<i class="fas fa-square-caret-up" /> Contents](#contents)<br/>

---

### GPS seismology

Traditional seismic instruments are accelerometers, recording very small motions of the Earth's surface. While accurate and sensitive, they can also present challenges: they tend to be delicate, expensive to run and maintain, and a relatively narrow sensitivity band -- an instrument designed to record distant earthquakes will be overwhelmed by the strength of ground shaking from nearby events. There was therefore considerable interest in how continuously-recording GPS stations could perform as seismometers, particularly for near-field monitoring of seismic zones. We [demonstrated](/files/OToole2012.pdf) that it is possible to obtain CMT solutions from GPS data,[^3] and [explored](/files/OToole2013.pdf) the feasibility of doing this in real-time settings.[^4]

[<i class="fas fa-square-caret-up" /> Contents](#contents)<br/>

---

### Earthquake early warning

![](/images/etew_schematic.png)


Real-time analysis is important because it enables earthquake early warning -- rapid analysis of the first seismic signals coming from an earthquake, so that alerts can be sent out ahead of the wavefront. A few seconds' warning is enough to take actions that mitigate the human and economic costs of the earthquake: machinery can be made safe, emergency generators can be started, and people can be warned to take cover. However, robust rapid analysis is a challenging problem. In particular, it is not feasible to run complex numerical simulations of wave propagation in the timeframe available. A number of studies had addressed this using approximate physics (sacrificing accuracy) or through vast pre-computed databases of synthetic seismograms. 

We saw an opportunity to apply [machine learning](/research/machinelearning.html) to the problem -- in particular, the [prior sampling](/research/priorsampling.html) technique that provides an efficient mechanism for storing and querying precomputed data. Paul Käufl systematically developed this concept, working up from [simple datasets](/files/Kaufl2014.pdf),[^5] through [more complex physics](/files/Kaufl2015.pdf),[^6] until he was able to demonstrate real-time earthquake early warning using [physically-complete modelling](/files/Kaufl2016a.pdf).[^7]

[<i class="fas fa-square-caret-up" /> Contents](#contents)<br/>
[<i class="fas fa-square-caret-left" /> Back to research overview](/research.html)


---

### References

[^1]: Valentine & Woodhouse, 2010. Reducing errors in seismic tomography: Combined inversion for sources and structure. [doi:10.1111/j.1365-246X.2009.04452.x](https://doi.org/10.1111/j.1365-246X.2009.04452.x).
[^2]: Valentine & Trampert, 2012. Assessing the uncertainties on seismic source parameters: Towards realistic error estimates for centroid-moment tensor determinations. [doi:10.1016/j.pepi.2012.08.003](https://doi.org/10.1016/j.pepi.2012.08.003)
[^3]: O'Toole, Valentine & Woodhouse, 2012. Centroid-moment tensor inversions using high-rate GPS waveforms. [doi:10.1111/j.1365-246X.2012.05608.x](https://doi.org/10.1111/j.1365-246X.2012.05608.x)
[^4]: O'Toole, Valentine & Woodhouse, 2013. Earthquake source parameters from GPS-measured static displacements with potential for real-time application. [doi:10.1029/2012GL054209](https://doi.org/10.1029/2012GL054209)
[^5]: Käufl, Valentine, O'Toole & Trampert, 2014. A framework for fast probabilistic centroid&ndash;moment-tensor determination &mdash; Inversion of regional static displacement measurements. [doi:10.1093/gji/ggt473](https://doi.org/10.1093/gji/ggt473)
[^6]: Käufl, Valentine, de Wit & Trampert, 2015. Robust and fast probabilistic source parameter estimation from near-field displacement waveforms using pattern recognition. [doi:10.1785/0120150010](https://doi.org/0.1785/0120150010)
[^7]: Käufl, Valentine & Trampert, 2016. Probabilistic point source inversion of strong-motion data in 3D media using pattern recognition: A case study for the 2008 Mw5.4 Chino Hills earthquake. [doi:10.1002/2016GL069887](https://doi.org/10.1002/2016GL069887)
