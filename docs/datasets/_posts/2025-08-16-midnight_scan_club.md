---
title: "Midnight Scan Club"
excerpt: "midnight_scan_club"
layout: single
categories: datasets

# Information for sidebar
site: Washington University in St. Louis
pi: Nico Dosenbach
website: https://www.dosenlab.com/
funding: NIH
publications:
recruitment:
age: 24.0
num_site: 1
institution: Washington University in St. Louis
number_of_sessions: 10
inclusion:
exclusion:
phenotyping:
neuroimaging:
data_source:
data_release_use:
sample_size: 10
smri_count: 10
fmri_count: 10
cubic_path: /cbica/projects/pennlinc_rbc/datasets/midnight_scan_club
cubids: Complete
babs: Complete
smriprep_session: 10
fmriprep_session: 10
xcpd_session: 10
qsiprep_session: n/a
qsirecon_session: n/a
smriprep_complete: 10
fmriprep_complete: 10
xcpd_complete: 10
qsiprep_complete: n/a
qsirecon_complete: n/a
smriprep_version: smriprep 24-1-1
fmriprep_version: fmriprep 24-1-1
xcpd_version: xcpd 0-10-6
qsiprep_version: n/a
qsirecon_version: n/a
smriprep_dl: /cbica/projects/pennlinc_rbc/datasets/midnight_scan_club/fmriprep_anat-24-1-1-babs/output_ria#~data
fmriprep_dl: /cbica/projects/pennlinc_rbc/datasets/midnight_scan_club/fmriprep_func-24-1-1-babs/output_ria#~data
xcpd_dl: /cbica/projects/pennlinc_rbc/datasets/midnight_scan_club/xcpd-0-10-6-babs/output_ria#~data
qsiprep_dl: n/a
qsirecon_dl: n/a
smriprep_ephe: /cbica/projects/pennlinc_rbc/datasets/midnight_scan_club/FMRIPREP_ANAT-24-1-1_zipped
fmriprep_ephe: /cbica/projects/pennlinc_rbc/datasets/midnight_scan_club/FMRIPREP_FUNC-24-1-1_zipped
xcpd_ephe: /cbica/projects/pennlinc_rbc/datasets/midnight_scan_club/XCPD-0-10-6_zipped
qsiprep_ephe: n/a
qsirecon_ephe: n/a
---
<div style="text-align: left;">
     <img src="{{ site.baseurl }}/assets/images/logos/uc_berkeley.png" style="width: auto; height: 10vw;" />
</div>

### About the dataset
[https://gallantlab.org/](https://gallantlab.org/)

*PI*
<br>
Jack Gallant

*Funding*
<br>
NIH, NSF

*Citations*
<br>
1. Huth AG, de Heer WA, Griffiths TL, Theunissen FE, Gallant JL. Natural speech reveals the semantic maps that tile human cerebral cortex. Nature. 2016 Apr 28;532(7600):453-8. doi: 10.1038/nature17637. PMID: 27121839; PMCID: PMC4852309.

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
<tr><th style="font-weight:bold">% Female</th><th style="font-weight:normal">45</th><th style="font-weight:normal"></th></tr>
<tr><th style="font-weight:bold">% Right Handed</th><th style="font-weight:normal">87</th><th style="font-weight:normal"></th></tr>
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
     <img src="{{ site.baseurl }}/assets/images/datasets/midnight_scan_club_Flowchart.png" width="80%" height="auto" />
</div>
