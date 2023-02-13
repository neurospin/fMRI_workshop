# Advanced encoding notebooks
Here is a selection of notebook to explore advanced topic, from the nilearn documentation. These notebook can be run on on binder.

[Explore predicted and residual signals](https://nilearn.github.io/stable/auto_examples/04_glm_first_level/plot_predictions_residuals.html)  
This notebook:
* uses the higher-level class FirstLevelModel that combines a number of things (design matrix specification, masking, smoothing...) and sets the floors for the model fit. Those different steps were split (using lower-level classes/functions) in the notebook basic_encoding.ipynb.
* demonstrates how to extract the signal from a spherical region of interest
* plots predicted and observed timeseries, and the histogram of residuals.

[Second level analysis with multiple comparison correction](https://nilearn.github.io/stable/auto_examples/05_glm_second_level/plot_second_level_one_sample_test.html)  
This script shows an example of group-level inference, and correction for multiple comparisons based on the Bonferroni method, and based on a non-parametric (permutation) test that takes into account the smoothness of the data.
The function used for non-parametric inference implements: 
* voxel-level inference, with FWER correction (see the [FSL documentation](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/Randomise/Theory) for more details)
* cluster-level inference with FWER correction, which requires to fix a cluster-forming threshold [Oostenveld et al 2011](https://doi.org/10.1155/2011/720971). This is the example provided in the notebook.
* a combined voxel-cluster based method with FWER correction that does not require to fix a cluster-forming threshold [Smith & Nichols, 2008](https://doi.org/10.1016/j.neuroimage.2008.03.061)

[An example using the BIDS format](https://nilearn.github.io/stable/auto_examples/04_glm_first_level/plot_bids_features.html)  
* show how to easily construct a design matrix and estimate a contrast when the data has a BIDS format
* get the stat/cluster table
* automatically save the contrast estimation using the BIDS format

[More options for design matrix specification](https://nilearn.github.io/stable/auto_examples/04_glm_first_level/plot_first_level_details.html)  
This notebook explores:
* changes in the drift model included in the design matrix
* changes in the hemodynamic response model
* addings time and dispersion derivatives of the hemodynamic response function
* the F-test
* changes the noise model
* changes the confounds
* example of volume censoring (link to fMRIPrep)
* changes the spatial smoothing of the data

The nilearn documentation provides more examples for [first level](https://nilearn.github.io/stable/auto_examples/04_glm_first_level/index.html) and [second level](https://nilearn.github.io/stable/auto_examples/05_glm_second_level/index.html) analyses.
