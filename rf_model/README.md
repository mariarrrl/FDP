# rf_model/

This folder contains all materials related to the training, evaluation, and spatial prediction of illegal primate hunting risk using the Random Forest (RF) classifier.

## Contents

- **modelo_rf_final.rds**  
  Final trained Random Forest model object. Generated using 10-fold cross-validation on the full cleaned dataset. Can be loaded directly into R for prediction or analysis.

- **random_forest.Rmd**  
  R Markdown script for full model pipeline, including:
  - Data preprocessing and variable selection
  - Model training and cross-validation
  - Variable importance analysis
  - ROC curve generation and AUC evaluation
  - Spatial prediction using raster layers
  - Risk map generation (cropped and masked to primate distribution)
  - Comparison with GLM performance
  - Boxplot visualizations of predictor distributions

- **riesgo_caza_rf_filtrado.tif**  
  Final output raster map of predicted illegal primate hunting risk, filtered using the IUCN primate distribution shapefile. Expressed as probability (0–1) of hunting presence.

## Requirements

The workflow relies on the following R packages:
- `randomForest`, `caret`, `pROC`
- `raster`, `sf`, `viridis`, `rnaturalearth`, `ggplot2`, `patchwork`, `dplyr`

## How to Reproduce

1. **Download and prepare input data:**
   - Load the main dataset `dataset_modelo_all.csv` from the `/data/` directory.
   - Download the predictive raster variables from the following google drive link directory: [`/variables/` ](https://drive.google.com/drive/folders/13ENit3NzjQ8nZb11pIet4NIscoZD0vE1?usp=share_link).
   - Download and load the IUCN primate distribution shapefile as explained in the `/data/` directory (hosted externally due to file size).

2. **Run the `random_forest.Rmd` script:**
   - Preprocess and clean the input data.
   - Train the Random Forest model using 10-fold cross-validation or load the existing model (`modelo_rf_final.rds`).
   - Predict spatial hunting risk using the stacked raster variables.
   - Apply the IUCN shapefile to crop and mask the risk output.
   - Export the final risk prediction raster (`riesgo_caza_rf_filtrado.tif`).

3. **Optional:**
   - Compare RF performance with the GLM model (AUC, ROC curves).
   - Generate visualizations of variable distributions and model importance.


## Notes

- The prediction raster (`riesgo_caza_rf_filtrado.tif`) can be visualized in QGIS, ArcGIS, or R using `raster::plot()`.

