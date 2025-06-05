# Variables Directory

This directory is intended to store the geospatial datasets used in this project. These datasets are essential for the analysis but have not been uploaded directly to this GitHub repository due to their large file size (each file is several hundred MB or more). GitHub has a file size limit, and large binary files are generally not suitable for version control here.

To ensure the project remains accessible and reproducible, all required `.tif` files have been uploaded to a public Google Drive folder. You can download them using the links provided below.

Please download the files manually and place them in the appropriate subdirectories within `variables/` as described here.

## How to Use

1. Create the following folder structure inside the `variables/` directory:
   variables/
   ├── LU_change/
   ├── climate_extremes/
   └── travel_time/

2. Download each `.tif` file from the Google Drive links provided below.

3. Place each file in its respective subfolder.

## LU_change

Contains land use and vegetation type data.

File:
- tree_PFT_sum_2020.tif  
Description: Represents the summed tree Plant Functional Types (PFT) for the year 2020.

Link: https://drive.google.com/your-link-here

## climate_extremes

Contains climate extreme indicators derived from ETCCDI datasets.

Files:
- cMedia_Decennale_cddETCCDI_2015_2024.tif: Decadal average of consecutive dry days.
- Media_Decennale_txnETCCDI_2015_2024.tif: Decadal average of minimum daily maximum temperature.

Link: https://drive.google.com/your-link-here

## travel_time

Contains data on geographic accessibility.

File:
- Accessibility2015.tif  
Description: Represents estimated travel time to the nearest city (in minutes) for the year 2015.

Link: https://drive.google.com/your-link-here

## Note

Make sure that the Google Drive links are publicly accessible. If you experience any problems accessing the data, ensure that:
- The links are set to “Anyone with the link can view.”
- You are logged into a Google account (if required).

If the issue persists, contact the repository maintainer for help.

This structure helps keep the repository lightweight while maintaining reproducibility and clarity for anyone using or reviewing this project.
