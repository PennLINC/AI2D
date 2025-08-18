---
title: "BABS: BIDS App Bootstrap"
excerpt: "BABS"
layout: single

---

<div style="text-align: center;">
     <img src="{{ site.baseurl }}/assets/images/misc/babs_workflow.png" width="70%" height="auto" />
</div>

**Citation**
<br>
Zhao, C., Jarecka, D., Covitz, S., Chen, Y., Eickhoff, S. B., Fair, D. A., ... & Satterthwaite, T. D. (2024). A reproducible and generalizable software workflow for analysis of large-scale neuroimaging data collections using BIDS Apps. Imaging Neuroscience, 2, 1-19. doi:10.1162/imag_a_00074.
<p style="margin: 2px 0;"></p>
Zhao, C., Chen, Y., Jarecka, D., Ghosh, S., Cieslak, M., & Satterthwaite, T. D. (2024). BABS in Action: Merging Reproducibility and Scalability for Large-Scale Neuroimaging Analysis With BIDS Apps. Biological Psychiatry, 95(10), S21-S22. doi:10.1016/j.biopsych.2024.02.056.


<br>
Most of the AI2D datasets were processed using **[BABS](https://pennlinc-babs.readthedocs.io/en/stable/)**. Knowing whether BABS was used for a dataset is important for determining how to access the data (see example: [CCNP]({{ site.baseurl }}/docs/datasets/dCCNP/#dataset-summary)).


**BABS** implements the [“FAIRly-big” framework](https://www.nature.com/articles/s41597-022-01163-2) (Wagner et al., 2021) for reproducible image processing, ensuring all data analyses were accompanied by a full audit trail in [Datalad](https://www.datalad.org/) (Halchenko et al., 2021). For AI2D datasets, if `BABS == true` in the Dataset Summary, all BIDS-apps (e.g., fMRIPrep, XCP-D) were run using BABS.
