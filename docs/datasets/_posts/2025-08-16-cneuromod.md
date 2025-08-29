---
title: "Neural Modelling"
excerpt: "cneuromod"
layout: single
categories: datasets

# Information for sidebar
site: Université de Montréal
pi: Lune Bellec
website: "/AI2D/docs/datasets/cneuromod"
study_website: https://www.cneuromod.ca
funding: 
institution: Université de Montréal<br>Centre intégré universitaire de santé et de services sociaux du Centre-Sud-de-l'Île-de-Montréal
publications: 
recruitment: 
inclusion: 
exclusion: 
phenotyping: 
neuroimaging: 
data_source: 
data_release_use: 
num_site: 1
age_avg: variable
age_range: variable
number_of_sessions: variable
sample_size: variable
cubic_project: open-datasets
cubic_path: /cbica/projects/open-datasets/datasets/cneuromod
cubids: No
cubids_version: No
cubids_url: 
babs: No
babs_version: No
t1w: Yes
fmri: Yes
dmri: No
fmap: Yes
dua: https://docs.cneuromod.ca/en/latest/ACCESS.html
dua_restrict:
data_license: https://docs.cneuromod.ca/en/latest/ACCESS.html#complete-cneuromod-databank-via-data-transfer-agreement-dta
data_paper_1: https://docs.cneuromod.ca/en/latest/DATASETS.html
data_paper_2: https://www.cneuromod.ca/gallery/datasets/
demo_data: sex, age
p_female: variable
p_right: 100
smriprep_session: variable
freesurfer_session:
fmriprep_session: variable
xcpd_session:
smriprep_complete: variable
freesurfer_complete:
fmriprep_complete: variable
xcpd_complete:
smriprep_version: v20.2.1
freesurfer_version: v6.0.1
fmriprep_version: v20.2.3
xcpd_version: xcpd 0-10-6
bids_dset1: /cbica/projects/open-datasets/datasets/cneuromod/cneuromod
bids_dset2: /cbica/projects/open-datasets/datasets/cneuromod/floc
bids_dset3: /cbica/projects/open-datasets/datasets/cneuromod/mario
bids_dset4: /cbica/projects/open-datasets/datasets/cneuromod/retinotopy
bids_dset5: /cbica/projects/open-datasets/datasets/cneuromod/things
freesurfer_path:
smriprep_path: /cbica/projects/open-datasets/datasets/cneuromod/cneuromod.processed/smriprep
fmriprep_path: /cbica/projects/open-datasets/datasets/cneuromod/cneuromod.processed/fmriprep

---
<div style="text-align: left;">
     <img src="{{ site.baseurl }}/assets/images/logos/cneuromod.png" style="width: auto; height: 10vw;" />
</div>

### About the dataset

The Courtois project on Neural Modelling (cneuromod) aims at training artificial neural networks using extensive experimental data on individual human brain activity and behaviour. Six subjects (three women, three men) were scanned weekly for five years (2018-23), with more sporadic scanning sessions still ongoing.

The cneuromod dataset currently features up to **200 hours** of functional data per subject, including functional localizers (vision, language, memory, emotion), movies and video game play. So far functional neuroimaging data have been collected with functional magnetic resonance imaging and a variety of sensors (including electrodermal activity and occulometry). A smaller subset of data was collected with electroencephalography.

The cneuromod project is funded by a donation of the Courtois foundation. Courtois NeuroMod data are freely shared with the scientific community to advance research at the interface of neuroscience and artificial intelligence. Four subjects have shared their data without any restriction, while access to the full sample follows a registered access model.

An overview of the project is available on the [cneuromod website](https://www.cneuromod.ca/) and the technical documentation of the latest release is accessible [here](https://docs.cneuromod.ca/en/latest/).

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
      <th style="font-weight:bold; width:250px;">Data Descriptor 1</th>
      <th style="font-weight:normal"><a href="{{ page.data_paper_1 }}">Documentation</a></th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">Data Descriptor 2</th>
      <th style="font-weight:normal"><a href="{{ page.data_paper_2 }}">Dataset Gallery</a></th>
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
      <th style="font-weight:normal">{{ page.demo_data }}</th>
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
      <th style="font-weight:bold; width:250px;">BIDS Dataset 1</th>
      <th style="font-weight:normal">
        <div id="bids-dataset-copy" class="copy-container" style="border: 1px solid #6c6edc; border-radius: 3px; padding: 6px; background-color: #f8f9fa;">
          <span class="copy-text"><code>{{ page.bids_dset1 }}</code></span>
          <button class="copy-button" onclick="copyToClipboard('bids-dataset-copy')">Copy</button>
        </div>
        <br>This path contains rawdata for following datasets:<br/>
        • <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#friends">friends</a><br/>
        • <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#harrypotter">harrypotter</a><br/>
        • <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#hcptrt">hcptrt</a><br/>
        • <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#movie10">movie10</a><br/>
        • <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#shinobi">shinobi</a><br/>
        • <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#shinobi-training">shinobi_training</a>
      </th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">BIDS Dataset 2</th>
      <th style="font-weight:normal">
        Rawdata for the <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#floc">floc</a> dataset
        <div id="bids-dataset2-copy" class="copy-container" style="border: 1px solid #6c6edc; border-radius: 3px; padding: 6px; background-color: #f8f9fa;">
          <span class="copy-text"><code>{{ page.bids_dset2 }}</code></span>
          <button class="copy-button" onclick="copyToClipboard('bids-dataset2-copy')">Copy</button>
        </div>
      </th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">BIDS Dataset 3</th>
      <th style="font-weight:normal">
        Rawdata for the <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#mario">mario</a> dataset
        <div id="bids-dataset3-copy" class="copy-container" style="border: 1px solid #6c6edc; border-radius: 3px; padding: 6px; background-color: #f8f9fa;">
          <span class="copy-text"><code>{{ page.bids_dset3 }}</code></span>
          <button class="copy-button" onclick="copyToClipboard('bids-dataset3-copy')">Copy</button>
        </div>
      </th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">BIDS Dataset 4</th>
      <th style="font-weight:normal">
        Rawdata for the <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#retinotopy">retinotopy</a> dataset
        <div id="bids-dataset4-copy" class="copy-container" style="border: 1px solid #6c6edc; border-radius: 3px; padding: 6px; background-color: #f8f9fa;">
          <span class="copy-text"><code>{{ page.bids_dset4 }}</code></span>
          <button class="copy-button" onclick="copyToClipboard('bids-dataset4-copy')">Copy</button>
        </div>
      </th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">BIDS Dataset 5</th>
      <th style="font-weight:normal">
        Rawdata for the <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#things">things</a> dataset
        <div id="bids-dataset5-copy" class="copy-container" style="border: 1px solid #6c6edc; border-radius: 3px; padding: 6px; background-color: #f8f9fa;">
          <span class="copy-text"><code>{{ page.bids_dset5 }}</code></span>
          <button class="copy-button" onclick="copyToClipboard('bids-dataset5-copy')">Copy</button>
        </div>
      </th>
      <th style="font-weight:normal"></th>
    </tr>
    <tr>
      <th style="font-weight:bold; width:250px;">Available preprocessed data</th>
      <th style="font-weight:normal">For the following datasets:<br/>
• <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#friends">friends</a><br/>
• <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#harrypotter">harrypotter</a><br/>
• <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#hcptrt">hcptrt</a><br/>
• <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#movie10">movie10</a><br/>
• <a href="https://docs.cneuromod.ca/en/latest/DATASETS.html#shinobi">shinobi</a></th>
      <th style="font-weight:normal"></th>
    </tr>

         {% assign pipelines = "smriprep,fmriprep" | split: "," %}
     {% for pipe in pipelines %}
       {% assign version_key = pipe | append: "_version" %}
       {% assign complete_key = pipe | append: "_complete" %}
       {% assign session_key = pipe | append: "_session" %}
       {% assign path_key = pipe | append: "_path" %}
      <tr>
        <th style="font-weight:bold; width:250px;">
          {% if pipe == "smriprep" %}
            <a href="{{ site.baseurl }}/docs/imaging/image_smriprep/">sMRIPrep</a>
          {% elsif pipe == "fmriprep" %}
            <a href="{{ site.baseurl }}/docs/imaging/image_fmriprep/">fMRIprep</a>
          {% endif %}
          {{ page[version_key] }}
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
The Courtois NeuroMod project was made possible by a donation from the Courtois foundation. These funds are administered by the Fondation Institut Gériatrie Montréal (FIGM) at Centre de Recherche de l’institut Universitaire de Gériatrie de Montréal, part of CIUSSS du Centre-Sud-de-l’île-de-Montréal, as well as University of Montreal. The team has grown to include individuals from various institutions, and an up-to-date list of contributors can be found in the documentation.

*Citations*
<br>
Julie Boyle, Basile Pinsard, Valentina Borghesani, Francois Paugam, Elizabeth DuPre, and Lune Bellec. The courtois neuromod project: quality assessment of the initial data release (2020). In 2023 Conference on Cognitive Computational Neuroscience, pages 2023–1602, 2023.

St-Laurent, M., Pinsard, B., Contier, O., Seeliger, K., Borghesani, V., Boyle, J., ... & Hebart, M. (2023). cneuromod-things: a large-scale fMRI dataset for task-and data-driven assessment of object representation and visual memory recognition in the human brain. Journal of Vision, 23(9), 5424-5424.