# Mapping the Threat: Spatial Analysis of Illegal Hunting Pressure on Primates

This repository contains the complete workflow used to model and predict the risk of illegal primate hunting across tropical regions.  
The analysis combines environmental, climatic, and anthropogenic predictors using supervised classification methods to identify potential hotspots of hunting pressure.

## Overview

- Objective: Predict spatial patterns of illegal primate hunting.
- Methods: Random Forest (RF) and Generalized Linear Model (GLM).
- Geographic scope: Tropical regions within the global primate distribution range.
- Input data: Presence records of illegal mammal hunting, pseudo-absences, and globally harmonized raster layers.

## Repository Structure
'''
├── data/
│ ├── dataset_modelo_all.csv # Model training data
│ └── redlist_species_data/ # IUCN primate ranges (.shp hosted externally)
│
├── variables/
│ ├── LU_change/ # Tree cover raster (GCAM)
│ ├── climate_extremes/ # ETCCDI-based climate variables
│ └── travel_time/ # Accessibility to urban centers
│
├── rf_model/
│ ├── random_forest.Rmd # Full model workflow
│ ├── modelo_rf_final.rds # Trained Random Forest model
│ └── riesgo_caza_rf_filtrado.tif # Final prediction raster
'''


## How to Reproduce

1. Download required input data:
   - `dataset_modelo_all.csv` from `/data/`
   - Raster predictors from the following Google Drive folder:  
     [Raster Variables](https://drive.google.com/drive/folders/13ENit3NzjQ8nZb11pIet4NIscoZD0vE1?usp=share_link)
   - IUCN primate distribution shapefile from:
     - https://drive.google.com/drive/folders/12v32ctX-P9l-fV5P1VM1j9vdchSndkYD?usp=sharing

2. Run `random_forest.Rmd` to:
   - Train or load the RF model
   - Predict spatial risk using the raster stack
   - Apply masking with the primate range shapefile
   - Generate and export visual outputs

3. Output files include:
   - `riesgo_caza_rf_filtrado.tif`: filtered prediction raster
   - Evaluation figures: ROC curve, variable importance, predictor distributions


