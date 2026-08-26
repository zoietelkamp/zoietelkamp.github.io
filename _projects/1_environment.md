---
layout: page
title: "The SOFIA Massive (SOMA) Star Formation Survey. V. Clustered Protostars"
# description: "[One-sentence summary of this project.]"
category: environment
importance: 1
# github: "[link to the sedcreator package on GitHub/PyPI]"
paper: "https://iopscience.iop.org/article/10.3847/1538-4357/adcd79"
press: "https://aasnova.org/2025/12/22/selections-from-2025-the-formation-of-massive-stars/"
press_label: "AAS Nova: Selections from 2025"
summary: >
  <p> This project utilized ~5–500 μm (Mid/Far-IR) data to investigate the <b>initial conditions</b> required for massive stars to form by examining protostars and their host environments on scales of ~10,000 au–1 parsec as part of the SOFIA Massive (SOMA) Star Formation Survey (<a href="https://iopscience.iop.org/article/10.3847/1538-4357/aa74c8">De Buizer et al. 2017</a>; <a href="https://ui.adsabs.harvard.edu/abs/2019ApJ...874...16L/abstract">Liu et al. 2019</a>, <a href="https://iopscience.iop.org/article/10.3847/1538-4357/abbefb">2020</a>; <a href="https://iopscience.iop.org/article/10.3847/1538-4357/aca4cf">Fedriani et al. 2022</a>; <a href="https://iopscience.iop.org/article/10.3847/1538-4357/adcd79">Telkamp et al. 2025</a>). The SOMA survey used the SOFIA-FORCAST instrument to observe a large sample of intermediate- and high-mass protostars across a wide range of environments and evolutionary stages to test predictions of massive star formation models. SOMA Paper V (Telkamp et al. 2025) investigated protostars forming in "clustered" environments. Using SOFIA-FORCAST observations in conjunction with archival Spitzer and Herschel data, we identified 34 protostars in 7 regions of clustered star formation and performed spectral energy distribution (SED) fitting to derive their properties. Synthesizing results from the entire SOMA survey of over 70 protostars across different environments, we found massive stars forming under diverse conditions, with no evidence that they require their environment to meet a minimum mass surface density ($\Sigma_{cl}$) threshold. This contradicts models that predict that massive stars, unlike their low-mass counterparts, require a minimum $\Sigma_{cl}$ to form.</p>

  <div class="project-figure-center">
    <img src="/al-folio/assets/img/G18.67.jpg" alt="Multiwavelength images of the massive protostellar region G18.67" style="max-width: 850px;" class="img-fluid rounded z-depth-1">
    <p class="caption">Multiwavelength images of the AFGL 5180 star-forming region with the facility and wavelength given in the upper right of each panel (Telkamp et al. 2025). Black plus signs represent the protostar positions, white circles represent the apertures used for photometry, and the color map indicates the relative flux intensity compared to that of the peak flux in each image panel.</p>
  </div>

  <div class="project-figure-right" style="width: 160px; text-align: center;">
    <img src="/al-folio/assets/img/sedcreator_logo.png" alt="A logo showing the word 'sedcreator' at the top of the circle, with a multicolored SED inside the circle" style="width: 100%;" class="img-fluid rounded z-depth-1">
    <p class="caption">sedcreator</p>
  </div>

  <p>As part of this work, I led the development of version 2.0 of <code>sedcreator</code> (Fedriani et al. 2022, Telkamp et al. 2025), an open-source Python package that automates the photometry and SED building and fitting process for large protostellar samples. Version 2.0 expanded <code>sedcreator</code>'s capabilities to simultaneously analyze any number of protostars in clustered regions, where contamination from neighboring sources must be accounted for.</p>

  <p>
  Telkamp et al. (2025) was featured in AAS Nova's Selections from 2025, a series highlighting some of the most-downloaded articles published in AAS journals that year.
  </p>
---
