# Martes Caurina SSA

Lilah, Kayli, Louis, Sidra

## Overview

- Creating Species Occurence Maps and Species Distribution Models for Species Status Assessment of Martes Caurina

## Dependencies 

The following  R packages are required (these will be installed in each file where necessary):
- raster
- dismo
- spocc
- rJava
- tidyverse
- maps
- maptools

## Structure

### Data
  + wc2-5: climate data at 2.5 minute resolution from [WorldClim](http://www.worldclim.org) (_note_: this folder is not under version control, but will be created by running the setup script (`scr/setup.R`))
  + cmip5: forcast climate data at 2.5 minute resolution from [WorldClim](http://www.worldclim.org). The data are for the year 2070, based on the GFDL-ESM2G model with an RCP of 4.5 CO<sub>2</sub>. For an examination of different forecast models, see [McSweeney et al. 2015](https://link.springer.com/article/10.1007/s00382-014-2418-8). (_note_: this folder is not under version control, but will be created by running the currentsdm script (`scripts/currentsdm.R`))
  + marten.csv: data harvested from [GBIF](https://www.gbif.org/) and [iNaturalist](https://www.inaturalist.org) for _Martes Caurina_. .
  
### Outputs
+ output
  + occurencemap.jpeg
  + currentsdm.jpeg
  + futuresdm.jpeg
  + maxent_outputs (contents are not under version control)

### Scripts
+ scripts (directory containing R scripts for gathering occurrence data, running forecast models, and creating map outputs)
  + `dataaquisitioncleaning.R` for obtaining the GBIF data
  + `occurencemap.R` to create the occurance map of the GBIF data
  + `currentSDM.R` to run a maxent model and generate a current sdm
  + `futureSDM.R` to generate a future sdm, in 70 years under IP model 
 

## Running the code
- Run the scripts in the following order
1. `dataaquisitioncleaning.R`
2. `occurencemap.R`
3. `currentSDM.R`
4. `futureSDM.R`
