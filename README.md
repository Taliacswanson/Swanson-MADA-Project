# Analysis of Rural-Urban Differences in Drinking Water System Violations in Georgia 

## Project Overview

This project examines whether rural public water systems in Georgia are more likely to experience drinking water quality violations compared to urban systems. The analysis uses publicly available data from the EPA Safe Drinking Water Information System (SDWIS) and Rural–Urban Commuting Area (RUCA) classifications.

The primary outcome is whether a water system has experienced at least one drinking water violation. The primary predictor 
is rural versus urban classification of the system's service area. Multivariable logistic regression was used to evaluate this association while adjusting for system-level characteristics. 

## Repository structure
`data/raw-data/` --> Original datasets 
`data/processed-data/` --> Cleaned dataset used for analysis 
`code/analysis-code/` --> Main analysis scripts 
`code/eda-code/` --> Exploratory data analysis scripts 
`manuscript/` --> Final Quarto manuscripts 
`output/` --> figures and tables 

## Required Data 
Ensure the raw data files are placed in data/raw-data/:

`GA_PUB_WATER_SYSTEMS.csv`
`SDWA_PN_VIOLATION_ASSOC.csv`
`RUCA-codes-2020-zipcode.csv`

The original SDWA dataset is a national scope and contains information on public water systems across the United States. For this project, the data were restricted to public water systems located in Georgia, and this subset is stored as the raw data named `GA_PUB_WATER_SYSTEMS.csv` used for analysis.

The RUCA is used to classify water systems as rural or urban based on ZIP code. 

## Required Packages
Install the following R packages before running the analysis 

install.packages(c("tidyverse", "ggplot2", "dplyr", "readr", "broom", "knitr", "pROC", "here"))

## Steps to Reproduce the analysis
1. Clone or download this repository
2. Open the .Rproj file in RStudio.
3. Ensure all raw data are located in "data/raw-data/"
4. Run the exploratory analysis:
code/eda-code/edqa.qmd 
5. Run the manin analysis:
code/analysis-code/analysis.qmd 
6. Render manuscript:
quarto render manuscript/manuscript.qmd 


All required output files (processed data and figures) will be generated automatically.

## Key Variables 
`any_violation` --> Binary indicator of ≥1 violation
`rural` --> Rural (1) vs Urban (0) classification 
`log_population` --> log-transformed population served 
`PWS_TYPE_CODE` --> Water system type 

## Notes
* File paths are managed using here() package 
* Systems with missing RUCA classifications were excluded from the final analysis 

### Author 
Talia C. Swanson, B.S.