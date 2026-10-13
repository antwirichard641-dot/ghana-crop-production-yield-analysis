# Exploring Crop Production and Yield Trends in Ghana (1961–2024)

## Project Overview

How has Ghana's crop production changed over the past six decades? This project explores historical trends in production, harvested area, and yield for four major crops: maize, rice, cassava, and yams.

Using data from the Food and Agriculture Organization of the United Nations (FAO) FAOSTAT database, this analysis examines changes between 1961 and 2024. It demonstrates foundational skills in agricultural data management, exploratory data analysis, statistical reasoning, and scientific communication using Python.

## Research Question

**How have production, harvested area, and yield for selected major crops in Ghana changed from 1961 to 2024?**

## Objectives

- Analyze long-term trends in crop production.
- Examine changes in harvested area.
- Investigate changes in crop yield as an indicator of land productivity.
- Compare trends across four major crops.
- Quantify linear trends and assess their statistical significance.
- Interpret findings while distinguishing association from causation.

## Crops and Indicators

**Crops**
- Maize
- Rice
- Cassava
- Yams

**Indicators**
- Production, measured in tonnes (t)
- Area harvested, measured in hectares (ha)
- Yield, measured in kilograms per hectare (kg/ha)

## Visual Results

### 1. Crop Production Trends

<img width="989" height="490" alt="image" src="https://github.com/user-attachments/assets/8bf56430-8f12-4501-a19b-07a04a5d1406" />

This figure compares annual production across the four selected crops. Production reflects both the area harvested and the amount produced per unit of harvested area.

### 2. Harvested Area Trends

<img width="989" height="490" alt="image" src="https://github.com/user-attachments/assets/71391ecb-88dc-41d1-bdc4-f67ffaa424fd" />


This figure examines changes in the area harvested for each crop. Changes in harvested area can contribute to changes in total production, independently of changes in yield.

### 3. Crop Yield Trends


<img width="989" height="490" alt="image" src="https://github.com/user-attachments/assets/6fecbb6d-779c-4d6d-ade1-6aee5b8592f9" />


This figure compares crop yield over time, providing a measure of output per hectare. Yield is distinct from total production and should be interpreted separately.

## Data Source

**Source:** FAO FAOSTAT, Crops and livestock products domain.

- **Country:** Ghana
- **Period:** 1961–2024
- **Crops:** Four
- **Indicators:** Three
- **Observations:** 768

The cleaned dataset contains 768 records, representing four crops, three indicators, and 64 years.

The cleaned data are available at [`data/ghana_crop_data_clean.csv`](data/ghana_crop_data_clean.csv).

## Methods

The analysis was conducted in Python using Google Colab.

1. **Data selection:** Selected the four crops and three indicators from the FAOSTAT dataset.
2. **Data quality checks:** Examined dataset dimensions, year coverage, missing values, duplicates, units, and data flags.
3. **Descriptive statistics:** Summarized the distribution and variability of each crop indicator.
4. **Trend visualization:** Plotted annual production, harvested area, and yield.
5. **Long-term change:** Compared values in 1961 and 2024.
6. **Linear trend analysis:** Used linear regression to estimate the direction and magnitude of trends over time and evaluate statistical significance.

## Key Findings

- All 12 crop-indicator combinations had positive estimated linear trend slopes.
- Production, harvested area, and yield generally increased over the study period for the selected crops.
- The magnitude of change varied by crop and indicator.
- Production and yield describe different agricultural outcomes: increased production may reflect changes in harvested area, yield, or both.
- Statistically significant trends do not, by themselves, establish why the changes occurred.

Detailed outputs are available in the [`results/`](results/) folder.

## Repository Structure

```text
ghana-crop-production-yield-analysis/
├── data/
│   └── ghana_crop_data_clean.csv
├── figures/
│   ├── figure_1_production_trends.png
│   ├── figure_2_harvested_area_trends.png
│   └── figure_3_yield_trends.png
├── notebooks/
│   └── Ghana_Crop_Production_Yield_Analysis.ipynb
├── results/
│   ├── summary_statistics.csv
│   ├── long_term_change.csv
│   └── linear_trend_results.csv
├── README.md
├── requirements.txt
└── LICENSE
```

## Tools and Technologies

- Python
- pandas
- NumPy
- Matplotlib
- SciPy
- Google Colab
- GitHub

## Limitations

- This is a descriptive observational analysis; it does not establish causal relationships.
- Linear regression summarizes long-term trends but does not fully account for time-series characteristics such as autocorrelation.
- FAOSTAT records may include estimated, imputed, or externally supplied values. Data flags should be considered when interpreting results.
- National-level trends do not explain variation among individual farms or growing regions within Ghana.
- Production, harvested area, and yield should be interpreted as distinct indicators.

## Reproducibility

The repository includes the analysis notebook, cleaned dataset, and derived result tables.

To reproduce the analysis:

1. Download or clone this repository.
2. Open `notebooks/Ghana_Crop_Production_Yield_Analysis.ipynb` in Google Colab or Jupyter.
3. Obtain the corresponding original FAOSTAT source dataset.
4. Follow the notebook's data-loading instructions.
5. Install the dependencies listed in `requirements.txt` if they are not already installed.

## Future Improvements

Potential extensions include:

- Comparing crop trends with rainfall and temperature data.
- Investigating year-to-year yield variability.
- Examining regional differences where suitable data are available.
- Exploring additional agricultural productivity indicators.

## Author

**Richard Antwi**

Agricultural Science | Animal Science | Agricultural Data Analysis

This project is part of an agricultural data science portfolio demonstrating quantitative reasoning, reproducible research, and the application of data analysis to agricultural questions.
