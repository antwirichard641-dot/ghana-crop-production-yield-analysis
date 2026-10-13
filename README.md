# Exploring Crop Production and Yield Trends in Ghana (1961–2024)

## Project Overview

This project explores historical trends in crop production, harvested area, and yield for four major crops in Ghana: maize, rice, cassava, and yams. Using data from the Food and Agriculture Organization of the United Nations (FAO) FAOSTAT database, the analysis examines how these agricultural indicators changed between 1961 and 2024.

The project demonstrates foundational skills in agricultural data analysis, data cleaning, descriptive statistics, visualization, and linear trend analysis using Python.

## Research Question

**How have production, harvested area, and yield for selected major crops in Ghana changed from 1961 to 2024?**

## Objectives

- Examine historical trends in crop production.
- Analyze changes in harvested area.
- Investigate changes in crop yield as an indicator of land productivity.
- Compare trends across the four selected crops.
- Quantify long-term linear trends and interpret their statistical significance.

## Crops Included

- Maize
- Rice
- Cassava
- Yams

## Data Source

**Source:** FAO FAOSTAT, Crops and livestock products domain.

**Geographic coverage:** Ghana  
**Time coverage:** 1961–2024  
**Indicators:** Production, area harvested, and yield

The cleaned project dataset contains 768 observations covering four crops, three indicators, and 64 years.

Original measurements use the following units:

- Production: tonnes (t)
- Area harvested: hectares (ha)
- Yield: kilograms per hectare (kg/ha)

The cleaned dataset is available in [`data/ghana_crop_data_clean.csv`](data/ghana_crop_data_clean.csv).

## Methods

The analysis was conducted in Python using Google Colab.

1. **Data selection and cleaning:** Selected the four crops and three agricultural indicators from the FAOSTAT dataset.
2. **Data validation:** Examined dataset dimensions, year coverage, missing values, duplicate records, units, and data flags.
3. **Descriptive statistics:** Calculated summary statistics for the selected crop indicators.
4. **Trend visualization:** Plotted annual production, harvested area, and yield.
5. **Long-term change:** Compared the first and last available years.
6. **Linear trend analysis:** Used linear regression to estimate the direction and magnitude of trends over time.

## Key Findings

- All 12 crop-indicator combinations had positive estimated linear trend slopes.
- Production, harvested area, and yield generally showed long-term increases across the selected crops.
- The magnitude of change differed among crops and indicators.
- Production and yield represent different agricultural outcomes: increased production may reflect changes in harvested area, yield, or both.
- Statistical significance in a linear trend model does not establish the cause of the observed changes.

Detailed outputs are available in the [`results/`](results/) folder.

## Repository Structure

```text
ghana-crop-production-yield-analysis/
├── data/
│   └── ghana_crop_data_clean.csv
├── notebooks/
│   └── Ghana_Crop_Production_Yield_Analysis.ipynb
├── results/
│   ├── summary_statistics.csv
│   ├── long_term_change.csv
│   └── linear_trend_results.csv
├── figures/
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

- The analysis is descriptive and observational; it does not establish causal relationships.
- Linear regression summarizes long-term trends but does not fully account for all time-series characteristics, such as autocorrelation.
- Some FAOSTAT observations are estimated, imputed, or supplied by external organizations. Data flags should therefore be considered when interpreting the results.
- National-level trends do not explain differences among individual farms or growing regions within Ghana.

## Reproducibility

The analysis notebook and derived result tables are included in this repository.

To reproduce the analysis:

1. Download or clone this repository.
2. Open `notebooks/Ghana_Crop_Production_Yield_Analysis.ipynb` in Google Colab or Jupyter.
3. Install the dependencies listed in `requirements.txt`.
4. Obtain the corresponding original FAOSTAT source dataset and follow the notebook's data-loading instructions.

## Future Improvements

Possible extensions include:

- Comparing agricultural trends with rainfall and temperature records.
- Investigating year-to-year variability in crop yields.
- Examining regional differences where suitable data are available.
- Exploring agricultural productivity using additional indicators.

## Author

**Richard Antwi**

Agricultural Science | Animal Science | Agricultural Data Analysis

This project is part of an agricultural data science portfolio developed to demonstrate quantitative reasoning, reproducible research, and the application of data analysis to agricultural questions.
