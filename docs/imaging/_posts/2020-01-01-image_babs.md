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
**[BABS](https://pennlinc-babs.readthedocs.io/en/stable/)** implements the [“FAIRly-big” framework](https://www.nature.com/articles/s41597-022-01163-2) (Wagner et al., 2021) for reproducible and scalable image processing, ensuring all data analyses were accompanied by a full audit trail in [Datalad](https://www.datalad.org/) (Halchenko et al., 2021). 

Several AI2D datasets were processed using **[BABS](https://pennlinc-babs.readthedocs.io/en/stable/)**. This is noted in the `BABS` section of each dataset-specific page (dataset links listed [here]({{ site.baseurl }}/docs/datasets)). If `BABS is not false` in the dataset-specific page, all BIDS-apps (e.g., fMRIPrep, XCP-D) were run using BABS. Knowing whether BABS was used for a dataset is important, as it affects how the data can be accessed (see [Get Data]({{ site.baseurl }}/docs/get_data/#1-request-access-to-a-cubic-project)).