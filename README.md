# Analysis of Rural-Urban Difference in Drinking Water System Violations in Georgia 

## Project overview

This project analyzes whether rural public water systems in Georgia are more likely to experience drinking water quality violations compared to urban systems. The analysis uses publicly available data from the EPA Safe Drinking Water Act (SDWA) database and Rural–Urban Commuting Area (RUCA) classifications.
The primary outcome is whether a water system experienced at least one drinking water violation. The main predictor of interest is whether the water system serves a rural or urban area.

## Reproducibility  
To reproduce the analysis:

## Required Data 
Ensure the raw data files are placed in data/raw-data/:

`GA_PUB_WATER_SYSTEMS.csv`
`SDWA_PN_VIOLATION_ASSOC.csv`
`RUCA-codes-2020-zipcode.csv`

The original SDWA dataset is a national scope and contains information on public water systems across the United States. For this poject, the data were restricted to public water systems located in Georgia, and this subset is stored as the raw data named `GA_PUB_WATER_SYSTEMS.csv` used for analysis.

The RUCA ZIP code classification dataset is also used to classify water systems as rural or urban. 

## Steps to Reproduce the analysis
1. Clone or download this repository
2. Open the R project in RStudio.
3. Run code/analysis-code/analysis.qmd to perform exploratory data analysis and examine the structure of the raw datasets.
4. Run code/eda-code/eda.qmd to perform exploratory data analysis and examine the structure of the raw datasets.
5. Render manuscript/manuscript.qmd to generate the manuscript containing the main results, figures, and interpretations.


All required output files (processed data and figures) will be generated automatically.
