---
title: Research 
layout: default
usemathjax: true
---

My research centres on **geophysical inversion and inference**: the mathematical ideas that allow us to understand the Earth's current state and its evolution across geological time, using the limited information that can be obtained from the Earth's surface and at the present day. I develop tools and techniques that allow us to address geoscience questions more robustly, by enabling better-targeted analysis, and by providing more rigorous constraint on the uncertainties and unknowns associated with results. 

![Progress in geophysical inversion]({{ site.home }}/images/prog.png)
*Progress in geophysical inversion, 1960s--present day. We need to move beyond Monte Carlo techniques to enable robust imaging in the most complex settings.*

As the above figure illustrates, efforts to characterise uncertainty in geophysical images have led to the current popularity of Monte Carlo-based techniques, which involve the creation and interrogation of a large 'ensemble' of candidate images that are all compatible with available data. However, such approaches are extremely computationally-expensive, and are only feasible for relatively modest-scale applications. To address big-picture geoscience questions---such as providing robust constraints on Earth's 3D structure, or its geodynamic history---something fundamentally new is required. A major focus of my work at present, and in the coming years, is the development of new techniques that enable direct inference for the probability distributions that characterise our knowledge about an imaging problem. The key insight is that probabilistic inference can be cast as an optimisation problem, avoiding computationally-prohibitive sampling schemes, and enabling a step change in our imaging capabilities.

This work draws heavily on current research from the fields of **statistics, data science and machine learning**, such as the concept of 'variational inference'. I have a long-standing interest in understanding how developments from these fields can be imported and applied within the geosciences. In some cases, this may be via a relatively direct application of machine learning techniques in combination with earth science datasets (e.g. [Valentine & Woodhouse, 2010](https://doi.org/10.1111/j.1365-246X.2010.04658.x)), but often it involves translation of mathematical ideas developed within the data science community to suit the particular needs and characteristics of a different context (e.g. [Valentine & Sambridge, 2018](https://doi.org/10.1093/gji/ggy303); [Valentine & Sambridge, 2020](https://doi.org/10.1093/gji/ggz520)).

Methodological development must be problem-driven, and I am always keen to advise, or collaborate with, colleagues from any field who seek new approaches to address their research questions. As such, I have worked on a broad range of topics over the course of my career, and I consider this breadth essential to the development of widely-applicable theory. Ongoing projects can be summarised under four general categories:

**Earthquake early warning** --- In conjunction with my PhD students at Utrecht, I developed the 'prior sampling' strategy for solving certain types of inference problem in a real-time environment ([Käufl *et al.*, 2016a](https://doi.org/10.1093/gji/ggw108)). Using this, we were able to carry out a proof-of-concept study for a physically-complete earthquake early warning system ([Käufl *et al.*, 2016b](https://doi.org/10.1002/2016GL069887)), allowing earthquake parameters to be determined within seconds of the first detection of shaking. However, for most practical applications, knowledge of the earthquake parameters is of secondary importance compared to knowledge of the anticipated ground shaking at some location(s) of interest. The next stage of this work is to extend the inference framework to enable direct prediction of such consequences from near-field data. This has potential to deliver a step change in the specificity of warnings that can be given, with significant impact on hazard mitigation in earthquake-prone areas.

**Resource exploration** -- Rapid, robust characterisation of the subsurface complete with quantification of uncertainty has immense commercial value for the resources industries. My work on novel probabilistic inference strategies has attracted interest and [investment from CSIRO](http://www.inlab.org.au). In a parallel with my earthquake early warning work, a particular focus is whether it is possible to directly infer particular pieces of target information---perhaps the size of an ore body---from observable data, without the need to construct a full 3D image of the subsurface. I anticipate a growing engagement with industry-facing applications in my research portfolio over the coming years.

**Normal mode seismology & earth structure** -- The free oscillations of the Earth, or normal modes, provide a probe of the planet's large-scale structure. In particular, they provide sensitivity to density variations within the Earth's interior, offering a route to determining whether heterogeneity is dominated by thermal or chemical effects. Additionally, the normal mode framework allows the calculation of synthetic seismic waveforms, with scaling properties that make it suited for efficient computation within probabilistic imaging. I am engaged in a long-term effort to develop theory and software tools that can enable accurate modelling of the free oscillations of the Earth and other planetary bodies (e.g. [Al-Attar *et al.*, 2018](https://doi.org/10.1093/gji/ggy141)). By combining these with my work on probabilistic imaging, I then aim to perform probabilistic global tomography, allowing a rigorous understanding of the current state of the mantle, and providing key constraints for the geodynamic modelling community.


**Inference in geodynamics** -- I have worked on a number of inference problems that arise from issues in geodynamics, ranging from cataloguing of seamounts ([Valentine *et al.*, 2013](https://doi.org/10.1002/grl.50615)) to efforts to constrain parameters governing the initiation and evolution of mantle convection ([Atkins *et al.*, 2016](https://doi.org/10.1016/j.pepi.2016.05.016)). Together with Rhodri Davies, I have addressed a recent controversy surrounding the spectrum of dynamic topography ([Davies *et al.*, 2019](https://doi.org/10.1038/s41561-019-0441-4); [Valentine & Davies, 2020](https://doi.org/10.1029/2020GC009240)), and we are beginning to develop capabilities for tackling 'inverse geodynamics' via adjoint simulations. I expect this work to be another growth area in my research profile for the coming years.