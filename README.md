# IGIMF_theory_codes
This repository contains codes to generate data samples of stars for star clusters or even whole galaxies. It is based on the IGIMF theory and similar to the [galIMF](https://github.com/Azeret/galIMF) code by Yan Zhiqiang et al. In contrast to their module, the main focus of the provided codes are sub-galactic regions, especially composite IMFs, instead of galaxy-wide stellar populations. Further, the provided codes calculate the discrete stellar masses instead of histograms. This allows for more exact simulations of dynamical processes within star-forming regions, such as dynamical ejections.

For a general introduction to the IGIMF theory and Optimal sampling, it is suggested to read the supplementary pdf.\
This file also contains the mathematics concerning a reformulation of the Optimal sampling in order to generate star cluster samples with a fixed most massive cluster mass. This may be useful to more easily create cluster distributions that match observational samples, especially on sub-galactic scales where the local most massive cluster mass won't always be the mass of the most massive cluster that formed galaxy-wide. This sampling procedure is not constrained to only the generation of star clusters but can also be used to generate e.g. molecular cloud masses and may therefore also be useful e.g. for the ICIMF theory.\
Opposed to quantile-based sampling it does not take the number of data points $N$ as input, but the desired properties of the generated data (total sum, value of the largest data point).\
A generalized formulation and possible uses of this algorithm may be covered in the future.

It is further suggested to read the supplementary document of the galIMF module.

## Contents

* IMF_sampling: Generates optimally sampled stellar Initial Mass Functions (IMFs)
* ECMF_sampling: Generates optimally sampled Embedded Cluster Mass Functions (ECMFs) within the IGIMF theory as well as custom star cluster samples
* cIMF_and_IGIMF_sampling: Generates optimally sampled Integrated Galactic IMFs (IGIMFs) and custom composite IMFs (cIMFs)
* cIMF_generating_optimal: Calculates the optimally sampled cIMF of a custom star cluster sample. Allows to investigate the cIMF form without drawing stellar masses
* cIMF_generating_random: Similar to cIMF_generating_optimal but for randomly sampled stellar IMFs. Allows for comparison between optimally and randomly sampled cIMFs

All code is provided in the form of jupyter notebook files.

## Caution

The codes were not yet tested independently, so currently caution is advised when using them.
