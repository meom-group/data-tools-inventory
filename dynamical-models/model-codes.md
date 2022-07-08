# Model codes

*click on the arrows to have more informations*

## Modelling framework

<details>
  <summary><strong><a href="https://www.nemo-ocean.eu/"> NEMO </a> standing for "Nucleus for European Modelling of the Ocean" is a state-of-the-art modelling framework for research activities and forecasting services in ocean and climate sciences, developed in a sustainable way by a European consortium.</strong></summary>

<hr style="border:1px solid blue">  
  
The NEMO ocean model has 3 major components: NEMO-OCE models the ocean {thermo}dynamics and solves the primitive equations NEMO-ICE (SI3: Sea-Ice Integrated Initiative) models sea-ice {thermo}dynamics, brine inclusions and subgrid-scale thickness variations and NEMO-TOP (Tracers in the Ocean Paradigm) models the {on,off}line oceanic tracers transport and biogeochemical processes. Adaptative mesh refinement is available in NEMO through the AGRIF package (go to the [external modules](#external-modules) section pour more information
    
  
Go to the [Ocean models](#ocean-models), the [Sea ice models](#sea-ice-models) and the [Biogeochemical models](#biogeochemical-models) sections to have more details about NEMO-OCE, SI3 and PISCES

In the MEOM team, this modelling framework is widely used for :
  * realistic global or regional simulations of the ocean and the sea-ice,   
  * stochastic ensemble runs of ocean, sea-ice and biogechestry
  * ...
  
Got to [the configuration information page](https://github.com/meom-group/data-tools-inventory/blob/main/dynamical-models/model-configurations.md) for a description of the scripts needed to run NEMO and to the [the simulation data page](https://github.com/meom-group/data-tools-inventory/blob/main/dynamical-models/simulation-data.md) for informations on where to find and how to build configuration files.
  
<hr style="border:1px solid blue">  
</details>

## Ocean models

<details>
  <summary><strong> <a href="https://zenodo.org/record/6334656#.YsbRaOxByBQ"> NEMO ocean engine </a> is a primitive equation model designed for performing oceanic general circulation simulations.</strong> </summary>

<hr style="border:1px solid blue">  

This primitive equation model is adapted to regional and global ocean circulation problems down to kilometric scale. Prognostic variables are the three-dimensional velocity field, a non-linear sea surface height, the Conservative Temperature and the Absolute Salinity. In the horizontal direction, the model uses a curvilinear orthogonal grid and in the vertical direction, a full or partial step z-coordinate, or s-coordinate, or a mixture of the two. The distribution of variables is a three-dimensional Arakawa C-type grid. Various physical choices are available to describe ocean physics, so as various HPC functionalities to improve performances.
  
In MEOM team, NEMO ocean model is usually coupled to SI3 or neXtSIM sea ice models and sometimes to PISCES.
  
<hr style="border:1px solid blue">  
</details>

## Sea ice models

<details>
  <summary><strong> <a href="https://forge.ipsl.jussieu.fr/nemo/chrome/site/doc/SI3/manual/pdf/SI3_manual.pdf"> Sea Ice modelling Integrated Initiative (SI3) </a> is a flexible tool for studying the sea ice dynamics and thermodynamics, as well as its interactions with the other components of the Earth climate system over a wide range of space and time scales.</strong></summary>
 
<hr style="border:1px solid blue">  

Designed for global to regional applications up to 10 km of effective resolution, SI3 is a curvilinear grid, finite-difference implementation of the classical AIDJEX model (Arctic Ice Dynamics Joint EXperiment), combining the conservation of momentum for viscous-plastic continuum, energy and salt-conserving halo-thermodynamics, an explicit representation of subgrid-scale ice thickness variations, snow and melt ponds. An option to switch back to the single-category (or 2-level) framework provides a cheap sea ice modelling solution.
    
<hr style="border:1px solid blue">  
</details>

<details>
  <summary><strong> The <a href="https://tc.copernicus.org/articles/10/1055/2016/tc-10-1055-2016.pdf"> neXt generation Sea Ice Model (neXtSIM) </a> is a Lagrangian dynamical-thermodynamical sea-ice model that faithfully represents large-scale sea ice thickness, concentration and drift patterns, statistical properties of pack ice deformation and drift, diffusion and dispersion </strong></summary>
 
<hr style="border:1px solid blue">  
  
 neXtSIM exhibits a strong capacity for short-term sea ice forecasting at Pan-Arctic scales 6 . neXtSIM was developed to explore the role of sea-ice mechanics and dynamics in determining the large-scale behaviour of Arctic sea ice. As such, it has served as a testing and development ground for the brittle sea-ice rheologies developed over the past decade.
  
 In MEOM team, neXtSIM is coupled to the NEMO ocean engine or in a standalone mode.
  
<hr style="border:1px solid blue">  
  
</details>


<details>
  <summary><strong> <a href="https://nextsim-dg.readthedocs.io/en/latest/?badge=latest"> neXtSIM_DG </a> is the Eulerian version of the neXtSIM model, using the discontinuous Galerkin method (DG) for advection, instead of the Lagrangian scheme.</strong></summary>
    
<hr style="border:1px solid blue">  

neXtSIM_DG is cuurently in development in the framework of [SASIP project](https://sasip-climate.github.io/)
  
The DG method that has proven extremely effective and efficient in retaining high gradients in fluid dynamics.
  
With the new version we aim to extend the use of the model to fully coupled and global simulations, resulting in a model that can be used from regional short term forecasting applications to global climate simulations. To achieve this, the model infrastructure will be modular and flexible, so that it can easily be coupled to other models and systems and so that new parameterisations and physical routines can easily be added. The dynamical core will use the DG method to ensure the best possible preservation of high gradients in an Eulerian framework, while still maintaining good computational performance.
  
<hr style="border:1px solid blue">  
</details>

## Biogeochemical models

<details>
  <summary><strong> <a href="https://gmd.copernicus.org/articles/8/2465/2015/gmd-8-2465-2015.pdf"> PISCES </a> s a biogeochemical model that simulates marine biological productivity and describes the biogeochemical cycles of carbon and of the main nutrients (P, N, Si, Fe). </strong></summary>
 
<hr style="border:1px solid blue">  

It is the marine biogeochemistry component of two ocean modeling platforms (NEMO and CROCO), three Earth System models (IPSL-CM, CNRM-CM and EC-Earth) and one operational oceanographic system (MERCATOR-Ocean).
    
<hr style="border:1px solid blue">  
</details>

## External modules


<details>
  <summary><strong> <a href="https://forge.ipsl.jussieu.fr/ioserver"> XML-IO-Server (XIOS) </a> is a library dedicated to input and output management of climate code</strong></summary>
 
<hr style="border:1px solid blue">  
This library outsources the management of output diagnostic and allows some temporal and spatial post-processing operations. It aims at improving flexibility and perfomance.
    
<hr style="border:1px solid blue">  
</details>

<details>
  <summary><strong> The <a href="https://gmd.copernicus.org/articles/10/3297/2017/gmd-10-3297-2017.pdf"> OASIS </a> coupler is a software allowing synchronized exchanges of coupling information between numerical codes representing different components of the climate system </strong></summary>
 
<hr style="border:1px solid blue">  

When interfaced with the Model Coupling Toolkit (MCT), OASIS3-MCT offers a fully parallel implementation of coupling field regridding and exchange. Low-intrusiveness, portability and flexibility are OASIS3-MCT key design concepts. 
    
<hr style="border:1px solid blue">  
</details>


<details>
  <summary><strong> <a href="http://agrif.imag.fr/"> AGRIF </a> is a Fortran 90 package for the integration of full adaptative mesh refinement (AMR) features within a multidimensional finite difference model. </strong></summary>
 
<hr style="border:1px solid blue">  
Its main objective is to simplify the integration of these capacities in an existing model with almost no changes in this one. 


    
<hr style="border:1px solid blue">  
</details>
