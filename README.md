# BreadBean Café Chain Analysis

### Project Overview

This project analyzes operating performance and site selection potential for a fictional café chain, **BreadBean**. The objective is to evaluate existing store profitability and model potential new sites based on demographic, competitive, and spatial characteristics.

### Repository Structure

```
breadbean-cafe-analysis/
├── data/
│   ├── raw/
│   │   ├── BreadBeanData.parquet                # Original dataset (renamed and standardized)
│   │   └── BreadBeanData_description.md         # Data dictionary and variable definitions
│   └── processed/
│       ├── BreadBeanData_Cleaned.parquet        # Cleaned and standardized dataset
│       └── BreadBeanFix_v95.parquet             # Winsorized variant (95th percentile capped)
│
├── notebooks/
│   └── BreadBean_Analysis.ipynb                 # Main analysis notebook
│
└── README.md
```

### Data Summary

* **Source**: Proprietary synthetic dataset representing 60 existing cafés and 10 candidate locations.
* **Key Variables**:

  * `PROFIT`: Annual operating profit ($1,000s)
  * `CAPITAL`: Investment cost ($1,000s)
  * `AREA`: Store size (square meters)
  * `INCOME`: Average household income in nearby area ($1,000s)
  * `POP_TOTAL` and `AGE_A–E`: Local population breakdown within 3 km radius
  * `COMPETITOR_COUNT`, `NONCOMPETITOR_COUNT`, `OTHER_BUSINESS_COUNT`: Competition indicators
  * `RENT_RATE`: Rent per square meter
  * `COST_INDEX`: Local cost-of-living index

### Data Processing

Two processed datasets are available:

1. **BreadBeanData_Cleaned.parquet** – standardized column names, numeric conversions, and missing-value handling.
2. **BreadBeanFix_v95.parquet** – an additional winsorized version where extreme or invalid values are replaced by the 95th percentile for robustness testing.

### Notebook Contents (`notebooks/BreadBean_Analysis.ipynb`)

1. **Data loading and standardization**
2. **Exploratory analysis** – distributions, correlations, and scatter plots
3. **Feature engineering** – per-capita indicators and derived ratios
4. **Regression modeling** – OLS models comparing raw vs per-capita predictors
5. **Diagnostics** – VIF, Durbin–Watson, Cook’s distance, and standardized coefficients
6. **Site selection modeling** – predicting profitability for potential new café locations

### Usage

```bash
# Clone the repository
git clone https://github.com/chaodajiang/breadbean-cafe-analysis.git

# Navigate into the project directory
cd breadbean-cafe-analysis

# Open the main analysis notebook
jupyter notebook notebooks/BreadBean_Analysis.ipynb
```

### Author

Developed by **Chaoda (Simon) Jiang** as part of the Business Analytics coursework at UC San Diego.

### License

This repository is intended for academic and portfolio presentation only. All data and analyses are fictional and not for commercial use.
