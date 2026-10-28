# Exploring Long-Term Crop Production, Harvested Area, and Yield Trends in Ghana (1961–2024)

## Project Overview

Agricultural production plays an important role in food availability, rural livelihoods, and agricultural development. Understanding how crop production and productivity change over time can help identify long-term patterns, highlight differences among crops, and establish a foundation for further agricultural research.

This project examines six decades of agricultural trends in Ghana, focusing on four major food crops: **maize, rice, cassava, and yams**. Using historical data from the Food and Agriculture Organization of the United Nations (FAO) FAOSTAT database, the analysis investigates changes in annual crop production, harvested area, and yield between 1961 and 2024.

The project combines agricultural data management, exploratory data analysis, descriptive statistics, time-series visualization, and linear trend analysis to investigate how these indicators have evolved over the study period.

Rather than treating agricultural production as a single measure of performance, the analysis distinguishes between total output, land area harvested, and output per unit of harvested area. This distinction is important because changes in total production can reflect changes in cultivated area, yield, or both.

The project represents an exploratory application of quantitative methods to an agricultural research question and contributes to my developing interests in crop productivity, agricultural systems, and evidence-based approaches to understanding agricultural development in Ghana.

## Research Question

**How have crop production, harvested area, and yield for maize, rice, cassava, and yams in Ghana changed between 1961 and 2024, and what differences emerge across these agricultural indicators?**

### Research Objectives

The analysis was designed to:

1. Examine long-term changes in the production of maize, rice, cassava, and yams in Ghana.
2. Investigate changes in the harvested area associated with each crop.
3. Assess historical yield trends as an indicator of output per unit of harvested area.
4. Compare the direction and magnitude of trends across crops and agricultural indicators.
5. Quantify linear trends and evaluate their statistical significance.
6. Interpret production, area, and yield patterns while distinguishing descriptive associations from causal explanations.
7. Establish a reproducible analytical workflow that can support further research into agricultural productivity.

## Agricultural Significance

Crop production, harvested area, and yield describe related but distinct aspects of agricultural production.

- **Crop production** measures the total quantity harvested and provides an indication of the scale of crop output.
- **Harvested area** measures the land area from which a crop was harvested and helps contextualize changes in total production.
- **Crop yield** measures output per unit of harvested area and provides an indicator of land productivity.

Examining these indicators together offers a more informative perspective than considering production alone. For example, an increase in total output may coincide with an expansion in harvested area, an increase in yield, or changes in both.

However, these indicators alone cannot establish the causes of observed changes. Factors such as rainfall, temperature, soil conditions, input use, technology, agricultural policies, and management practices were not directly evaluated in this project.

The analysis therefore focuses on documenting historical patterns and identifying questions that warrant further investigation.

## Study Scope

| Study component | Description |
|---|---|
| Country | Ghana |
| Study period | 1961–2024 |
| Temporal coverage | 64 years |
| Crops | Maize, rice, cassava, and yams |
| Agricultural indicators | Production, harvested area, and yield |
| Cleaned dataset | 768 records |
| Data source | FAO FAOSTAT |
| Analytical environment | Python and Google Colab |
| Research approach | Descriptive and exploratory quantitative analysis |

### Crops Investigated

**Maize (corn)**

Maize production trends provide a basis for examining changes in the output and harvested area of an important cereal crop in Ghana.

**Rice**

Rice is examined as a second cereal crop, allowing its historical production, land-use, and yield patterns to be compared with those of maize.

**Cassava**

Cassava is included as a major root crop. Its production and yield trends provide a different perspective on the evolution of Ghana's crop production systems.

**Yams**

Yams are examined as another important root and tuber crop, allowing comparisons between its historical trajectory and those of maize, rice, and cassava.

The project compares these crops using the same three indicators while recognizing that differences in crop biology, production systems, and measurement units affect the interpretation of results.

## Data Source and Preparation

The analysis uses agricultural statistics from the FAO's FAOSTAT database, specifically the Crops and livestock products domain.

**Data source:** [FAOSTAT — Crops and livestock products](https://www.fao.org/faostat/en/#data/QCL)

The dataset was filtered to retain observations relevant to Ghana, the four selected crops, the three agricultural indicators, and the 1961–2024 study period.

### Variables and Measurement Units

| Indicator | Unit | Interpretation |
|---|---|---|
| Production | Tonnes (t) | Total crop output |
| Area harvested | Hectares (ha) | Area harvested for the crop |
| Yield | Kilograms per hectare (kg/ha) | Crop output per unit of harvested area |

The cleaned dataset contains 768 records, corresponding to the expected combinations of four crops, three indicators, and 64 years:

4 crops × 3 indicators × 64 years = 768 records.

This structure provides a consistent basis for comparing historical patterns across the selected crops and indicators.

### Data Quality and Preparation

The data preparation process included checks and selection procedures covering:

- Dataset dimensions and variable structure.
- Country, crop, indicator, and year selection.
- Temporal coverage across the study period.
- Missing values and duplicate records.
- Measurement units and consistency.
- Available FAOSTAT data flags and associated metadata.

These checks support more transparent interpretation of the results. Nevertheless, the presence of a complete expected record structure should not be treated as proof that every observation is free of uncertainty or measurement limitations.

The cleaned dataset is available at [`data/ghana_crop_data_clean.csv`](data/ghana_crop_data_clean.csv).

## Visual Analysis and Results

The following figures present the three principal dimensions of the analysis: production, harvested area, and yield.

### 1. Long-Term Crop Production Trends

![Line chart showing annual production trends for maize, rice, cassava, and yams in Ghana from 1961 to 2024, measured in tonnes.](https://github.com/user-attachments/assets/8bf56430-8f12-4501-a19b-07a04a5d1406)

*Figure 1. Historical production trends for maize, rice, cassava, and yams in Ghana, 1961–2024. Source: FAOSTAT data analyzed in this project.*

The production figure shows an overall upward trajectory for the four selected crops, although the magnitude and timing of changes differ across crops.

Cassava displays the largest absolute production scale in the figure, with a pronounced increase in the later decades of the study period. Yam production also rises over time, with fluctuations and a noticeable increase in later years. Maize production increases overall, particularly toward the end of the period, while rice production remains comparatively lower in absolute tonnage.

These visual patterns suggest that the historical trajectories of the selected crops have not been identical. The differences highlight the importance of evaluating individual crop trends rather than assuming that all crops have experienced agricultural change at the same rate.

Production alone, however, cannot determine whether the observed increases resulted primarily from more land being harvested, higher yields, or a combination of both.

### 2. Changes in Harvested Area

![Line chart showing annual harvested area trends for maize, rice, cassava, and yams in Ghana from 1961 to 2024, measured in hectares.](https://github.com/user-attachments/assets/71391ecb-88dc-41d1-bdc4-f67ffaa424fd)

*Figure 2. Historical changes in harvested area for the four selected crops in Ghana, 1961–2024. Source: FAOSTAT data analyzed in this project.*

The harvested-area figure indicates an overall expansion in the area harvested for the selected crops, alongside substantial year-to-year fluctuations.

Maize shows considerable variation across the historical period, followed by a pronounced increase in harvested area in more recent years. Cassava also displays a broad upward trajectory. The harvested areas for rice and yams increase over time, although their trajectories differ in magnitude and timing.

These patterns indicate that changes in harvested area are an important dimension of the observed production trends.

However, harvested area should not be interpreted as a direct measure of total agricultural land, farm size, or permanent expansion of cultivated land. The indicator records the area harvested for a particular crop and does not independently establish the underlying land-use changes.

Further investigation would be required to determine how much of the observed increase in total production can be attributed to changes in harvested area.

### 3. Long-Term Crop Yield Trends

![Line chart showing annual yield trends for maize, rice, cassava, and yams in Ghana from 1961 to 2024, measured in kilograms per hectare.](https://github.com/user-attachments/assets/6fecbb6d-779c-4d6d-ade1-6aee5b8592f9)

*Figure 3. Historical yield trends for maize, rice, cassava, and yams in Ghana, 1961–2024. Source: FAOSTAT data analyzed in this project.*

The yield figure shows an overall upward trajectory across the selected crops, but with differences in the magnitude, timing, and variability of change.

Cassava displays a substantial increase in reported yield in the later years. Yam yield also increases over the study period, with notable fluctuations in earlier observations and a general upward trajectory in subsequent years.

Maize and rice exhibit lower yield values on the chart's common vertical scale, although both show an overall increase toward the end of the period.

The differences in scale are important when interpreting this figure. A single axis makes it possible to compare the magnitude of recorded yields, but it can make fluctuations in lower-yielding crops more difficult to see. Separate crop-specific plots or carefully designed indexed comparisons could help investigate their temporal patterns in greater detail.

Yield is an indicator of output per harvested hectare, not a direct measure of technical efficiency or the adoption of improved farming practices. The observed trends do not establish which production factors contributed to the changes.

## Key Findings

The project reports the following principal findings from the exploratory analysis and linear trend assessment.

### 1. Positive estimated long-term trends

All 12 crop-indicator combinations were reported to have positive estimated linear trend slopes.

This result indicates that the fitted linear trends point upward for production, harvested area, and yield across the four selected crops. It does not imply that every annual observation increased or that the trajectories followed a straight line.

### 2. Production increased alongside changes in harvested area

The production and harvested-area figures both display broad upward trajectories.

This provides a basis for investigating the relationship between land area harvested and total crop output. However, the relative contribution of harvested area and yield to production changes requires further quantitative assessment.

### 3. Yield trajectories differed among crops

The yield figure shows differences in the magnitude and timing of changes across the four crops.

These differences reinforce the need to analyze crop-specific production systems rather than assume that a single pattern adequately describes all agricultural commodities.

### 4. Historical changes were not uniform

The visualizations contain periods of relatively gradual change, noticeable fluctuations, and more pronounced increases.

Consequently, a single linear trend provides a useful summary of the overall direction of change but may not capture important shifts within the 64-year period.

### 5. Statistical trends do not establish causation

An estimated positive trend, even when statistically significant, does not independently explain why a crop's production, harvested area, or yield changed.

Potential explanations involving climate, agricultural inputs, improved varieties, technology, policy, and management practices remain hypotheses for further investigation unless they are examined using appropriate data and methods.

**Important distinction:** The findings above summarize the reported project outputs and the supplied figures. Exact slope estimates, p-values, confidence intervals, and crop-specific changes should be obtained from the corresponding result tables before making more precise quantitative claims.

## Analytical Methods

The project was conducted in Python using Google Colab, with a workflow designed to support transparent agricultural data analysis.

### 1. Data selection and filtering

The original FAOSTAT data were filtered to retain Ghana, the four selected crops, the three agricultural indicators, and the years 1961–2024.

### 2. Data quality assessment

The dataset was examined for dimensions, year coverage, missing values, duplicates, measurement units, and available data flags.

### 3. Descriptive statistical analysis

Summary statistics were calculated to examine the distributions and variability of production, harvested area, and yield.

Descriptive statistics provide information about the observed data but do not independently explain the processes underlying the recorded patterns.

### 4. Time-series visualization

Line charts were produced to examine annual changes in each indicator and compare the historical trajectories of the selected crops.

These visualizations were used to identify broad patterns, fluctuations, and differences in scale.

### 5. Long-term change assessment

Values from 1961 and 2024 were compared to describe changes between the beginning and end of the study period.

Endpoint comparisons provide a useful summary, although they do not capture all fluctuations occurring between those years.

### 6. Linear trend analysis

Linear regression was used to estimate the direction and magnitude of trends over time and assess their statistical significance.

The estimated slope summarizes the average linear change associated with a one-year increase in the time variable. Its interpretation depends on the indicator and its measurement unit.

For example, a production slope is expressed in tonnes per year, while a yield slope is expressed in kilograms per hectare per year.

Statistical significance was considered as evidence about the estimated linear relationship, not as proof of a causal mechanism or an indication of practical importance.

### 7. Interpretation and scientific communication

The findings were interpreted by distinguishing total production, harvested area, and yield, acknowledging differences across crops, and identifying methodological limitations that affect the conclusions.

## Limitations and Interpretation

Several limitations should be considered when interpreting this analysis.

### Observational design

The project uses historical agricultural statistics rather than a controlled experiment. It can describe patterns and estimate trends but cannot establish causal relationships.

### Linear model assumptions

Linear regression provides a simplified summary of long-term trends. Agricultural time series may exhibit serial correlation, non-linear patterns, structural changes, and variation in the magnitude of annual fluctuations.

These features may affect conventional estimates of statistical uncertainty and significance. The trend results should therefore be interpreted in light of the model's assumptions.

### Data uncertainty and reporting

FAOSTAT records may incorporate estimates, imputed values, or information supplied by national authorities and other sources. Relevant flags and metadata should be considered when assessing data quality and comparability.

### National-level aggregation

The analysis focuses on national-level statistics for Ghana. It does not examine differences between individual farms, districts, agroecological zones, or production systems.

National trends may conceal substantial local variation.

### Interpretation of yield

Yield is measured as output per harvested hectare. Changes in this indicator do not necessarily imply improvements in every aspect of productivity, profitability, resource-use efficiency, or environmental sustainability.

### Comparability across crops

The selected crops differ in their biological characteristics, production practices, and typical yield levels. Comparisons should therefore consider the meaning and scale of each indicator rather than interpret numerical differences as direct rankings of agricultural performance.

### Scope of explanatory variables

Rainfall, temperature, soil characteristics, fertilizer use, seed varieties, irrigation, mechanization, prices, and agricultural policies were not jointly modeled in this project.

The analysis consequently does not identify which factors explain the historical trends.

## Research and Agricultural Relevance

This project illustrates how historical agricultural statistics can be used to investigate questions about crop production and land productivity.

For agricultural research, the combined analysis of production, harvested area, and yield provides a useful starting point for distinguishing changes in total output from changes in output per unit of land.

The findings also motivate additional questions:

- To what extent are changes in crop production associated with harvested-area expansion rather than changes in yield?
- Have crop-specific trends changed direction or magnitude during particular periods?
- How do rainfall and temperature variability relate to annual yield fluctuations?
- Do national trends conceal differences across Ghana's agroecological zones?
- How might additional data on agricultural inputs and production practices improve the interpretation of observed trends?

These are potential directions for further research, not conclusions established by the current analysis.

The project also demonstrates the application of data preparation, statistical reasoning, visualization, and reproducible analytical practices to a clearly defined agricultural question. These methods are relevant to further study in agricultural science, crop science, sustainable agriculture, and related interdisciplinary fields.

## Repository Structure

The repository is organized to separate the analytical notebook, data, visualizations, and derived results.

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

### Repository contents

| Path | Purpose |
|---|---|
| `data/ghana_crop_data_clean.csv` | Cleaned crop-indicator dataset |
| `figures/` | Visualizations of production, harvested area, and yield |
| `notebooks/Ghana_Crop_Production_Yield_Analysis.ipynb` | Main analytical notebook |
| `results/summary_statistics.csv` | Descriptive statistical outputs |
| `results/long_term_change.csv` | Beginning-to-end period comparisons |
| `results/linear_trend_results.csv` | Estimated linear trend results |
| `requirements.txt` | Python dependency list |
| `LICENSE` | Repository licensing information |

The paths above describe the intended repository structure and should be checked against the published repository before release.

## Tools and Technologies

The following tools supported the analysis:

- **Python:** General-purpose analytical programming.
- **pandas:** Data manipulation, filtering, and tabular analysis.
- **NumPy:** Numerical operations.
- **Matplotlib:** Statistical visualization and plotting.
- **SciPy:** Scientific computing and statistical methods, where used in the notebook.
- **Google Colab:** Cloud-based notebook execution.
- **GitHub:** Version-controlled project presentation and sharing.

These tools serve as analytical means for investigating agricultural questions. The primary focus of the project is the interpretation of crop production, harvested area, and yield trends.

## Reproducibility

Reproducibility is an important component of transparent agricultural research.

The repository is intended to provide the analytical notebook, cleaned dataset, derived tables, and figures required to inspect the analysis.

### Steps to reproduce the analysis

1. Clone or download the repository.
2. Open `notebooks/Ghana_Crop_Production_Yield_Analysis.ipynb` in Google Colab or a compatible Jupyter environment.
3. Obtain the corresponding original dataset from the [FAOSTAT Crops and livestock products domain](https://www.fao.org/faostat/en/#data/QCL).
4. Follow the notebook's data-loading and filtering instructions.
5. Install the dependencies specified in `requirements.txt`, if required.
6. Run the notebook cells in sequence.
7. Compare the generated figures and result tables with the outputs included in the repository.

The reproducibility instructions depend on the notebook's actual data-loading configuration and the continued availability of the original source data.

## Potential Future Research

The current analysis establishes a descriptive foundation for several possible extensions.

### Climate and crop productivity

Integrate suitable rainfall and temperature records to investigate associations between climatic variability and annual crop yields.

### Yield variability

Examine year-to-year variation, identify periods of unusual changes, and evaluate whether linear trends adequately summarize the observed trajectories.

### Crop-specific trend changes

Investigate potential changes in trend magnitude or direction over time using methods appropriate for historical agricultural time series.

### Regional agricultural analysis

Where comparable data are available, investigate differences among regions or agroecological zones within Ghana.

### Agricultural inputs and production systems

Explore whether additional data on fertilizer use, irrigation, seed varieties, mechanization, or other production factors help explain observed patterns.

### Robustness of statistical inference

Evaluate alternative trend specifications and account for time-series characteristics, including serial correlation, when estimating uncertainty.

These extensions would require additional data, explicit research questions, and suitable analytical methods. They are proposed research directions rather than completed components of the present project.

## Conclusion

This project examines the long-term evolution of maize, rice, cassava, and yam production in Ghana between 1961 and 2024 using FAOSTAT agricultural statistics.

By examining production, harvested area, and yield separately, the analysis provides a structured description of changes in agricultural output and land productivity across four selected crops.

The reported results indicate positive estimated linear trends for all 12 crop-indicator combinations, although the magnitude and timing of changes vary among crops and indicators. The visualizations also demonstrate why production, harvested area, and yield must be interpreted as related but distinct measures.

The study does not establish the causes of these trends. Instead, it provides a reproducible analytical foundation for further investigation into crop productivity, agricultural systems, and the factors associated with long-term agricultural change.

Ultimately, the project reflects my interest in applying quantitative methods to agricultural questions and developing the analytical and scientific reasoning needed for further graduate study in agriculture-related disciplines.

## About the Author

**Richard Antwi**

BSc in Agriculture, majoring in Animal Science

Research interests include agricultural production systems, crop productivity, livestock production, sustainable agriculture, and quantitative approaches to agricultural research.

This project forms part of my developing agricultural research portfolio, which explores how data analysis can support the investigation of agricultural production and productivity questions.

---

*Data source: Food and Agriculture Organization of the United Nations (FAO), FAOSTAT. Study period: 1961–2024. Country: Ghana.*

*This repository presents an exploratory analysis of historical agricultural statistics. Findings should be interpreted in accordance with the data, analytical methods, and limitations documented above.*
