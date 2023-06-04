# NPtransDVC
Code for digital volume correlation of 3D grain structures and analysis of nano particle transport and retention in porous media.

The repository consists of multible python scripts.
DVC_registerMultiscale, analysis, and calculate_mean_sum_of_squared_differences.

The DVC_registerMultiscale performs at image registration between all volumes and a reference volume. It then transforms the reference volume to
minimize the error function by appliying a phi. Additionally it produces the difference images used for analysis. To use the script, a series of volume has
to be loaded. The binning should also be defined.

The calculate_mean_sum_of_squared_differences can be used for calculating the error function values between differently correlated image data. To run the
the corrected t0 images should be loaded as well as the time step 1 and time step 2 image data.

The analysis script takes care of segmenting the nanoparticle phase using the difference images. To run the script, the t0 images should be loaded as well as
the difference images resulting from the DVC_registerMultiscale script. The t0 grain mask should also be loaded. The script should ideally be run as a notebook, one section as a time. The threshold used for segmenting the NP-phase in the difference images is found i a different way than in the thesis handed in, to correct for oversegmentation.

