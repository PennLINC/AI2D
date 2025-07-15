---
title: "How to Get Data on CUBIC"
excerpt: "Get Data"
layout: single
permalink: /docs/get_data

---

The following instruction are intended specifically to get data on CUBIC.

## Table of Contents

1. [Request access to a CUBIC project](#1-request-access-to-a-cubic-project)
2. [Get data without DataLad](#2-get-data-without-datalad)
   - [Prerequisites](#21-prerequisites)
   - [Explore the Data Structure](#22-explore-the-data-structure)
   - [Extract Specific Data](#23-extract-specific-data)
3. [Get data with DataLad](#3-get-data-with-datalad)
   - [Install DataLad](#31-install-datalad)
   - [Pick a dataset](#32-pick-a-dataset)
   - [Clone the data](#33-clone-the-data)
   - [Example walkthrough](#34-example-walkthrough)
   - [FAQs](#35-faqs)

---

## 1. Request access to a CUBIC project

1. Send Dr. Satterthwaite a request including the following:
    - The level of access, in this case, you will need **read-only access**
    - The name of the user[s] to be given access (full name or login name). If you plan to store and analyze data in a CUBIC project, you should use **your project username**, not personal CUBIC username.
    - The full path to the project you need access to. You can find the project path for each study [here]({{ site.baseurl }}/docs/datasets/).
2. Submit the approval from Dr. Satterthwaite — including the specified user name, project name, and type of access — as a PDF printout to help@cbica.upenn.edu.

## 2. Get data without DataLad

Outputs from our processing pipelines were most of the time zipped to save inodes.

This section provides instructions in case you prefer NOT to use DataLad and instead want to unzip the output files directly into your CUBIC project directory.

**Pros:**
- Simple and requires no additional software
- Lightweight — you extract only the files you need

**Cons:**
- Does not support data provenance tracking  

### 2.1. Prerequisites

**Download the extraction script:** [unzip_files.sh]({{ site.baseurl }}/scripts/unzip_files.sh). The script supports:
- Extracting all files from zip archives
- Filtering by subject list (text file with subject IDs)
- Extracting specific file patterns using regex
- Combining subject lists with file patterns

For usage instructions, run the script with the `-h` or `--help` flag.

### 2.2. Explore the Data Structure

Before extracting data, it's helpful to understand what files are included in the zip file. You can either:

**Option A: Extract a sample participant's data**
```bash
# Create a single subject list file (e.g., one exemplar subject)
echo "sub-100307" > single_subject.txt

# HCP-YA XCP-D example
input_dir=/cbica/projects/pennlinc_hcpya/data/rbc_xcpd/DANGER
output_dir=/your/cubic/project/sample

bash unzip_files.sh ${input_dir} ${output_dir} single_subject.txt
```

**Option B: List contents of a zip file**
```bash
# HCP-YA XCP-D
input_dir=/cbica/projects/pennlinc_hcpya/data/rbc_xcpd/DANGER
7z l ${input_dir}/<subject_id>_xcpd-0.9.1.zip

# HCP-YA QSIRecon HSVS  
input_dir=/cbica/projects/pennlinc_hcpya/data/qsirecon_hsvs/DANGER
7z l ${input_dir}/<subject_id>_qsirecon-1-0-0rc2.zip
```

### 2.3 Step 2: Extract Specific Data

Once you understand the data structure, you can extract exactly what you need:

**Extract specific files for selected subjects:**
```bash
# HCP-YA XCP-D: Get functional connectivity matrices
input_dir=/cbica/projects/pennlinc_hcpya/data/rbc_xcpd/DANGER
output_dir=/your/cubic/project/xcpd-results
file_pattern="xcpd*/sub-*/func/sub-*_task-rest*space-fsLR_seg-Glasser_stat-pearsoncorrelation_relmat.tsv"

bash unzip_files.sh ${input_dir} ${output_dir} subject_list.txt "${file_pattern}"

# HCP-YA QSIRecon: Get diffusion segmentation files
input_dir=/cbica/projects/pennlinc_hcpya/data/qsirecon_hsvs/DANGER
output_dir=/your/cubic/project/qsirecon-results
file_pattern="qsirecon*/sub*/dwi/sub*seg-Glasser_dseg.mif.gz"

bash unzip_files.sh ${input_dir} ${output_dir} subject_list.txt "${file_pattern}"
```

**Extract specific files for all available subjects:**
```bash
# Omit the subject list to process all subjects
bash unzip_files.sh ${input_dir} ${output_dir} "${file_pattern}"
```

## 3. Get data with DataLad

This section provides instructions in case you prefer to use DataLad.

**Pros:**
- Full data provenance tracking

**Cons:**
- Some knowledge of `datalad`, `git`, `git annex` and how to debug  

### 3.1. Install DataLad

AI2D data is accessible via `datalad`. Follow the instructions [here](https://www.datalad.org/#install) to get it installed.

Accessing AI2D data via DataLad happens in two steps. You will first `clone` a AI2D data repository from github. This will make a copy of the AI2D file layout, but none of the actual data will be present. The next step is to `get` your data, which tells DataLad to download the content of specific files to your copy. Once the file content is present in your copy, you can use AI2D data just like any other set of files.


### 3.2. Pick a dataset

You can find each of the unprocessed BIDS MRI data, processed functional and processed structural
derivatives in their corresponding repositories on GitHub.

The repositories (you can find them all
[here](https://github.com/orgs/ReproBrainChart/repositories)) are consistently named such that:

 * If you're looking for BIDS MRI, the repo will be named `<study>_BIDS`
 * If you're looking for processed functional data, the repo will be named `<study>_CPAC`
 * If you're looking for processed structural MRI, the repo will be named `<study>_FreeSurfer`

where `<study>` is replaced with `HBN`, `NKI`, `PNC`, `BHRC` or `CCNP`.

Note: Participant demographics and phenotypic data are under `<study>_BIDS` repository for each study and are named `study-<study>_desc-participants.tsv`.

#### Choose a QC threshold

When you download AI2D data at a specific QC threshold you can be sure that
any file you find in your downloaded data is usable for further analysis.
AI2D releases data at 3 different QC thresholds:

 * `complete-pass`: Structural and BOLD data have passed QC
 * `complete-artifact`: Structural data can be "Pass" or "Artifact", BOLD is "Pass"
 * `warning-fail`: Contains all the AI2D data including QC failures. This threshold
  is not recommended and you'll have to explain why you chose this threshold in
  any publication resulting from it.

#### Choose a version

Lastly, you'll need to pick a _version_ of the data to get. Each time AI2D makes
changes to the data, it will be released with a new version number. By picking
a version number for your AI2D-based study you can be sure that your input data
will never change. The current release of AI2D is `0.1`.


### 3.3. Clone the data

Getting data on to your system will involve running a command like this:

```bash
$ datalad clone \
    https://github.com/ReproBrainChart/<study>_<content>.git \
    -b <qc_threshold>-<version>
```


### 3.4. Example walkthrough

Suppose I'd like to get some processed structural data from PNC. I've decided that I don't
want to include T1ws with notable artifacts, so I choose the QC threshold to be `complete-pass`.
I've checked the AI2D website and see that the most recent release is `0.1`. This means that
my last argument to `datalad clone` will be `-b complete-pass-0.1`.

From the example command in [ths documentation](#clone-the-data) I replace `<study>`
with `PNC` and `<content>` with `FreeSurfer`. My command would be:

```bash
$ datalad clone \
    https://github.com/ReproBrainChart/PNC_FreeSurfer.git \
    -b complete-pass-0.1
```

I see some warnings such as these:

```
[INFO   ] Unable to parse git config from origin
[INFO   ] Remote origin does not have git-annex installed; setting annex-ignore
[INFO   ] This could be a problem with the git-annex installation on the remote. Please make sure that git-annex-shell is available in PATH when you ssh into the remote. Once you have fixed the git-annex installation, run: git annex enableremote origin
install(ok): /home/cieslakm/data/PNC_FreeSurfer (dataset)
```

but these are ok. I now have a `DataLad` dataset with everything I need to start exploring AI2D data.


That command finishes surprisingly quickly: PNC
FreeSurfer has over a thousand subjects in it! But this is normal for `DataLad`.
(Note that cloning the processed functional data (i.e., `CPAC` files) will take
longer as `CPAC` functional outputs include more files compared to
`FreeSurfer`.) There is now a `PNC_FreeSurfer` directory that I can look
around in. Since I don't know which files I might want, I will explore this directory
in my terminal:

```bash
$ cd PNC_FreeSurfer/freesurfer/sub-192413932
$ ls
sub-192413932_brainmeasures.json@  sub-192413932_fsaverage.tar.xz@
sub-192413932_brainmeasures.tsv@   sub-192413932_fsLR_den-164k.tar.xz@
sub-192413932_freesurfer.tar.xz@   sub-192413932_regionsurfacestats.tsv@
```

These two tsv files contain the anatomical variables in tabular form, so I'd like
to copy these contents to my computer:

```bash
$ datalad get *.tsv
get(ok): freesurfer/sub-192413932/sub-192413932_regionsurfacestats.tsv (file) [from output-storage...]
get(ok): freesurfer/sub-192413932/sub-192413932_brainmeasures.tsv (file) [from output-storage...]
action summary:
  get (ok: 2)
```

Shell glob patterns can be used to get whichever files you might need.

<div class="alert alert-primary" role="alert">
  <b>WARNING:</b> DO NOT attempt to `get` all the file content! These studies take up
  a lot of disk space and you will likely run out of space unless you have a very big
  hard drive.
</div>


### 3.5. FAQs

#### Running `datalad get` appears to be stuck - what should I do?

The first time you run `datalad get` may take 30 minutes or more to finish
copying the file. Subsequent runs of `datalad get` will be much faster.

Unless you see an error message when running `datalad get`, you should let
the command run until you see something printed out.

#### Do I need a supercomputer to get this data?

You can clone any of these datasets to any machine with internet access,
[`DataLad` (`git` and `git-annex`) installed](https://www.datalad.org/#install)
and your agreement with the License. The rest of the answer depends on what type
of data you plan on copying to your computer:

 * If you plan on copying only tabular data content to your computer you will need
at most a few free GB.
 * If you plan on copying 3D imaging data (e.g. ALFF, REHO) you will need hundreds of GB free.
 * If you plan on copying 4D denoised BOLD timeseries data you will need up to 4TB of free space.

