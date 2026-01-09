---
title: "NiChart_DLMUSE"
excerpt: "NiChart_DLMUSE"
layout: single

---

<style>
details p { margin: 8px 0 !important; }
details div { line-height: 1.6; }
.page__content { text-align: left !important; }
</style>

<br>
<div style="margin: 10px 0;">
<strong>Citation</strong><br/>
Doshi, Jimit, Guray Erus, Yangming Ou, Susan M Resnick, Ruben C Gur, Raquel E Gur, Theodore D Satterthwaite, Susan Furth, Christos Davatzikos, and Alzheimer’s Neuroimaging Initiative. 2016. “MUSE: MUlti-Atlas Region Segmentation Utilizing Ensembles of Registration Algorithms and Parameters, and Locally Optimal Atlas Selection.” NeuroImage 127: 186–95. https://doi.org/10.1016/j.neuroimage.2015.11.073.
</div>

<br>
[**NiChart_DLMUSE**](https://github.com/CBICA/NiChart_DLMUSE) performs deep-learning based brain extraction and segmentation on T1-weighted images. This is based on the MUSE framework (MUlti-atlas region Segmentation utilizing Ensembles of registration algorithms and parameters, and locally optimal atlas selection; Doshi et al. 2016). 

Shared AI2D data were either processed with [**NiChart_DLMUSE**](https://github.com/CBICA/NiChart_DLMUSE), or with a **[BIDS-app wrapper of NiChart_DLMUSE](https://github.com/CBICA/BIDS_NiChart_DLMUSE)**. 

ROI labels: [**MUSE_ROI_complete_list.csv**](https://github.com/CBICA/NiChart_DLMUSE/blob/main/NiChart_DLMUSE/shared/dicts/MUSE_ROI_complete_list.csv)

Brain extraction is done using [**DLICV**](https://github.com/CBICA/DLICV).
 <div style="text-align: center;">
     <img src="{{ site.baseurl }}/assets/images/misc/dlicv.png" width="80%" height="auto" />
</div>

<br><br>
Brain segmentation is done using [**DLMUSE**](https://github.com/CBICA/DLMUSE).
 <div style="text-align: center;">
     <img src="{{ site.baseurl }}/assets/images/misc/dlmuse.png" width="80%" height="auto" />
</div>

<br>

This package uses [nnU-Net v2](https://github.com/MIC-DKFZ/nnUNet) as a basis model architecture for the deep learning parts.
