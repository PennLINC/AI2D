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


<br>
**[BABS](https://pennlinc-babs.readthedocs.io/en/stable/)** implements the [“FAIRly-big” framework](https://www.nature.com/articles/s41597-022-01163-2) (Wagner et al., 2021) for reproducible and scalable image processing, ensuring all data analyses were accompanied by a full audit trail in [Datalad](https://www.datalad.org/) (Halchenko et al., 2021). 

Several AI2D datasets were processed using **[BABS](https://pennlinc-babs.readthedocs.io/en/stable/)**. This is noted in the `BABS` section of each dataset-specific page (dataset links listed [here]({{ site.baseurl }}/docs/datasets)). If `BABS is not false` in the dataset-specific page, all BIDS-apps (e.g., fMRIPrep, XCP-D) were run using BABS.

<div class="alert alert-warning" role="alert">
  <strong>IMPORTANT:</strong> Knowing whether BABS was used for a dataset is important, as it affects how the data can be accessed (see <a href="{{ site.baseurl }}/docs/get_data/#1-request-access-to-a-cubic-project">Get Data</a>).
</div>