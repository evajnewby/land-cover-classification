# Land Cover Classification of Southern Santa Barbara County, California

Author: Eva Newby (https://github.com/evajnewby)

## About
The following repository was created for edicational purposes for EDS 220 - Environmental Data, for the Masters of Environmental Data Science program at the Bren School of Environmental Science and Management at the University of California, Santa Barbara. 

The purpose of this repository is to hold both data and code necessary for the completion of the one decision tree and one map detailing the landcover (green vegetation, soil/dead grass, urban, or water) for southern Santa Barbara county.

This repository contains one data folder, one R project, one Quarto document, one rendered html and associated files. 

The `land-cover-classification.qmd` contains all the code necessay to read in the data, create a decision tree, train the decision tree, and create a plot with classified land cover types. The `land-cover-classification.html` is the rendered version. 

The data folder contains the landsat data .tif files, the shapefiles (and associated files) for southern Santa Barbara county, and training data. This folder was added to the gitignore to prevent any pushing issues or delays.

## Highlights
- Load and process Landsat scene
- Crop and mask Landsat data to study area
- Extract spectral data at training sites
- Train and apply decision tree classifier
- Plot results using `tmap()`.

## Data
The `landsat-data` is from the Landsat 5 Thematic mapper, and contains 1 scene from September 25, 2007, with bands 1, 2, 3, 4, 5, 6, and 7. 

Additionally, the data folder also contains a shapefile representing southern Santa Barbara county, and training data containing polygons representing sites. 

## Repository Structure
```bash
land-cover-classification
├── README.md
├── .gitignore
      ├── data
          ├── SB_county_south.cpg
          ├── SB_county_south.dbf
          ├── SB_county_south.prj
          ├── SB_county_south.sbn
          ├── SB_county_south.shp
          ├── SB_county_south.shx
          ├── SB_validation_points.dbf
          ├── SB_validation_points.prj
          ├── SB_validation_points.qpj
          ├── SB_validation_points.shp
          ├── SB_validation_points.shx
          ├── trainingdata.dbf
          ├── trainingdata.cpg
          ├── trainingdata.prj
          ├── trainingdata.qpj
          ├── trainingdata.shp
          ├── landsat-data.shx
                ├── LT05_L2SP_042036_20070925_20200829_02_T1_SR_B1.tif
                ├── LT05_L2SP_042036_20070925_20200829_02_T1_SR_B2.tif
                ├── LT05_L2SP_042036_20070925_20200829_02_T1_SR_B3.tif
                ├── LT05_L2SP_042036_20070925_20200829_02_T1_SR_B4.tif
                ├── LT05_L2SP_042036_20070925_20200829_02_T1_SR_B5.tif
                ├── LT05_L2SP_042036_20070925_20200829_02_T1_SR_B7.tif
├── land-cover-classification.Rproj
├── land-cover-classification_files
├── land-cover-classification.html
└──  land-cover-classification.qmd
```

## References
U.S. Geological Survey, September 25, 2007. Landsat 5. U.S. Department of the Interior. Retrieved December 6, 2024, from https://www.usgs.gov/landsat-missions/landsat-5
