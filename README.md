# Soil Health and Corn Yield Stability Under Drought Conditions

## Project Overview
This project analyzes the relationship between soil health scores and corn yield stability across different drought severity levels in major corn-producing counties of the United States. The analysis uses county-level data from 2000-2016 to understand how soil health influences agricultural productivity during climate stress events.

## Research Question
How does soil health score influence corn yield stability across different drought severity levels in major corn-producing counties of the United States?

## Data Sources

### Primary Dataset
- **Source**: Zenodo Repository
- **DOI**: https://doi.org/10.5281/zenodo.11069166
- **Citation**: Mahmood, S., Nunes, M. R., Kane, D. A., & Lin, Y. (2023). Soil health explains the yield-stabilizing effects of soil organic matter under drought [Data set]. Zenodo.
- **License**: Creative Commons Attribution 4.0 International (CC BY 4.0)
- **Original Paper**: https://doi.org/10.1016/j.seh.2023.100048

### Additional Data
- **Climate Enhancement**: Derived climate variables calculated from existing climate data (map, mat, summer_spei)
- **Source**: Enhanced using WorldClim methodology principles applied to existing data

## File Descriptions

### Primary Data Files
- `all_data.csv`: Complete primary dataset with soil, yield, and climate variables
- `all_data_metadata.csv`: Metadata describing columns, units, and notes for primary dataset
- `yield_deficit.csv`: Processed yield deficit data under different drought conditions
- `yield_deficit_metadata.csv`: Metadata for yield deficit dataset
- `info.txt`: Citation and licensing information

### Enhanced Data Files
- `enhanced_climate_dataset.csv`: Primary dataset enhanced with additional climate variables

## Variable Dictionary

### Geographic Identifiers
- `GEOID`: County Geographic Identifier (integer)
- `state_alpha`: State abbreviation (text)
- `state_ansi`: State ANSI code (integer)
- `county_ansi`: County ANSI code (integer)
- `county_name`: County name (text)

### Temporal Variables
- `year`: Year of observation (2000-2016)

### Yield Variables
- `Yield_Mg_ha`: Corn yield in megagrams per hectare (Mg/ha)
- `Yield_VS`: Yield under very severe drought (Mg/ha)
- `Yield_S`: Yield under severe drought (Mg/ha)
- `Yield_M`: Yield under moderate drought (Mg/ha)
- `Yield_N`: Yield under normal conditions (Mg/ha)
- `Deficit_VS`: Yield deficit under very severe drought (Mg/ha)
- `Deficit_S`: Yield deficit under severe drought (Mg/ha)
- `Deficit_M`: Yield deficit under moderate drought (Mg/ha)

### Soil Variables
- `ssurgo_soc_mean`: Mean soil organic carbon (%)
- `ssurgo_clay_mean`: Mean clay content (%)
- `ssurgo_sand_mean`: Mean sand content (%)
- `ssurgo_silt_mean`: Mean silt content (%)
- `ssurgo_om_mean`: Mean soil organic matter (%)
- `ssurgo_awc_mean`: Mean available water capacity (%)
- `ssurgo_aws_mean`: Mean available water storage (%)
- `ssurgo_cec_mean`: Mean cation exchange capacity (cmol/kg)
- `ssurgo_ph_mean`: Mean soil pH
- `Score_Mean`: Soil health score (0-1 scale)

### Climate Variables
- `summer_spei`: Summer Standardized Precipitation Evapotranspiration Index
- `spei.cat`: SPEI category (very severe, severe, moderate, normal)
- `map`: Mean annual precipitation (mm)
- `mat`: Mean annual temperature (°C)

### Soil Classification
- `ORDER`: Soil order classification
- `Suborder`: Soil suborder classification
- `Texture`: Soil texture classification
- `OC`: Organic carbon content (%)

### Enhanced Climate Variables (Added in Step 4)
- `aridity_index`: Temperature to precipitation ratio (°C/mm)
- `climate_zone`: Climate classification (Cold_Dry, Cold_Wet, Temperate_Dry, Temperate_Wet, Warm_Dry, Warm_Wet)
- `growing_degree_days`: Accumulated temperature above 10°C base (degree-days)
- `heat_stress_index`: Temperature-based stress indicator (°C above 25°C)
- `drought_stress_index`: Combined drought stress measure (0+ scale)
- `climate_variability`: Climate stability measure based on SPEI deviation (absolute value)

## Data Quality Notes

### Missing Values
- Primary dataset: Complete records for all 12,376 observations
- Enhanced climate variables: No missing values introduced

### Outliers Identified
- `aridity_index`: 330 potential outliers (>3 standard deviations)
- `growing_degree_days`: 363 potential outliers (>3 standard deviations)
- Outliers retained as they represent legitimate climate extremes

### Data Processing Steps
1. Original data obtained from Zenodo repository
2. Climate enhancement performed using derived variables
3. Climate zones classified based on temperature and precipitation thresholds
4. Stress indicators calculated using established agricultural metrics
5. Quality control performed to validate ranges and identify outliers

## Usage Rights and Attribution

### License Terms
This dataset is available under Creative Commons Attribution 4.0 International (CC BY 4.0) license, which allows:
- Use for any purpose including commercial applications
- Sharing and redistribution in any medium
- Modification and adaptation for research needs
- Combination with other datasets

### Required Attribution
When using this data, you must:
- Cite the original authors: Mahmood, S., Nunes, M. R., Kane, D. A., & Lin, Y.
- Reference the original publication and dataset DOI
- Indicate any changes made to the original data
- Include this attribution in any publications or presentations

### Recommended Citation
```
Mahmood, S., Nunes, M. R., Kane, D. A., & Lin, Y. (2023). Soil health explains 
the yield-stabilizing effects of soil organic matter under drought [Data set]. 
Zenodo. https://doi.org/10.5281/zenodo.11069166
```

## Technical Specifications

### File Formats
- Primary data: CSV (Comma Separated Values)
- Metadata: CSV format with column descriptions
- Documentation: Plain text and Markdown formats

### Data Structure
- Tabular data with rows representing county-year observations
- 12,376 total observations across 31 variables (enhanced dataset)
- Time series data spanning 2000-2016
- Geographic coverage: Major corn-producing counties in the United States

### Software Requirements
- Python 3.x with pandas, numpy for data processing
- Matplotlib, seaborn for visualization
- Standard statistical packages for analysis

## Contact Information
For questions about this dataset or analysis approach, refer to the original publication:
- Journal: Soil & Environmental Health
- DOI: https://doi.org/10.1016/j.seh.2023.100048

## Version History
- v1.0: Original dataset from Zenodo
- v1.1: Enhanced with additional climate variables (Step 4 of THA1)

## Acknowledgments
This work builds upon the original research by Mahmood et al. (2023) and utilizes publicly available datasets from USDA, NOAA, and other government agencies. Climate enhancement methodology follows principles established in agricultural climatology and soil science literature.
