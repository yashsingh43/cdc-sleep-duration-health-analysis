# Raw Data (Not Included)

This folder is a placeholder for the large raw BRFSS data file used in this project.

The CDC Behavioral Risk Factor Surveillance System (BRFSS) 2022 dataset used in this project is too large to upload to GitHub (~900 MB) and is not publicly redistributed here.

To retrieve the dataset:
1. Download the BRFSS 2022 dataset (`LLCP2022ASC.zip`) from the [CDC website](https://www.cdc.gov/brfss/annual_data/2022/files/LLCP2022ASC.zip).
2. Extract the `.ASC` file and convert it to a text file named `LLCP2022.txt`.
3. Place that file in this folder before running the data cleaning notebook (`02_data_cleaning.ipynb`).

The CDC BRFSS Codebook (HTML) and CDC Chronic Disease Indicators (JSON API) are accessed within the notebooks and are not stored in this folder.