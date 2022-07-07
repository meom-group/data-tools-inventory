# Model codes

## Modelling framework

<details>
  <summary> <a href="https://www.nemo-ocean.eu/"> NEMO </a> standing for "Nucleus for European Modelling of the Ocean" is a state-of-the-art modelling framework for research activities and forecasting services in ocean and climate sciences, developed in a sustainable way by a European consortium. </summary>

The NEMO ocean model has 3 major components: NEMO-OCE models the ocean {thermo}dynamics and solves the primitive equations NEMO-ICE (SI3: Sea-Ice Integrated Initiative) models sea-ice {thermo}dynamics, brine inclusions and subgrid-scale thickness variations and NEMO-TOP (Tracers in the Ocean Paradigm) models the {on,off}line oceanic tracers transport and biogeochemical processes.
  
Go to the #ocean-models and the #ice-models sections to have more details about NEMO-OCE and SI3

</details>

## Ocean models

<details>
  <summary> <a href="https://zenodo.org/record/6334656#.YsbRaOxByBQ"> NEMO ocean engine </a> is a primitive equation model designed for performing oceanic general circulation simulations. </summary>

This primitive equation model is adapted to regional and global ocean circulation problems down to kilometric scale. Prognostic variables are the three-dimensional velocity field, a non-linear sea surface height, the Conservative Temperature and the Absolute Salinity. In the horizontal direction, the model uses a curvilinear orthogonal grid and in the vertical direction, a full or partial step z-coordinate, or s-coordinate, or a mixture of the two. The distribution of variables is a three-dimensional Arakawa C-type grid. Various physical choices are available to describe ocean physics, so as various HPC functionalities to improve performances.
  
NEMO also includes a sea ice component (SI3), a passive tracer component (TOP) interfaced with bio-geochemical models (PISCES) and other passive tracer models (CFC11, CO2, etc...). Adaptative mesh refinement is available in NEMO through the AGRIF package.

</details>

## Ice models

<details>
  <summary> <a href="https://forge.ipsl.jussieu.fr/nemo/chrome/site/doc/SI3/manual/pdf/SI3_manual.pdf"> Sea Ice modelling Integrated Initiative (SI3) </a> is a flexible tool for studying the sea ice dynamics and thermodynamics, as well as its interactions with the other components of the Earth climate system over a wide range of space and time scales.</summary>
  
Designed for global to regional applications up to 10 km of effective resolution, SI3 is a curvilinear grid, finite-difference implementation of the classical AIDJEX model (Arctic Ice Dynamics Joint EXperiment), combining the conservation of momentum for viscous-plastic continuum, energy and salt-conserving halo-thermodynamics, an explicit representation of subgrid-scale ice thickness variations, snow and melt ponds. An option to switch back to the single-category (or 2-level) framework provides a cheap sea ice modelling solution.

</details>

<details>
  <summary> <a href="https://tc.copernicus.org/articles/10/1055/2016/tc-10-1055-2016.pdf"> neXtSIM </a> is a fully Lagrangian dynamical/thermodynamical sea ice model developped at NERSC, Norway </summary>
  
</details>


<details>
  <summary> <a href="https://nextsim-dg.readthedocs.io/en/latest/?badge=latest"> neXtSIM_DG </a> is the Eulerian version of the neXtSIM model, using the discontinuous Galerkin method (DG) for advection, instead of the Lagrangian scheme.</summary>
  
It is cuurently in development in the framework of [SASIP](https://sasip-climate.github.io/)
  
    
</details>

