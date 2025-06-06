# variables/

This directory contains all geospatial raster predictors used to train and project the Random Forest model for illegal primate hunting risk.  
Due to GitHub's file size restrictions, the `.tif` files have been uploaded externally and can be accessed via the link below.

**Download full folder:**  
[Google Drive – Raster Predictors](https://drive.google.com/drive/folders/13ENit3NzjQ8nZb11pIet4NIscoZD0vE1?usp=share_link)

---

## Contents and Description

### 1. `LU_change/`
**File:** `tree_PFT_sum_2020.tif`  
- Tree canopy coverage derived from GCAM/SSP4 downscaled land-use data.  
- Represents the total percentage of vegetative tree cover per 1-km grid cell in 2020.  
- Used as a proxy for habitat density and accessibility.

---

### 2. `climate_extremes/`
**Files:**
- `Media_Decennale_txnETCCDI_2015_2024.tif`  
  – Decadal average of extreme minimum temperature (txn).  
- `Media_Decennale_cddETCCDI_2015_2024.tif`  
  – Decadal average of consecutive dry days (cdd).

> Both datasets were derived from the ETCCDI climate indices and resampled to match model resolution.  
> They capture local climatic stress that may influence primate habitat and human activity.

---

### 3. `travel_time/`
**File:** `Accessibility2015.tif`  
- Estimated travel time to the nearest urban center with >50,000 inhabitants.  
- Originally developed by Weiss et al. (2018).  
- Used as a proxy for market access and anthropogenic pressure.

---

## Usage Notes

- All rasters were resampled and reprojected to a common 1-km resolution and CRS prior to stacking.
- File naming conventions align with variable names used in the model training script (`random_forest.Rmd`).
- These layers are stacked and passed to the RF model using the same order of predictors.

---





