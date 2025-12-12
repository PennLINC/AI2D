---
title: "Diffusion Data Reconstruction"
excerpt: "Diffusion Data Reconstruction"
layout: single

---

<style>
details p { margin: 8px 0 !important; }
details div { line-height: 1.6; }
</style>

<div style="text-align: center;">
     <img src="{{ site.baseurl }}/assets/images/misc/qsirecon_workflow.png" width="60%" height="auto" />
</div>

<br/>
<div style="margin: 10px 0;">
<strong>Citation</strong><br/>
Cieslak, Matthew, Philip A Cook, Xiaosong He, Fang-Cheng Yeh, Thijs Dhollander, Azeez Adebimpe, Geoffrey K Aguirre, et al. 2021. “QSIPrep: An Integrative Platform for Preprocessing and Reconstructing Diffusion Mri Data.” Nature Methods 18 (7). Nature Publishing Group US New York: 775–78. https://doi.org/10.1038/s41592-021-01185-5.
</div>

<details style="margin: 10px 0;">
<summary><strong>More citations (Click to expand/minimize)</strong></summary>
<div style="padding: 10px 0; line-height: 1.6;">
Abraham, Alexandre, Fabian Pedregosa, Michael Eickenberg, Philippe Gervais, Andreas Mueller, Jean Kossaifi, Alexandre Gramfort, Bertrand Thirion, and Gael Varoquaux. 2014. “Machine Learning for Neuroimaging with Scikit-Learn.” Frontiers in Neuroinformatics 8. https://doi.org/10.3389/fninf.2014.00014.
<p style="margin: 2px 0;"></p>
Dhollander, Thijs, David Raffelt, and Alan Connelly. 2016. “Unsupervised 3-Tissue Response Function Estimation from Single-Shell or Multi-Shell Diffusion Mr Data Without a Co-Registered T1 Image.” In ISMRM Workshop on Breaking the Barriers of Diffusion Mri, 5:5.
<p style="margin: 2px 0;"></p>
Dhollander, T, R Mito, D Raffelt, and A Connelly. 2019. “Improved White Matter Response Function Estimation for 3-Tissue Constrained Spherical Deconvolution.” In Proc. Intl. Soc. Mag. Reson. Med, 555.
<p style="margin: 2px 0;"></p>
Garyfallidis, Eleftherios, Matthew Brett, Bagrat Amirbekian, Ariel Rokem, Stefan Van Der Walt, Maxime Descoteaux, and Ian Nimmo-Smith. 2014. “Dipy, a Library for the Analysis of Diffusion Mri Data.” Frontiers in Neuroinformatics 8. Frontiers: 8.
<p style="margin: 2px 0;"></p>
Gorgolewski, K., C. D. Burns, C. Madison, D. Clark, Y. O. Halchenko, M. L. Waskom, and S. Ghosh. 2011. “Nipype: A Flexible, Lightweight and Extensible Neuroimaging Data Processing Framework in Python.” Frontiers in Neuroinformatics 5: 13. https://doi.org/10.3389/fninf.2011.00013.
<p style="margin: 2px 0;"></p>
Gorgolewski, Krzysztof J., Oscar Esteban, Christopher J. Markiewicz, Erik Ziegler, David Gage Ellis, Michael Philipp Notter, Dorota Jarecka, et al. 2018. “Nipype.” Software. Zenodo. https://doi.org/10.5281/zenodo.596855.
<p style="margin: 2px 0;"></p>
J-Donald, Robert Smith, David Raffelt, Rami Tabbara, Thijs Dhollander, Maximilian Pietsch, Daan Christiaens, Ben Jeurissen, Chun-Hung Yeh, and Alan" Connelly. 2019. “MRtrix3: A Fast, Flexible and Open Software Framework for Medical Image Processing and Visualisation.” NeuroImage 202: 116137.
<p style="margin: 2px 0;"></p>
Raffelt, David, Thijs Dhollander, J-Donald Tournier, Rami Tabbara, Robert E Smith, Eric Pierre, and Alan Connelly. 2017. “Bias Field Correction and Intensity Normalisation for Quantitative Analysis of Apparent Fibre Density.” In Proc. Intl. Soc. Mag. Reson. Med, 25:3541.
<p style="margin: 2px 0;"></p>
Tournier, J-Donald, Fernando Calamante, David G Gadian, and Alan Connelly. 2004. “Direct Estimation of the Fiber Orientation Density Function from Diffusion-Weighted Mri Data Using Spherical Deconvolution.” NeuroImage 23 (3). Elsevier: 1176–85.
<p style="margin: 2px 0;"></p>
Tournier, J-Donald, Chun-Hung Yeh, Fernando Calamante, Kuan-Hung Cho, Alan Connelly, and Ching-Po Lin. 2008. “Resolving Crossing Fibres Using Constrained Spherical Deconvolution: Validation Using Diffusion-Weighted Imaging Phantom Data.” Neuroimage 42 (2). Elsevier: 617–25.
<p style="margin: 2px 0;"></p>
Yeh, Fang-Cheng. 2020. “Shape Analysis of the Human Association Pathways.” Neuroimage 223. Elsevier: 117329.
<p style="margin: 2px 0;"></p>
Yeh, Fang-Cheng, Van Jay Wedeen, and Wen-Yih Isaac Tseng. 2010. “Generalized q-Sampling Imaging.” IEEE Transactions on Medical Imaging 29 (9). IEEE: 1626–35.
</div>
</details>


<br>
Preprocessed diffusion data (QSIPrep outputs) were further analyzed using **[QSIRecon](https://qsirecon.readthedocs.io/en/latest/)**, which executes reconstruction workflows defined in a `recon-spec` YAML file. This file specifies reconstruction steps, parameter settings, post-processing tools, and software dependencies. We used a `recon-spec` file for AutoTrack bundle reconstruction and bundle-wise statistics ([Bundle Stats](#bundle-stats)).

## Bundle Stats

Diffusion tensors were estimated with TORTOISE, and diffusion orientation distribution functions (ODFs) were reconstructed using two approaches: generalized q-sampling imaging (GQI) in DSI Studio and single-shell three-tissue constrained spherical deconvolution (SS3T-CSD) in MRtrix3. AutoTrack tractography was applied to both [**GQI**](https://qsirecon.readthedocs.io/en/latest/builtin_workflows.html#dsi-studio-autotrack) and [**SS3T**](https://qsirecon.readthedocs.io/en/latest/builtin_workflows.html#ss3t-fod-autotrack) reconstructions to delineate major white matter tracks. For each method, bundle-wise mean values were computed for [GQI and tensor scalars](https://qsirecon.readthedocs.io/en/latest/builtin_workflows.html#id36).

 * `recon-spec` for [single-shell data](https://github.com/PennLINC/AI2D/blob/main/_data/reconspec_singleshell_bundle-stats_v1.yaml)
 * `recon-spec` for [multi-shell data](https://github.com/PennLINC/AI2D/blob/main/_data/reconspec_multishell_bundle-stats_v1.yaml)

## Boilerplate

<div class="alert alert-primary" role="alert">
  <strong>IMPORTANT:</strong> The exact <strong>QSIRecon</strong> pipeline is documented in the <em>boilerplate</em> located at <code>&lt;QSIRecon_output&gt;/logs/CITATION.html</code>. If the data were processed with <a href="{{ site.baseurl }}/docs/imaging/image_babs/"><strong>BABS</strong></a> (i.e., were zipped), refer to <a href="{{ site.baseurl }}/docs/get_data#312-explore-the-data-structure"><strong>Get Data</strong></a> for details on unzipping <code>&lt;QSIRecon_output&gt;</code> to access the boilerplate file.
</div>