---
title: "Single-echo/multi-echo comparison pilot"
excerpt: "Mobile Phenomics Pilot"
layout: single
categories: datasets

# Information for sidebar
site: University of Pennsylvania / CHOP Lifespan Brain Institute
pi: Theodore D. Satterthwaite
website: "/AI2D/docs/datasets/mobile_phenomics_pilot"
study_website: https://openneuro.org/datasets/ds005250/versions/1.1.5
funding: AE Foundation; Penn-CHOP Lifespan Brain Institute; NIMH R01MH113550
institution: University of Pennsylvania
publications:
recruitment:
inclusion:
exclusion:
phenotyping:
neuroimaging: T1w; single-echo fMRI; multi-echo fMRI; field maps (SE, ME, PEpolar)
data_source:
data_release_use:
num_site: 1
age_avg: 24.5
age_range: 21-30
number_of_sessions: 17
sample_size: 8
cubic_project: open-datasets
cubic_path: /cbica/projects/open-datasets/datasets/mobile_phenomics_pilot
cubids: "No"
cubids_version:
cubids_url: 
babs: "No"
babs_version:
t1w: Yes
fmri: Yes
dmri: No
fmap: Yes
dua: None
dua_restrict:
data_license: CC BY-NC-SA
data_paper: https://openneuro.org/datasets/ds005250/versions/1.1.5
demo_data: https://openneuro.org/datasets/ds005250/versions/1.1.5/file-display/participants.json
p_female: 50
p_right: 
smriprep_session: 
freesurfer_session: 17
fmriprep_session: 17
xcpd_session: 
smriprep_complete: 
freesurfer_complete: 17
fmriprep_complete: 17
xcpd_complete: 
smriprep_version: 
freesurfer_version: v7.3.2
fmriprep_version: v24.0.1
xcpd_version: 
qsiprep_version: 
qsirecon_bundle_version: 
qsirecon_whole_version: 
bids_dset: /cbica/projects/open-datasets/datasets/mobile_phenomics_pilot/ds005250
freesurfer_path: /cbica/projects/open-datasets/datasets/mobile_phenomics_pilot/derivatives/fmriprep-24.0.1/sourcedata
fmriprep_path: /cbica/projects/open-datasets/datasets/mobile_phenomics_pilot/derivatives/fmriprep-24.0.1

---
<div style="text-align: left;">
     <img src="{{ site.baseurl }}/assets/images/logos/university_of_pennsylvania.png" style="width: auto; height: 10vw;" />
</div>

### About the dataset

This dataset contains ABCD-protocol single-echo BOLD scans, along with complex-valued, multi-echo BOLD scans for comparison. The multi-echo BOLD protocol uses the CMRR MB-EPI sequence, and comes from collaborators at UMinn. These scans include five echoes with both magnitude and phase reconstruction.

The primary goal of this dataset was to evaluate the usability of the multi-echo fMRI protocol in a larger study, via direct comparison to the ABCD fMRI protocol, as well as via test-retest reliability analyses. However, these data may be useful to others (e.g., for testing complex-valued models, applying phase regression to multi-echo data, testing multi-echo denoising methods).

Dataset contents
This dataset includes 8 participants, each with between 1 and 3 sessions. MR data were acquired using a 3-Tesla Siemens Prisma MRI scanner. More information about the dataset [here](https://openneuro.org/datasets/ds005250/versions/1.1.5).

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
      <th style="font-weight:bold; width:250px;">Data Descriptor</th>
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
        {% if page.cubids == "Yes" %}
          {% if page.cubids_url %}
            <a href="{{ page.cubids_url }}">{{ page.cubids }} ({{ page.cubids_version }})</a>
          {% else %}
            {{ page.cubids }} ({{ page.cubids_version }})
          {% endif %}
        {% else %}
          {{ page.cubids }}
        {% endif %}
      </th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;"><a href="{{ site.baseurl }}/docs/imaging/image_babs/">BABS</a></th>
      <th style="font-weight:normal">
        {% if page.babs == "Yes" %}
          {{ page.babs }} ({{ page.babs_version }})
        {% else %}
          {{ page.babs }}
        {% endif %}
      </th>
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
            <a href="{{ site.baseurl }}/docs/imaging/image_fmriprep/">fMRIPrep</a>
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
AE Foundation  
Penn-CHOP Lifespan Brain Institute  
NIMH R01MH113550  

*Citations*
<br>
Taylor Salo and M. Dylan Tisdall and Lia Brodrick and Adam Czernuszenko and David R. Roalf and Sage Rush-Goebel and Nicholas Wellman and Matthew Cieslak and Theodore D. Satterthwaite (2024). Single-echo/multi-echo comparison pilot. OpenNeuro. [Dataset] doi: doi:10.18112/openneuro.ds005250.v1.1.5