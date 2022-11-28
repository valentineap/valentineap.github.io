---
title: Numerical modelling
layout: default
---

### Contents

- [pyprop8](#pyprop8)

[<i class="fas fa-square-caret-left" /> Back to research overview](/research.html)

### pyprop8
Most packages that have been developed to perform simulations of seismic wave propagation have been designed with the research community in mind, and installation and use tend to come with steep learning curves. This makes them poorly-suited to use in teaching and outreach settings, as technical issues create barriers to engagement. To circumvent these problems, I developed the `pyprop8` Python package, which enables seismogram synthesis and depends on only two mainstream libraries: `numpy` and `scipy`. Installation is as simple as `pip install pyprop8`, and the package can simulate static offset, waveform and InSAR data in a layered half-space, and also compute derivatives of observables with respect to seismic source parameters.

<video controls width="100%">
    <source src="/files/idaho2.mp4"
            type="video/mp4" autoplay muted preload="auto" loop>
    Sorry, your browser doesn't support embedded videos.
</video>
*Seismic wave propagation simulated using pyprop8*

The code is available [on Github](https://github.com/valentineap/pyprop8), along with [full documentation](https://pyprop8.readthedocs.io) and [a short paper](/files/Valentine2022.pdf) announcing the package.[^1] It is based on theory described in papers by [O'Toole and Woodhouse](https://academic.oup.com/gji/article/187/3/1516/616302) and [O'Toole et al](https://academic.oup.com/gji/article/191/1/257/586793).[^2] There's also an [online demo](https://mybinder.org/v2/gh/valentineap/pyprop8/HEAD?labpath=examples%2Fdemo.ipynb)!


[<i class="fas fa-square-caret-up" /> Contents](#contents)<br/>
[<i class="fas fa-square-caret-left" /> Back to research overview](/research.html)


---

### References
[^1]: Valentine & Sambridge, 2022. pyprop8: A lightweight code to simulate seismic observables in a layered half-space. [doi:10.21105/joss.04217](https://doi.org/10.21105/joss.04217)
[^2]: O'Toole, Valentine & Woodhouse, 2012. Centroid-moment tensor inversions using high-rate GPS waveforms. [doi:10.1111/j.1365-246X.2012.05608.x](https://doi.org/10.1111/j.1365-246X.2012.05608.x)
