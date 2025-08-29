---
title: "How to Get Data on CUBIC"
excerpt: "Get Data"
layout: single
permalink: /docs/get_data

---

The following instruction are intended specifically to get data on CUBIC.


## Table of Contents

1. [Request access to a CUBIC project](#1-request-access-to-a-cubic-project)
2. [Dataset processed without BABS](#2-dataset-processed-without-babs)
3. [Dataset processed with BABS](#3-dataset-processed-with-babs)
   - 3.1. [Get data without DataLad](#31-get-data-without-datalad)
     - [Prerequisites](#311-prerequisites)
     - [Explore the Data Structure](#312-explore-the-data-structure)
     - [Extract Specific Data](#313-extract-specific-data)
   - 3.2. [Get data with DataLad](#32-get-data-with-datalad)
     - [Prerequisites](#321-prerequisites)
     - [Example walkthrough](#322-example-walkthrough)

---

## 1. Request access to a CUBIC project

<span style="color: #7556b7;">🌟 **Check the `CUBIC Project` section on the dataset-specific page to identify which CUBIC project you need to request access to** (Dataset-specific links listed [here]({{ site.baseurl }}/docs/datasets)).</span>

<span style="color: #7556b7;">🌟 **Check the `DUA` section on the dataset-specific page and obtain the appropriate DUA** (Dataset-specific links listed [here]({{ site.baseurl }}/docs/datasets)).</span> 

Then, follow these steps:

1. Send Dr. Satterthwaite a request including the following:
    - The level of access, in this case, you will need **read-only access**
    - The name of the user[s] to be given access (full name or login name). If you plan to store and analyze data in a CUBIC project, you should use **your project username**, not personal CUBIC username.
    - The full path to the project you need access to, `/cbica/projects/<project_name>`.
2. Submit the DUA (if required) and Dr. Satterthwaite’s approval (PDF) — specifying access level, requesting users/project users, and the full project path — to <span style="color: blue;">**help@cbica.upenn.edu**</span>.


<span style="color: #7556b7;">🌟 **Once you have access to the project, check the `BABS` section on the dataset-specific page to determine whether the dataset was processed with [BABS]({{  site.baseurl }}/docs/imaging/image_babs)** (Dataset-specific links listed [here]({{ site.baseurl }}/docs/datasets)).</span>

## 2. Dataset processed without BABS

If the dataset was NOT processed with BABS, you can copy the data as follows:

```bash
$ cp -r /path/to/AI2D/dataset /path/to/your/project
```

## 3. Dataset processed with BABS

If the dataset WAS processed with BABS, you can either [get data WITHOUT `datalad`](#31-get-data-without-datalad), or [get data USING `datalad`](#32-get-data-with-datalad).

### 3.1. Get data without DataLad

Outputs from our processing pipelines were most of the time zipped to save inodes.

This section provides instructions in case you prefer NOT to use DataLad and instead want to unzip the output files directly into your CUBIC project directory.

**Pros:**
- Simple and requires no additional software
- Lightweight — you extract only the files you need

**Cons:**
- Does not support data provenance tracking  

### 3.1.1. Prerequisites

<span style="color: #7556b7;">🌟 **Check the dataset-specific page for the paths of the ephemeral clones** (Dataset-specific links listed [here]({{ site.baseurl }}/docs/datasets)).</span>

<span style="color: #7556b7;">🌟 **Download the extraction script:** [unzip_files.sh]({{ site.baseurl }}/scripts/unzip_files.sh).</span> The script supports:
- Extracting all files from zip archives
- Filtering by subject list (text file with subject IDs)
- Extracting specific file patterns using regex
- Combining subject lists with file patterns

For usage instructions, run the script with the `-h` or `--help` flag.

### 3.1.2. Explore the Data Structure

Before extracting data, it's helpful to understand what files are included in the zip file. You can either:

**Option A: Extract a sample participant's data**
```bash
# Create a single subject list file (e.g., one exemplar subject)
echo "sub-100307" > single_subject.txt

input_dir=/path/to/ephemeral/clone
output_dir=/path/to/your/cubic/project

bash unzip_files.sh ${input_dir} ${output_dir} single_subject.txt
```

**Option B: List contents of a zip file**
```bash
# XCP-D example
input_dir=/path/to/ephemeral/clone
7z l ${input_dir}/<subject_id>*.zip
```

### 3.1.3. Extract Specific Data

Once you understand the data structure, you can extract exactly what you need:

**Extract specific files for selected subjects:**
```bash
# XCP-D example
input_dir=/path/to/ephemeral/clone
output_dir=/path/to/your/cubic/project
file_pattern="xcpd*/sub-*/func/sub-*_task-rest*space-fsLR_seg-Glasser_stat-pearsoncorrelation_relmat.tsv"

bash unzip_files.sh ${input_dir} ${output_dir} subject_list.txt "${file_pattern}"

```

**Extract specific files for all available subjects:**
```bash
# Omit the subject list to process all subjects
bash unzip_files.sh ${input_dir} ${output_dir} "${file_pattern}"
```

### 3.2. Get data with DataLad

This section provides instructions in case you prefer to use [DataLad](https://handbook.datalad.org/en/latest/intro/philosophy.html).

**Pros:**
- Full data provenance tracking

**Cons:**
- Some knowledge of `datalad`, `git`, `git annex` 

### 3.2.1. Prerequisites

<span style="color: #7556b7;">🌟 **Check the dataset-specific page for the paths of the datalad datasets** (Dataset-specific links listed [here]({{ site.baseurl }}/docs/datasets)).</span>

<span style="color: #7556b7;">🌟 **Install DataLad**</span>

Follow the instructions [here](https://www.datalad.org/#install) to get `datalad` installed.

Accessing AI2D data via DataLad happens in two steps. You will first `clone` a AI2D data repository. This will make a copy of the AI2D file layout, but none of the actual data will be present. The next step is to `get` your data, which tells DataLad to download the content of specific files to your copy. Once the file content is present in your copy, you can use AI2D data just like any other set of files.

### 3.2.2. Example walkthrough

```bash
$ datalad clone \
    ria+file:///cbica/projects/pennlinc_rbc/datasets/LINC_CCNP/derivatives/xcpd-0-10-6-babs/output_ria#~data \
    ccnp_xcpd

[INFO   ] Configure additional publication dependency on "output-storage"                                                                           
configure-sibling(ok): . (sibling)
install(ok): /cbica/projects/pennlinc_rbc/ccnp_xcpd (dataset)
action summary:
  configure-sibling (ok: 1)
  install (ok: 1)

$ cd ccnp_xcpd
$ datalad get sub-colornest001_ses-1_xcpd-0-10-6.zip
get(ok): sub-colornest001_ses-1_xcpd-0-10-6.zip (file) [from output-storage...]

$ datalad drop sub-colornest001_ses-1_xcpd-0-10-6.zip
drop(ok): sub-colornest001_ses-1_xcpd-0-10-6.zip (file)  
```

<div class="alert alert-primary" role="alert">
  <b>WARNING:</b> These studies take up a lot of disk space. If you attempt to `get` all the file content, you will likely run out of space unless you have a very large storage.
</div>
