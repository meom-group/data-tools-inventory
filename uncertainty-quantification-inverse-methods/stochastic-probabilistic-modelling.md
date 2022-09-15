# Stochastic/probabilistic modelling

*click on the arrows to have more informations*

<details>
  <summary><strong>Probabilistic NEMO (with <a href="http://doi.org/10.5281/zenodo.61611">NEMOv3.5</a> and <a href="http://doi.org/10.5281/zenodo.6303007">NEMOv4.0</a>). This includes additional/modified NEMO modules to perform ensemble simulations (members running in parallel) and to explicitly simulate model uncertainties (with stochastic parameterizations).</strong></summary>

<hr style="border:1px solid blue">

Ensemble simulations are performed by defining one MPI communicator for each instance of the NEMO code (ensemble members), as described in <a href="http://dx.doi.org/10.5194/gmd-10-1091-2017">Bessières et al. (2017)</a>. The code includes the possibility of defining cross-members comunicators to allow the exchange of information between members (for instance to compute ensemble statistics).

Stochastic parameterizations are implemented as described in <a href="http://dx.doi.org/10.5194/gmd-8-1285-2015">Brankart et al. (2015)</a>. They include:
  * the simulation of uncertainties resulting from the effect of unresolved scales in the seawater equation of state <a href="http://dx.doi.org/10.1016/j.ocemod.2013.02.004">(Brankart, 2013)</a>,
  * the simulation of uncertainties in the PISCES biogeochemical model (<a href="http://dx.doi.org/10.1016/j.jmarsys.2015.10.012">Garnier et al., 2016)</a>,
  * the simulation of location uncertainties resulting from unresolved processes (<a href="https://os.copernicus.org/preprints/os-2022-11/">Leroux, 2022)</a>.

Applications of these tools can be found for instance in <a href="http://dx.doi.org/10.5194/os-11-425-2015">Candille et al. (2015)</a>, <a href="https://doi.org/10.1175/JTECH-D-19-0002.1">Germineaud et al. (2019)</a>, <a href="https://doi.org/10.5194/os-15-443-2019">Tissier et al. (2019)</a>, <a href="https://doi.org/10.1002/qj.3397">Zanna et al. (2019)</a>, <a href="https://doi.org/10.5194/os-16-1297-2020">Santana-Falcon et al. (2020)</a>.

<hr style="border:1px solid blue">
</details>

