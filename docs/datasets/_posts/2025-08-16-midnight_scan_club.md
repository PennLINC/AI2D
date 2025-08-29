---
title: "Midnight Scan Club"
excerpt: "Midnight Scan Club"
layout: single
categories: datasets

# Information for sidebar
site: Washington University in St. Louis
pi: Nico Dosenbach
website: "/AI2D/docs/datasets/midnight_scan_club"
study_website: https://openneuro.org/datasets/ds000224/versions/1.0.4
funding: 
institution: Washington University in St. Louis
publications: 
recruitment: 
inclusion: 
exclusion: 
phenotyping: 
neuroimaging: 
data_source: 
data_release_use: 
num_site: 1
age_avg: 29.1
age_range: 24-34
number_of_sessions: 123
sample_size: 10
cubic_project: open-datasets
cubic_path: /cbica/projects/pennlinc_rbc/datasets/midnight_scan_club
cubids: No
cubids_version: No
cubids_url: 
babs: No
babs_version: No
t1w: Yes
fmri: Yes
dmri: No
fmap: Yes
dua: None
dua_restrict: 
data_license: CC BY-NC-SA
data_paper: http://www.cell.com/neuron/fulltext/S0896-6273(17)30613-X
demo_data: https://openneuro.org/datasets/ds000224/versions/1.0.4/file-display/participants.json
p_female: 50
p_right: 100
smriprep_session: 21
freesurfer_session: 21
fmriprep_session: 102
xcpd_session: 102
mriqc_session: 123
smriprep_complete:
freesurfer_complete:
fmriprep_complete: 102
xcpd_complete: 102
mriqc_complete: 123
smriprep_version: 
freesurfer_version: v7.3.2
fmriprep_version: v24-0-0
xcpd_version: v0.7.5
mriqc_version: v0.9.6
qsiprep_version: 
qsirecon_bundle_version: 
qsirecon_whole_version: 
bids_dset: /cbica/projects/open-datasets/datasets/midnight_scan_club/dset
freesurfer_path: /cbica/projects/open-datasets/datasets/midnight_scan_club/derivatives/fmriprep-24.0.0/sourcedata/freesurfer/
fmriprep_path: /cbica/projects/open-datasets/datasets/midnight_scan_club/derivatives/fmriprep-24.0.0
xcpd_path: /cbica/projects/open-datasets/datasets/midnight_scan_club/derivatives/xcp_d-0.7.5
mriqc_path: /cbica/projects/open-datasets/datasets/midnight_scan_club/ds000224/derivatives/mriqc

---
<div style="text-align: left;">
     <img src="{{ site.baseurl }}/assets/images/logos/WashU.png" style="width: auto; height: 10vw;" />
</div>

### About the dataset

This dataset contains the **Midnight Scanning Club (MSC) data**, a dataset focused on the precise characterization of ten individual subjects via collection of large amounts of per-individual data. Each subject underwent twelve separate two-hour scanning sessions. In the first two sessions we collected four T1 images, four T2 images, four MR angiograms, and eight MR venograms. In the last ten sessions we collected five hours of resting-state fMRI data and over five and a half hours of task fMRI data across three different tasks. Participants also underwent extensive neuropsychological testing. These raw data are all provided here.

In addition to the raw data, we also provide several derivatives processed using both a volumetric (Talaraich-space) and a surface-based (fs_LR_32k space) pipeline. Volumetric derivatives include cross-session-average T1 and T2 images linearly registered to atlas (Talaraich) space; as well as resting-state data from each scanning session that has been fully preprocessed, motion-censored, and confound-regressed. Surface pipeline derivatives include cortical surfaces which were segmented from the T1 scans using freesurfer, hand-edited, and registered to fs_LR atlas space; resting-state data from each scanning session that has been fully preprocessed, motion-censored, and confound-regressed in CIFTI format (cortical: fs_LR32k; subcortical: Talaraich); cortical parcellations estimated from the resting-state data; vertex-wise whole-brain networks estimated from the resting-state data; task timecourses in CIFTI (cortical: fs_LR32k; subcortical: Talaraich) space; a selection of task contrast images in CIFTI (cortical: fs_LR32k; subcortical: Talaraich) space; myelin maps estimated from the T1- and T2-weighted anatomical scans; and matrices describing the physical geodesic/euclidean distances between every two points in the cifti image.

<div class="table" align="center">
  <table style="text-align:center; width:100%; font-size:18px; border:1px solid black">
    <tr>
      <th style="font-weight:bold; width:250px;">PI</th>
      <th style="font-weight:normal">{{ page.pi }}</th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">Institution</th>
      <th style="font-weight:normal">{{ page.institution }}</th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">Study Website</th>
      <th style="font-weight:normal"><a href="{{ page.study_website }}">{{ page.title }}</a></th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">Data Descriptor Paper</th>
      <th style="font-weight:normal"><a href="{{ page.data_paper }}">{{ page.data_paper }}</a></th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">CUBIC Project</th>
      <th style="font-weight:normal"><span style="color:blue;">{{ page.cubic_project }}</span></th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">DUA</th>
      <th style="font-weight:normal">{{ page.dua }}</th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">License</th>
      <th style="font-weight:normal">{{ page.data_license }}</th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">Sample Size</th>
      <th style="font-weight:normal">{{ page.sample_size }}</th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">Number of Sessions</th>
      <th style="font-weight:normal">{{ page.number_of_sessions }}</th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;"><a href="{{ site.baseurl }}/docs/imaging/image_curation/">CuBIDS</a></th>
      <th style="font-weight:normal">
        {% if page.cubids_url %}
          <a href="{{ page.cubids_url }}">{{ page.cubids_version }}</a>
        {% else %}
          {{ page.cubids_version }}
        {% endif %}
      </th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;"><a href="{{ site.baseurl }}/docs/imaging/image_babs/">BABS</a></th>
      <th style="font-weight:normal">{{ page.babs_version }}</th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">Demographics</th>
      <th style="font-weight:normal">
        {% if page.demo_data %}
          <a href="{{ page.demo_data }}">View available demographics data</a>
        {% else %}
          Not available
        {% endif %}
      </th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">Average Age (y)</th>
      <th style="font-weight:normal">{{ page.age_avg }}</th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">% Female</th>
      <th style="font-weight:normal">{{ page.p_female }}</th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">% Right Handed</th>
      <th style="font-weight:normal">{{ page.p_right }}</th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">BIDS Dataset</th>
      <th style="font-weight:normal">
        <div id="bids-dataset-copy" class="copy-container" style="border: 1px solid #6c6edc; border-radius: 3px; padding: 6px; background-color: #f8f9fa;">
          <span class="copy-text"><code>{{ page.bids_dset }}</code></span>
          <button class="copy-button" onclick="copyToClipboard('bids-dataset-copy')">Copy</button>
        </div>
      </th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">
        <a href="https://mriqc.readthedocs.io/">MRIQC</a>
        {{ page.mriqc_version }}
        <br>
        <span style="font-weight:normal;">({{ page.mriqc_complete }}/{{ page.mriqc_session }} complete)</span>
      </th>
      <th style="font-weight:normal">
        <div id="mriqc-path" class="copy-container" style="border: 1px solid #6c6edc; border-radius: 3px; padding: 6px; background-color: #f8f9fa;">
          <span class="copy-text"><code>{{ page.mriqc_path }}</code></span>
          <button class="copy-button" onclick="copyToClipboard('mriqc-path')">Copy</button>
        </div>
      </th>
      <th style="font-weight:normal"></th>
    </tr>

         {% assign pipelines = "freesurfer,fmriprep" | split: "," %}
     {% for pipe in pipelines %}
       {% assign version_key = pipe | append: "_version" %}
       {% assign complete_key = pipe | append: "_complete" %}
       {% assign session_key = pipe | append: "_session" %}
       {% assign path_key = pipe | append: "_path" %}
      <tr>
        <th style="font-weight:bold; width:250px;">
          {% if pipe == "freesurfer" %}
            FreeSurfer
          {% elsif pipe == "fmriprep" %}
            <a href="{{ site.baseurl }}/docs/imaging/image_fmriprep/">fMRIprep</a>
          {% endif %}
          {{ page[version_key] }}
          {% if page[complete_key] and page[session_key] %}
          {% if pipe == "freesurfer" %}
          <br>
          <span style="font-weight:normal;"><a href="https://fmriprep.org/en/24.0.0/workflows.html#longitudinal-processing">Longitudinal pipeline</a> run by fMRIPrep</span>
          {% else %}
          <br>
          <span style="font-weight:normal;">({{ page[complete_key] }}/{{ page[session_key] }} complete)</span>
          {% endif %}
          {% endif %}
        </th>
                 <th style="font-weight:normal">
           <div id="{{ pipe }}-path" class="copy-container" style="border: 1px solid #6c6edc; border-radius: 3px; padding: 6px; background-color: #f8f9fa;">
             <span class="copy-text"><code>{{ page[path_key] }}</code></span>
             <button class="copy-button" onclick="copyToClipboard('{{ pipe }}-path')">Copy</button>
           </div>
         </th>
        <th style="font-weight:normal"></th>
      </tr>
    {% endfor %}
  </table>
</div>

<style>
.copy-container { display: flex; align-items: center; justify-content: space-between; gap: 10px; }
.copy-text { flex: 1; word-break: break-all; }
.copy-button {
  background-color: rgb(108, 110, 220);
  color: white;
  border: none;
  padding: 4px 8px;
  border-radius: 3px;
  cursor: pointer;
  font-size: 18px;
  white-space: nowrap;
  flex-shrink: 0;
}
.copy-button:hover { background-color: rgb(104, 106, 235); }
.copy-button:active { background-color: rgb(84, 86, 215); }
</style>

<script>
function showTab(tabName) {
  var tabType = tabName.indexOf('-dl') !== -1 ? 'datalad' : 'ephemeral';
  var tabContents = document.getElementsByClassName('tab-content');
  for (var i = 0; i < tabContents.length; i++) {
    tabContents[i].classList.remove('active');
  }
  var tabButtons = document.getElementsByClassName('tab-button');
  for (var j = 0; j < tabButtons.length; j++) {
    tabButtons[j].classList.remove('active');
  }
  if (tabType === 'datalad') {
    var dls = document.querySelectorAll('[id$="-dl"]');
    var dlButtons = document.querySelectorAll('[onclick*="-dl"]');
    dls.forEach(function(c) { c.classList.add('active'); });
    dlButtons.forEach(function(b) { b.classList.add('active'); });
  } else {
    var eph = document.querySelectorAll('[id$="-ephe"]');
    var epheButtons = document.querySelectorAll('[onclick*="-ephe"]');
    eph.forEach(function(c) { c.classList.add('active'); });
    epheButtons.forEach(function(b) { b.classList.add('active'); });
  }
}
function copyToClipboard(elementId) {
  var element = document.getElementById(elementId);
  var textToCopy = element.querySelector('.copy-text').textContent;
  var textarea = document.createElement('textarea');
  textarea.value = textToCopy;
  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand('copy');
  document.body.removeChild(textarea);
  var button = element.querySelector('.copy-button');
  var originalText = button.textContent;
  button.textContent = 'Copied!';
  button.style.backgroundColor = '#28a745';
  setTimeout(function() {
    button.textContent = originalText;
    button.style.backgroundColor = 'rgb(108, 110, 220)';
  }, 1000);
}
</script>

<br>

*Funding*
<br>
This work was supported by National Institutes of Health Grants NS088590, TR000448 (NUFD), MH104592 (DJG), and HD087011 (to the Intellectual and Developmental Disabilities Research Center at Washington University); the Jacobs Foundation (NUFD); the Child Neurology Foundation (NUFD); the McDonnell Center for Systems Neuroscience (NUFD, BLS); the Mallinckrodt Institute of Radiology (NUFD); the Hope Center for Neurological Disorders (NUFD, BLS, SEP); and Dart Neuroscience LLC.

*Citations*
<br>
Gordon, E. M., Laumann, T. O., Gilmore, A. W., Newbold, D. J., Greene, D. J., Berg, J. J., ... & Dosenbach, N. U. (2017). Precision functional mapping of individual human brains. Neuron, 95(4), 791-807.