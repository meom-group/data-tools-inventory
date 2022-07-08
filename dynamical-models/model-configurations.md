# Model configurations


*click on the arrows to have more informations*

## NEMO configurations

<details>
  <summary> <strong>NEMO based configurations are described in dedicated <a href="https://github.com/meom-configurations"> meom-configuration repository </a> on GitHub.  </strong></summary>
  

<hr style="border:1px solid blue">  
  
Using the information found there, one should be able to reconstruct a particular configuration. However, as far as fortran compilers may evolve 
in time, the exact reproducibility is not granted.   
In the meom-configuration repository, the following information can be found for each configuration:
  * reference for building source code
  * relevant namelist files for running experiments
  * relevant xml files for XIOS model output
  * relevant information on the required input data files.

  
In MEOM, [Drakkar Configurations Manager (DCM)](https://github.com/meom-group/DCM) has been developped in order to ease the deployment of NEMO based configurations. DCM provides both an environment for code developpement and setup (DCMTOOLS) and an environment for production at runtime (RUNTOOLS). In addition, a series of bash scripts (dcm_toolkit) were developped for helping the managment of simulations.

  
DCM is supporting historical NEMO versions (since NEMO 1.12). The actual version corresponds to NEMO 4.0.6 but branches for 4.0.7 and 4.2.0 are also operational.

  
<hr style="border:1px solid blue">  
  
 </details>
