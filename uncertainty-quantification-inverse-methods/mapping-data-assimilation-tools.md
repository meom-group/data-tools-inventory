# Mapping and data assimilation tools

*click on the arrows to have more information*

## Toolboxes

<details>
  <summary><strong><a href="https://github.com/brankart/ensdam">EnsDAM</a> is a collection of FORTRAN modules that can be used in ensemble data assimilation systems or, more generally in ensemble estimation problems.</strong></summary>

<hr style="border:1px solid blue">

The library includes the following tools:
  * Ensemble Bayesian update, using an MCMC sampler, with covariance localization (<a href="https://doi.org/10.3389/fams.2019.00058">Brankart, 2019</a>),
  * Ensemble augmentation, with covariance localization (<a href="https://doi.org/10.3389/fams.2019.00058">Brankart, 2019</a>),
  * Ensemble anamorphosis (<a href="http://www.ocean-sci.net/6/247/2010/">Béal et al., 2010</a>; <a href="http://dx.doi.org/10.5194/os-8-121-2012">Brankart et al., 2012</a>; <a href="https://doi.org/10.3389/fams.2019.00058">Brankart, 2019</a>)
  * Ensemble scores (<a href="http://dx.doi.org/10.5194/os-11-425-2015">Candille et al., 2015</a>; <a href="https://doi.org/10.1175/JTECH-D-19-0002.1">Germineaud et al., 2019</a>; <a href="https://doi.org/10.3389/fams.2019.00058">Brankart, 2019</a>),
  * Scale separation (<a href="https://doi.org/10.5194/os-15-443-2019">Tissier et al., 2019</a>),
  * Generation of stochastic fields,
  * etc.

<hr style="border:1px solid blue">
</details>

<details>
  <summary><strong><a href="https://github.com/brankart/sesam">SeSAM</a> is a FORTRAN program to perform various operations needed in data assimilation systems, or more generally in inverse problems. SeSAM is a user interface to the tools of the EnsDAM library (using data from NetCDF files rather than data arrays), but also provides older tools that are not included in EnsDAM.</strong></summary>

<hr style="border:1px solid blue">

The program includes an interface to the tools of the EnsDAM library
and also the following tools (not included in EnsDAM):
  * Ensemble Bayesian update, using the analysis step of the SEEK filter (slightly modified to be equivalent to the analysis step of the Ensemble Tranform Kalman Filter),
  * Modified algorithm using domain localization (developed in <a href="http://dx.doi.org/10.1016/S0924-7963(03)00022-8">Testut et al., 2003</a>; <a href="http://dx.doi.org/10.1029/2001JC001198">Brankart et al., 2003</a>, and still recently applied for instance in <a href="https://doi.org/10.5194/os-15-443-2019">Tissier et al., 2019</a>; <a href="https://doi.org/10.1175/JTECH-D-19-0002.1">Germineaud et al., 2019</a>; <a href="https://doi.org/10.3389/fmars.2019.00822">Metref et al., 2020</a>; <a href="https://doi.org/10.5194/os-16-1297-2020">Santana-Falcon et al., 2020</a>),
  * Generalization of the algorithm to truncated Gaussian distributions (<a href="http://dx.doi.org/10.1016/j.ocemod.2008.10.007">Lauvernet et al., 2009</a>),
  * Generalization of the algorithm to correlated observation errors (<a href="http://dx.doi.org/10.1175/2008MWR2693.1">Brankart et al., 2009</a> ; <a href="http://dx.doi.org/10.1175/JTECH-D-16-0048.1">Ruggiero al., 2016</a>),
  * Generalization of the algorithm to adaptive statistics (<a href="http://dx.doi.org/10.1175/2009MWR3085.1">Brankart et al., 2010</a>),
  * Empirical Orthogonal Fonctions (EOF) décomposition,
  * Interface to observation databases.

<hr style="border:1px solid blue">
</details>

## Inversion tools

<details>
  <summary><strong>LETKF/SEEK analysis step, in the <a href="https://github.com/brankart/sesam">SeSAM</a> toolbox.</strong></summary>

<hr style="border:1px solid blue">

This tool applies the LETKF/SEEK observational update algorithm to condition a prior ensemble to observations.

The input is an ensemble of model states (in 1D, 2D, 3D or 4D) and an observation vector.

The output is the updated ensemble (condtioned to the observations).

The main parameters controls the observation error standard deviation and the localization of the ensemble covariance.

<hr style="border:1px solid blue">
</details>

<details>
  <summary><strong>MCMC sampler, in the <a href="https://github.com/brankart/ensdam">EnsDAM</a> and <a href="https://github.com/brankart/sesam">SeSAM</a> toolboxes.</strong></summary>

<hr style="border:1px solid blue">

This tool applies the MCMC sampler algorithm (proposed in <a href="https://doi.org/10.3389/fams.2019.00058">Brankart, 2019</a>) to condition a prior ensemble to observations.

The input is an multiscale ensemble of model states (in 1D, 2D, 3D or 4D) and an observation vector.

The output is a sample of the posterior probability distribution (condtioned to the observations).

The main parameters controls the observation error standard deviation and the localization of the ensemble covariance.

The program can be adjusted to include additional conditions to the posterior probabilty distribution.

<hr style="border:1px solid blue">
</details>

<details>
  <summary><strong>Ensemble analysis of altimetric observations, in the <a href="https://github.com/brankart/ensemble-altimetry">ensemble-altimetry</a> repository, based on the MCMC sampler included in the <a href="https://github.com/brankart/ensdam">EnsDAM</a> and <a href="https://github.com/brankart/sesam">SeSAM</a> toolboxes.</strong></summary>

<hr style="border:1px solid blue">

This tool applies the MCMC sampler algorithm (proposed in <a href="https://doi.org/10.3389/fams.2019.00058">Brankart, 2019</a>) to produce an ensemble analysis of altimetric observations.

The tool is a collection of shell scripts to be run successively to obtain the result from the data.

Input data are along-track altimetric data (L3 product) used as observations, and mapped altimetric data (L4 product) used as a climatological prior ensemble.

Output data is a sample of the posterior distribution for the following fields (in 2D + time): absolute dynamic topography, velocity, relative vorticity and material derivative of the potential vorticity.

Probabilistic scores comparing the ensemble solution to independent observations can also be computed.

The main parameters controls the observation error standard deviation and the localization of the ensemble covariance.

<hr style="border:1px solid blue">
</details>

## Transformation tools

<details>
  <summary><strong>Ensemble anamorphosis, in the <a href="https://github.com/brankart/ensdam">EnsDAM</a> and <a href="https://github.com/brankart/sesam">SeSAM</a> toolboxes.</strong></summary>

<hr style="border:1px solid blue">

This tool computes and applies the anamorphosis transformation (described in <a href="http://dx.doi.org/10.5194/os-8-121-2012">Brankart et al., 2012</a>) to transform the marginal distributions of a given input ensemble into a specified distribution (usually a normalize Gaussian distribution). The transformation can then be applied to model state or observation vectors.

The first step is to compute the quantiles of the input ensemble (defining the piecwise linear anamorphosis transformation). The input is the ensemble; and the output is the set of required quantiles.

The second step is apply the transformation. The input is the vector to transform, and the output is the transformed vector.

The main parameters are the list of quantiles used to specify the transformation (for instance, the deciles) and the quantiles of the target marginal distribution.

<hr style="border:1px solid blue">
</details>

<details>
  <summary><strong>Ensemble augmentation, in the <a href="https://github.com/brankart/ensdam">EnsDAM</a> and <a href="https://github.com/brankart/sesam">SeSAM</a> toolboxes.</strong></summary>

<hr style="border:1px solid blue">

This tool applies the MCMC sampler algorithm (proposed in <a href="https://doi.org/10.3389/fams.2019.00058">Brankart, 2019</a>) to augment an input ensemble with new members with the same covariance matrix, with localization applied to dismiss long-range correlations. Combined with the anamorphosis tools, this can generate new ensemble members with the same marginal distribution and the same local rank correlation structure.

The input is an multiscale ensemble of model states (in 1D, 2D, 3D or 4D).

The output is an additional sample with the same covariance (with localization).

The main parameters controls localization of the ensemble covariance.

<hr style="border:1px solid blue">
</details>

<details>
  <summary><strong>Scale separation, in the <a href="https://github.com/brankart/ensdam">EnsDAM</a> and <a href="https://github.com/brankart/sesam">SeSAM</a> toolboxes.</strong></summary>

<hr style="border:1px solid blue">

This tool computes the spectrum of an input model state in the basis of the spherical harmonics.

Automatic iteration on 2D slices is applied if the tool is provided with a 3D or 4D state or with an ensemble of states.

The forward transformation compute the spectrum (for each slice and each member of the ensemble).

The backward transformation reconstruct the model state from the spectrum. Scale sepraration is then obtained by limiting the range of spherical harmonics used in the reconstruction.

<hr style="border:1px solid blue">
</details>

<details>
  <summary><strong>EOF decomposition, in the  <a href="https://github.com/brankart/sesam">SeSAM</a> toolbox.</strong></summary>

<hr style="border:1px solid blue">

This tool computes the EOF decomposition of an ensemble of model states (in 1D, 2D, 3D or 4D).

The input is an ensemble of model states. The output is the required number of EOFs.

The main parameters controls the metrics that is used to perform the decomposition (i.e. the relative importance to give to different state variables, especially if they have different dimensions).

This tool does not require that the whole ensemble be stored in memory (it is read twice if needed), and can thus be applied to large state vectors.

<hr style="border:1px solid blue">
</details>

## Utilities

<details>
  <summary><strong>Prepare observation operator, in the <a href="https://github.com/brankart/sesam">SeSAM</a> toolbox.</strong></summary>

<hr style="border:1px solid blue">

This tool extract observations from observation databases in their native NetCDF format, and prepare them to be used by the other tools.

This includes the localization of each observation in the model grid and the computation of the interpolation coefficients (to move from the model grid to observation locations) defining the observation operator.

<hr style="border:1px solid blue">
</details>

<details>
  <summary><strong>Prepare localization bubbles, in the <a href="https://github.com/brankart/sesam">SeSAM</a> toolbox.</strong></summary>

<hr style="border:1px solid blue">

This tool prepares the localization bubbles to be used in the LETKF/SEEK observational update algorithm (if localization is required).

<hr style="border:1px solid blue">
</details>

<details>
  <summary><strong>Generation of random fields, in the <a href="https://github.com/brankart/ensdam">EnsDAM</a> and partly in the <a href="https://github.com/brankart/sesam">SeSAM</a> toolbox.</strong></summary>

<hr style="border:1px solid blue">

This tool is dedicated to the generaton of random numbers, random fields, or stochastic processes of various types, to be used in stochastic modelling or data assimilation systems.  This includes:
 * the generation of random numbers with various probability distribution (uniform, normal, gamma, beta, exponential, truncated exponential, truncated normal);
 * the computation of the probabilty density function (pdf), the cumulative distribution function (cdf) or the inverse cdf of several probability distributions (normal, gamma, beta);
 * the computation of the cdf of the product of two normal random numbers;
 * the transformation of a normal random variable into a gamma or a beta random variable, and the transformation of the product of two normal random variables into a normal variable;
 * the generation of random fields with specified spectrum (in 1D, in 2D or in the basis of the spherical harmonics).

<hr style="border:1px solid blue">
</details>

<details>
  <summary><strong>Computation of ensemble correlations, in the <a href="https://github.com/brankart/sesam">SeSAM</a> toolbox.</strong></summary>

<hr style="border:1px solid blue">

This tool computes the ensemble correlation with respect to one of the variable.

The input is the ensemble of model state and the index of the reference variable.

The output is a model state vector with the correlation with respect to this reference variable.

<hr style="border:1px solid blue">
</details>

