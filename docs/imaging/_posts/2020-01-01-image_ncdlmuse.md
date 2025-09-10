---
title: "NiChart_DLMUSE"
excerpt: "NiChart_DLMUSE"
layout: single

---

<style>
details p { margin: 8px 0 !important; }
details div { line-height: 1.6; }
</style>

<br>
<div style="margin: 10px 0;">
<strong>Citation</strong><br/>
Doshi, Jimit, Guray Erus, Yangming Ou, Susan M Resnick, Ruben C Gur, Raquel E Gur, Theodore D Satterthwaite, Susan Furth, Christos Davatzikos, and Alzheimer’s Neuroimaging Initiative. 2016. “MUSE: MUlti-Atlas Region Segmentation Utilizing Ensembles of Registration Algorithms and Parameters, and Locally Optimal Atlas Selection.” NeuroImage 127: 186–95. https://doi.org/10.1016/j.neuroimage.2015.11.073.
</div>

<br>
[**NiChart_DLMUSE**](https://github.com/CBICA/NiChart_DLMUSE) performs deep-learning based brain extraction and segmentation on T1-weighted images. This is based on the MUSE framework (MUlti-atlas region Segmentation utilizing Ensembles of registration algorithms and parameters, and locally optimal atlas selection; Doshi et al. 2016). All shared AI2D data were processed with a **[BIDS-app wrapper of NiChart_DLMUSE](https://github.com/CBICA/BIDS_NiChart_DLMUSE)**:

Brain extraction is done using [**DLICV**](https://github.com/CBICA/DLICV).
 <div style="text-align: center;">
     <img src="{{ site.baseurl }}/assets/images/misc/dlicv.png" width="80%" height="auto" />
</div>

<br><br>
Brain segmentation is done using [**DLMUSE**](https://github.com/CBICA/DLMUSE).
 <div style="text-align: center;">
     <img src="{{ site.baseurl }}/assets/images/misc/dlmuse.png" width="80%" height="auto" />
</div>

<br><br>
The outputs include:

* ICV mask.
* Segmented T1w in native space.
* JSON files containing ROIs' volumes.
* HTML summary for visual quality control of DLICV and DLMUSE outputs.

This package uses [nnU-Net v2](https://github.com/MIC-DKFZ/nnUNet) as a basis model architecture for the deep learning parts.

