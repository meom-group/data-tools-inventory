# Model Input for simulations.

# NEMO based simulations:
Model input for simulations are of many kinds: 
  * **Parameter input files** such as namelist files of XIOS xml files. These files are kept in the [meom-configurations](https://github.com/meom-configurations) repository on GitHub.
  * **Configuration files**  corresponding to a specific configuration, in fact valid for a  particular domain and resolution. These (often large) files are kept 
on our local `ige-meom-cal1` server under `/mnt/meom/MODEL_SET/` directory, following Drakkar nomenclature (example : eORCA12/eORCA12-I/ ). These files can 
be made available through the [meom opendap server](https://ige-meom-opendap.univ-grenoble-alpes.fr/thredds). 
Recent publications policy requires a free access to some of these data. In this case, using a DOI with zenodo can be considered.
    * Note that initial conditions files (for T and S, for instance) are part of this kind of data. If they come from CMEMS of MOI some license agreement might be necessary, before use.
  * **Forcing files** like atmospheric reanalysis of other forcing data set. In general, these data can be used by different model configurations (and even by different model). They are 
kept locally on our local `ige-meom-cal1` server under `/mnt/meom/DATA_SET/FORCING_ATMOSPHERIQUE/`directory. Note that depending on the provider (ECMWF, JRA55...) users may need 
to be officially registed in order to use the products. In this sense, MEOM is not a data provider for these data set.
