---
title: "Neuroimaging"
excerpt: "Imaging"
layout: single
---

All raw imaging data and meta-data were carefully curated to conform with the [Brain Imaging Data Structure (BIDS)](https://bids.neuroimaging.io/) in a fully-reproducible fashion using [CuBIDS](https://cubids.readthedocs.io/en/latest/) (Covitz et al., 2022).
Next, we adopted the [“FAIRly-big” framework](https://www.nature.com/articles/s41597-022-01163-2) (Wagner et al., 2022) for reproducible image processing, ensuring all preparation and analysis were accompanied by a full audit trail in [DataLad](https://www.datalad.org/) (Halchenko et al., 2021).
Structural MRI data were processed using [FreeSurfer](https://surfer.nmr.mgh.harvard.edu/) and [sMRIPrep](https://www.nipreps.org/smriprep/), yielding commonly-used measures of brain structure.
Functional MRI data were preprocessed using [fMRIPrep](https://www.nipreps.org/fmriprep/) and [XCP-D](https://xcp-d.readthedocs.io/en/latest/usage.html) (Mehta et al., 2024) and a dedicated configuration that was rigorously quality controlled on all datasets, eventually yielding measures such as functional connectivity matrices, ReHo, and ALFF.
Processed structural and functional data were parcellated with 16 commonly-used atlases.