---
title: "cneuromod"
excerpt: "cneuromod"
layout: single
categories: datasets

# Information for sidebar
site: Université de Montréal
pi: Pierre Bellec
website: https://www.cneuromod.ca/
funding: Canadian Institute for Health Research
publications:
recruitment:
age: 30.0
num_site: 1
institution: Université de Montréal
number_of_sessions: 6
inclusion:
exclusion:
phenotyping:
neuroimaging:
data_source:
data_release_use:
sample_size: 6
smri_count: 6
fmri_count: 6
cubic_path: /cbica/projects/pennlinc_rbc/datasets/cneuromod
cubids: Complete
babs: Complete
smriprep_session: 6
fmriprep_session: 6
xcpd_session: 6
qsiprep_session: n/a
qsirecon_session: n/a
smriprep_complete: 6
fmriprep_complete: 6
xcpd_complete: 6
qsiprep_complete: n/a
qsirecon_complete: n/a
smriprep_version: smriprep 24-1-1
fmriprep_version: fmriprep 24-1-1
xcpd_version: xcpd 0-10-6
qsiprep_version: n/a
qsirecon_version: n/a
smriprep_dl: /cbica/projects/pennlinc_rbc/datasets/cneuromod/fmriprep_anat-24-1-1-babs/output_ria#~data
fmriprep_dl: /cbica/projects/pennlinc_rbc/datasets/cneuromod/fmriprep_func-24-1-1-babs/output_ria#~data
xcpd_dl: /cbica/projects/pennlinc_rbc/datasets/cneuromod/xcpd-0-10-6-babs/output_ria#~data
qsiprep_dl: n/a
qsirecon_dl: n/a
smriprep_ephe: /cbica/projects/pennlinc_rbc/datasets/cneuromod/FMRIPREP_ANAT-24-1-1_zipped
fmriprep_ephe: /cbica/projects/pennlinc_rbc/datasets/cneuromod/FMRIPREP_FUNC-24-1-1_zipped
xcpd_ephe: /cbica/projects/pennlinc_rbc/datasets/cneuromod/XCPD-0-10-6_zipped
qsiprep_ephe: n/a
qsirecon_ephe: n/a
---
<div style="text-align: left;">
     <img src="{{ site.baseurl }}/assets/images/logos/universite_de_montreal.png" style="width: auto; height: 10vw;" />
</div>

### About the dataset
[https://www.cneuromod.ca/](https://www.cneuromod.ca/)

*PI*
<br>
Pierre Bellec

*Funding*
<br>
Canadian Institutes of Health Research (CIHR)

*Citations*
<br>
1. Bellec P, et al. The CNeuromod dataset: a comprehensive multimodal dataset for neuroimaging research. Scientific Data. 2020;7(1):1-12.

<br>
<div class=table align='center'>
<table style="text-align: center;
width:63%; font-size:90%; border: 1px solid black">
<tr><th style="font-weight:bold">CUBIC Path</th><th style="font-weight:normal">{{ page.cubic_path }}</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold">Sample Size</th><th style="font-weight:normal">{{ page.sample_size }}</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold">Number of Sessions</th><th style="font-weight:normal">{{ page.number_of_sessions }}</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold"><a href="{{ site.baseurl }}/docs/imaging/image_curation/">CuBIDS</a></th><th style="font-weight:normal">{{ page.cubids }}</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold"><a href="{{ site.baseurl }}/docs/imaging/image_babs/">BABS</a></th><th style="font-weight:normal">{{ page.babs }}</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold">Average age</th><th style="font-weight:normal">{{ page.age }}</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold">% Female</th><th style="font-weight:normal">52</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold">% Right Handed</th><th style="font-weight:normal">88</th><th style="font-weight:normal"></th></tr>
</table>
</div>

<br>
<br>

## Data Access

<div class=table align='center'>
<table style="text-align: center; width:100%; font-size:90%; border: 1px solid black">
<tr>
<th style="font-weight:bold; text-align: center;"></th>
<th style="font-weight:bold; text-align: center;">Number of Sessions</th>
<th style="font-weight:bold; text-align: center;">Completed</th>
<th style="font-weight:bold; text-align: center;">Software Version</th>
<th style="font-weight:bold; text-align: center;">Datalad Dataset</th>
<th style="font-weight:bold; text-align: center;">Ephemeral Clone</th>
</tr>
<tr>
<th style="font-weight:bold; text-align: center;"><a href="{{ site.baseurl }}/docs/imaging/image_smriprep/">sMRIPrep</a></th>
<td style="font-weight:normal">{{ page.smriprep_session }}</td>
<td style="font-weight:normal">{{ page.smriprep_complete }}</td>
<td style="font-weight:normal">{{ page.smriprep_version }}</td>
<td style="font-weight:normal">{{ page.smriprep_dl }}</td>
<td style="font-weight:normal">{{ page.smriprep_ephe }}</td>
</tr>
<tr>
<th style="font-weight:bold; text-align: center;"><a href="{{ site.baseurl }}/docs/imaging/image_fmriprep/">fMRIPrep</a></th>
<td style="font-weight:normal">{{ page.fmriprep_session }}</td>
<td style="font-weight:normal">{{ page.fmriprep_complete }}</td>
<td style="font-weight:normal">{{ page.fmriprep_version }}</td>
<td style="font-weight:normal">{{ page.fmriprep_dl }}</td>
<td style="font-weight:normal">{{ page.fmriprep_ephe }}</td>
</tr>
<tr>
<th style="font-weight:bold; text-align: center;"><a href="{{ site.baseurl }}/docs/imaging/image_xcpd/">XCP-D</a></th>
<td style="font-weight:normal">{{ page.xcpd_session }}</td>
<td style="font-weight:normal">{{ page.xcpd_complete }}</td>
<td style="font-weight:normal">{{ page.xcpd_version }}</td>
<td style="font-weight:normal">{{ page.xcpd_dl }}</td>
<td style="font-weight:normal">{{ page.xcpd_ephe }}</td>
</tr>
</table>
</div>

<br>
<br>

<div style="text-align: center;">
     <img src="{{ site.baseurl }}/assets/images/datasets/cneuromod_Flowchart.png" width="80%" height="auto" />
</div>
