---
layout: post
date: 2016-08-29 09:00:00 +1000
title: Probabilistic point source inversion of strong-motion data in 3-D media using pattern recognition
---
The final paper to come from Paul Käufl's PhD thesis [has just been published in Geophysical Research Letters](https://doi.org/10.1002/2016GL069887). In it, he demonstrates how prior sampling can be used to implement earthquake early warning within a probabilistic framework, while properly incorporating all the complexities of wave propagation in realistic heterogenenous crustal structures.

These local crustal structures, and surface topography, can affect seismograms quite considerably. However, complete waveform modelling is extremely computationally expensive (perhaps 100 CPU-hours/earthquake for the frequency- and time-scales used in this paper). Thus, most earthqake early warning applications have been forced to adopt faster, approximate methods that neglect some or all of these effects. However, the prior sampling framework allows us to perform all these expensive calculations in advance. Then, once an earthquake occurs, we can recover probabilistic models for the seismic source---within milliseconds of the relevant data becoming available. Properly accounting for all of the complexities within the waveforms reduces the uncertainties associated with the results, permitting more robust early warning schemes.

Here's the abstract:
> Despite the ever increasing availability of computational power, real-time source inversions based on physical modeling of wave propagation in realistic media remain challenging. We investigate how a nonlinear Bayesian approach based on pattern recognition and synthetic 3-D Green's functions can be used to rapidly invert strong-motion data for point source parameters by means of a case study for a fault system in the Los Angeles Basin. The probabilistic inverse mapping is represented in compact form by a neural network which yields probability distributions over source parameters. It can therefore be evaluated rapidly and with very moderate CPU and memory requirements. We present a simulated real-time inversion of data for the 2008 Mw 5.4 Chino Hills event. Initial estimates of epicentral location and magnitude are available ∼14 s after origin time. The estimate can be refined as more data arrive: by ∼40 s, fault strike and source depth can also be determined with relatively high certainty.

You can also download Paul's complete PhD thesis [from the Utrecht thesis repository](http://dspace.library.uu.nl/handle/1874/321502).

