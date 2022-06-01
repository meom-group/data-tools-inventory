# Model codes

## Ocean models

<details>
  <summary> <a href="https://www.nemo-ocean.eu/"> NEMO OGCM </a> </summary>
  
NEMO is a primitive equation model designed for performing oceanic general circulation simulations. It includes a sea ice component (SI3), a passive tracer component (TOP) 
interfaced with bio-geochemical models (PISCES) and other passive tracer models (CFC11, CO2, etc...). Adaptative mesh refinement is available in NEMO through the AGRIF package.

In MEOM, [Drakkar Configurations Manager (DCM)](https://github.com/meom-group/DCM) has been developped in order to ease the deployment of NEMO based configurations. DCM provides 
both an environment for code developpement and setup (DCMTOOLS) and an environment for production at runtime (RUNTOOLS). In addition, a series of bash scripts (dcm_toolkit) were
developped for helping the managment of simulations.

DCM is supporting historical NEMO versions (since NEMO 1.12). The actual version corresponds to NEMO 4.0.6 but branches for 4.0.7 and 4.2.0 are also operational.

</details>

## Ice models

<details>
  <summary> <a href="https://forge.ipsl.jussieu.fr/nemo/chrome/site/doc/SI3/manual/pdf/SI3_manual.pdf"> SI3 </a> </summary>
  
Sea Ice modelling Integrated Initiative (SI3) is the NEMO sea ice engine ...

</details>

<details>
  <summary> <a href="https://tc.copernicus.org/articles/10/1055/2016/tc-10-1055-2016.pdf"> neXtSIM </a> </summary>
  
neXtSIM is a fully Lagrangian dynamical/thermodynamical sea ice model developped at NERSC, Norway

</details>


<details>
  <summary> <a href="https://nextsim-dg.readthedocs.io/en/latest/?badge=latest"> neXtSIM_DG </a> </summary>
  
neXtSIM_DG is the Eulerian version of the neXtSIM model, using the discontinuous Galerkin method (DG) for advection, instead of the Lagrangian scheme. It is cuurently in development in the framework of [SASIP](https://sasip-climate.github.io/)
