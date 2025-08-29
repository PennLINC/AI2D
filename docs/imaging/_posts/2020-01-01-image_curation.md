---
title: "Data Curation"
excerpt: "Data Curation"
layout: single

---

<br/>

<div style="text-align: center;">
    <img src="{{ site.baseurl }}/assets/images/logos/cubids.png" width="70%" height="auto" />
</div>

<div style="text-align: center;">
    <img src="{{ site.baseurl }}/assets/images/misc/cubids_workflow.png" width="70%" height="auto" />
</div>

<br/>
**Citation**
<br>
Covitz, S., Tapera, T. M., Adebimpe, A., Alexander-Bloch, A. F., Bertolero, M. A., Feczko, E., ... & Satterthwaite, T. D. (2022). Curation of BIDS (CuBIDS): A workflow and software package for streamlining reproducible curation of large BIDS datasets. NeuroImage, 263, 119609. doi:10.1016/j.neuroimage.2022.119609.

<br>
**[CuBIDS](https://cubids.readthedocs.io/en/latest/)** (Covitz et al., 2022) is a sanity preserving workflow that summarizes the heterogeneity in a MRI BIDS dataset, helps prepare BIDS datasets for preprocessing, and helps users perform metadata-based quality control on BIDS data.

CuBIDS was run for each dataset in the [Reproducible Brain Chart (RBC) study](https://reprobrainchart.github.io/): [CCNP]({{ site.baseurl }}/docs/datasets/dCCNP/), [HBN]({{ site.baseurl }}/docs/datasets/HBN/), [NKI]({{ site.baseurl }}/docs/datasets/NKI/), [PNC]({{ site.baseurl }}/docs/datasets/PNC/). A CuBIDS summary was created that provides an opportunity to evaluate the data and decide how to handle heterogeneity by grouping the scans on the basis of metadata.

You can find the link to the CuBIDS summary in each study-specific page. More information about how to interpret CuBIDS summaries can be found [here](https://cubids.readthedocs.io/en/latest/).
