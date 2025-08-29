---
title: "Structural Data Analysis"
excerpt: "Structural Data Analysis"
layout: single

---

<style>
details p { margin: 8px 0 !important; }
details div { line-height: 1.6; }
</style>

<div style="text-align: center;">
     <img src="{{ site.baseurl }}/assets/images/misc/smriprep_workflow.png" width="50%" height="auto" />
</div>

<br/>
<div style="margin: 10px 0;">
<strong>Citation</strong><br/>
Esteban, Oscar, Christopher Markiewicz, Ross W Blair, Craig Moodie, Ayse Ilkay Isik, Asier Erramuzpe Aliaga, James Kent, et al. 2019. "fMRIPrep: A Robust Preprocessing Pipeline for Functional MRI." Nature Methods 16: 111–16. https://doi.org/10.1038/s41592-018-0235-4.
<br><br>
Fischl, B. (2012). FreeSurfer. Neuroimage, 62(2), 774-781.
<br><br>
Dale, Anders M., Bruce Fischl, and Martin I. Sereno. 1999. "Cortical Surface-Based Analysis: I. Segmentation and Surface Reconstruction." NeuroImage 9 (2): 179–94. https://doi.org/10.1006/nimg.1998.0395.
</div>

<details style="margin: 10px 0;">
<summary><strong>More citations (Click to expand/minimize)</strong></summary>
<div style="padding: 10px 0; line-height: 1.6;">
Abraham, Alexandre, Fabian Pedregosa, Michael Eickenberg, Philippe Gervais, Andreas Mueller, Jean Kossaifi, Alexandre Gramfort, Bertrand Thirion, and Gael Varoquaux. 2014. "Machine Learning for Neuroimaging with Scikit-Learn." Frontiers in Neuroinformatics 8. https://doi.org/10.3389/fninf.2014.00014.
<p style="margin: 2px 0;"></p>
Avants, B. B., C. L. Epstein, M. Grossman, and J. C. Gee. 2008. "Symmetric Diffeomorphic Image Registration with Cross-Correlation: Evaluating Automated Labeling of Elderly and Neurodegenerative Brain." Medical Image Analysis 12 (1): 26–41. https://doi.org/10.1016/j.media.2007.06.004.
<p style="margin: 2px 0;"></p>
Ciric, R., William H. Thompson, R. Lorenz, M. Goncalves, E. MacNicol, C. J. Markiewicz, Y. O. Halchenko, et al. 2022. "TemplateFlow: FAIR-Sharing of Multi-Scale, Multi-Species Brain Models." Nature Methods 19: 1568–71. https://doi.org/10.1038/s41592-022-01681-2.
<p style="margin: 2px 0;"></p>
Evans, AC, AL Janke, DL Collins, and S Baillet. 2012. "Brain Templates and Atlases." NeuroImage 62 (2): 911–22. https://doi.org/10.1016/j.neuroimage.2012.01.024.
<p style="margin: 2px 0;"></p>
Fonov, VS, AC Evans, RC McKinstry, CR Almli, and DL Collins. 2009. "Unbiased Nonlinear Average Age-Appropriate Brain Templates from Birth to Adulthood." NeuroImage 47, Supplement 1: S102. https://doi.org/10.1016/S1053-8119(09)70884-5.
<p style="margin: 2px 0;"></p>
Glasser, Matthew F., Stamatios N. Sotiropoulos, J. Anthony Wilson, Timothy S. Coalson, Bruce Fischl, Jesper L. Andersson, Junqian Xu, et al. 2013. "The Minimal Preprocessing Pipelines for the Human Connectome Project." NeuroImage, Mapping the connectome, 80: 105–24. https://doi.org/10.1016/j.neuroimage.2013.04.127.
<p style="margin: 2px 0;"></p>
Gorgolewski, K., C. D. Burns, C. Madison, D. Clark, Y. O. Halchenko, M. L. Waskom, and S. Ghosh. 2011. "Nipype: A Flexible, Lightweight and Extensible Neuroimaging Data Processing Framework in Python." Frontiers in Neuroinformatics 5: 13. https://doi.org/10.3389/fninf.2011.00013.
<p style="margin: 2px 0;"></p>
Gorgolewski, Krzysztof J., Oscar Esteban, Christopher J. Markiewicz, Erik Ziegler, David Gage Ellis, Michael Philipp Notter, Dorota Jarecka, et al. 2018. "Nipype." Software. https://doi.org/10.5281/zenodo.596855.
<p style="margin: 2px 0;"></p>
Klein, Arno, Satrajit S. Ghosh, Forrest S. Bao, Joachim Giard, Yrjö Häme, Eliezer Stavsky, Noah Lee, et al. 2017. "Mindboggling Morphometry of Human Brains." PLOS Computational Biology 13 (2): e1005350. https://doi.org/10.1371/journal.pcbi.1005350.
<p style="margin: 2px 0;"></p>
Tustison, N. J., B. B. Avants, P. A. Cook, Y. Zheng, A. Egan, P. A. Yushkevich, and J. C. Gee. 2010. "N4ITK: Improved N3 Bias Correction." IEEE Transactions on Medical Imaging 29 (6): 1310–20. https://doi.org/10.1109/TMI.2010.2046908.
<p style="margin: 2px 0;"></p>
Zhang, Y., M. Brady, and S. Smith. 2001. "Segmentation of Brain MR Images Through a Hidden Markov Random Field Model and the Expectation-Maximization Algorithm." IEEE Transactions on Medical Imaging 20 (1): 45–57. https://doi.org/10.1109/42.906424.
</div>
</details>

<br>
Structural MRI data were processed using **sMRIPrep** by calling **[fMRIPrep](https://fmriprep.org/en/stable/)** with the `--anat-only` flag, which run the following steps: correction for intensity non-uniformity, skull-stripping with ANTs’ brain extraction workflow, and reconstruction of cortical surfaces using [**FreeSurfer**](https://surfer.nmr.mgh.harvard.edu/). The exact **sMRIPrep** pipeline is documented in the *boilerplate* located at `<fmriprep_anat_output>/logs/CITATION.html`. If the data were processed with [BABS]({{ site.baseurl }}/docs/imaging/image_babs/), refer to [Get Data]({{ site.baseurl }}/docs/get_data#312-explore-the-data-structure) for details on unzipping `<fmriprep_anat_output>` to access the boilerplate file.

**FreeSurfer** outputs were further processed using [**FreeSurfer-Post**](https://github.com/PennLINC/freesurfer-post/tree/main) which produced tabulated FreeSurfer data that were parcellated using 27 anatomical, functional, and multimodal atlases such as Desikan Killiany, Glasser, Gordon, and multiple resolutions of the Schaefer parcellation, among others. 

Outputs from this pipeline include commonly used measures of brain structure such as regional surface area, cortical thickness, gray matter volume, and folding and curvature indices. Moreover, summary brain measures such as total intracranial volume, ventricle size, and mean and standard deviation of various measures (e.g., cortical thickness, surface area) are provided for the whole brain and per hemisphere. Tabulated data are also accompanied by .json files describing each structural feature in detail.

