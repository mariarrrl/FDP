# data

This folder contains all datasets used in model training, evaluation, and supporting spatial analysis for predicting illegal primate hunting risk.

## dataset_modelo_all.csv

This is the main dataset used to train the Random Forest (RF) and Generalized Linear Model (GLM) classifiers.  
It includes both presence points of illegal hunting events and pseudo-absence records (generated using full or cluster-based strategies).

Contents:
- Predictor variables: environmental, anthropogenic, and socioeconomic features harmonized at 1-km resolution.
- Binary response variable: indicating presence (1) or pseudo-absence (0) of hunting activity.
- Includes pre-processed and cleaned data used directly in the modeling scripts.

Used in:
- Training the final RF model (see `rf_model/` folder).
- GLM model development (see `GLM_Code_Supplementary` folder in supplementary materials).

## redlist_species_data_.../

This folder contains species distribution data derived from the IUCN Red List.
- The data was used to spatially constrain predictions to regions where primates are naturally present.
 
Due to GitHub file size limitations, the full shapefile containing IUCN primate species distribution ranges is hosted externally.  
You can download it directly from the following Google Drive link:

[.shp](https://drive.google.com/drive/folders/12v32ctX-P9l-fV5P1VM1j9vdchSndkYD?usp=sharing)

It was originally sourced from the IUCN Red List Spatial Data portal.




