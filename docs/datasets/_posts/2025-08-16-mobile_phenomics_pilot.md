---
title: "Mobile Phenomics Pilot"
excerpt: "mobile_phenomics_pilot"
layout: single
categories: datasets

# Information for sidebar
site: University of California, San Francisco
pi: Melanie Rosen
website: https://www.ucsf.edu/
funding: NIH
publications:
recruitment:
age: 32.0
num_site: 1
institution: University of California, San Francisco
number_of_sessions: 50
inclusion:
exclusion:
phenotyping:
neuroimaging:
data_source:
data_release_use:
sample_size: 50
smri_count: 0
fmri_count: 0
cubic_path: /cbica/projects/pennlinc_rbc/datasets/mobile_phenomics_pilot
cubids: N/A (Mobile/Behavioral Data)
cubids_url: 
babs: N/A (Mobile/Behavioral Data)
smriprep_session: n/a
fmriprep_session: n/a
xcpd_session: n/a
qsiprep_session: n/a
qsirecon_session: n/a
smriprep_complete: n/a
fmriprep_complete: n/a
xcpd_complete: n/a
qsiprep_complete: n/a
qsirecon_complete: n/a
smriprep_version: n/a
fmriprep_version: n/a
xcpd_version: n/a
qsiprep_version: n/a
qsirecon_version: n/a
smriprep_dl: n/a
fmriprep_dl: n/a
xcpd_dl: n/a
qsiprep_dl: n/a
qsirecon_dl: n/a
smriprep_ephe: n/a
fmriprep_ephe: n/a
xcpd_ephe: n/a
qsiprep_ephe: n/a
qsirecon_ephe: n/a
---
<div style="text-align: left;">
     <img src="{{ site.baseurl }}/assets/images/logos/ucsf.png" style="width: auto; height: 10vw;" />
</div>

### About the dataset
[https://www.ucsf.edu/](https://www.ucsf.edu/)

*PI*
<br>
Tom Neylan

*Funding*
<br>
NIH

*Citations*
<br>
1. Neylan TC, et al. Mobile phenomics: using mobile devices to collect real-time data on sleep, mood, and cognitive function. Transl Psychiatry. 2019;9(1):1-10.

<br>
<div class=table align='center'>
<table style="text-align: center;
width:63%; font-size:90%; border: 1px solid black">
<tr><th style="font-weight:bold">CUBIC Path</th><th style="font-weight:normal">{{ page.cubic_path }}</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold">Sample Size</th><th style="font-weight:normal">{{ page.sample_size }}</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold">Number of Sessions</th><th style="font-weight:normal">{{ page.number_of_sessions }}</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold"><a href="{{ site.baseurl }}/docs/imaging/image_curation/">CuBIDS</a></th><th style="font-weight:normal">{% if page.cubids_url %}<a href="{{ page.cubids_url }}">{{ page.cubids }}</a>{% else %}{{ page.cubids }}{% endif %}</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold"><a href="{{ site.baseurl }}/docs/imaging/image_babs/">BABS</a></th><th style="font-weight:normal">{{ page.babs }}</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold">Average age</th><th style="font-weight:normal">{{ page.age }}</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold">% Female</th><th style="font-weight:normal">52</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold">% Right Handed:</th><th style="font-weight:normal">95</th><th style="font-weight:normal"></th></tr>
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
