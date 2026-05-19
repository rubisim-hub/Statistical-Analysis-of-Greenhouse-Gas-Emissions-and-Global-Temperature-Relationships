# Statistical Analysis of Greenhouse Gas Emissions and Global Temperature Relationships

A data science project analyzing the relationship between greenhouse gas (GHG) emissions and global temperature change across 43 countries from 1990 to 2014.

Project report: [Statistical_Analysis_of_Greenhouse_Gas_Emissions_and_Global_Temperature_Relationships](https://www.genspark.ai/api/files/s/3gWmglc2)

---

## Project Overview

This project investigates how different greenhouse gases relate to global temperature changes and how emissions are distributed geographically across countries.

The analysis combines emissions data and temperature data to study:
- statistical relationships between greenhouse gases and temperature
- differences across gases and countries
- temporal and spatial emission patterns
- the relative climate impact of different gases

---

## Research Question

**How do different greenhouse gases relate to global temperature changes, and what is their geographical distribution?**

---

## Dataset Sources

This project uses two main datasets:

1. **UN International Greenhouse Gas Inventory**
   - 8,406 emission records
   - 7 greenhouse gases
   - 43 countries
   - years: 1990–2014

2. **FAO Environmental Change / Temperature Change data**
   - temperature-related measurements matched by country and year

Source: [Project report](https://www.genspark.ai/api/files/s/3gWmglc2)

---

## Greenhouse Gases Analyzed

The report analyzes seven greenhouse gases, including:
- Carbon dioxide (**CO2**)
- Methane (**CH4**)
- Nitrous oxide (**N2O**)
- HFCs
- PFCs
- SF6
- NF3

Source: [Project report](https://www.genspark.ai/api/files/s/3gWmglc2)

---

## Methods

Because the report found that the data distributions were not normal, the project uses non-parametric statistical methods alongside regression-based modeling.

### Statistical methods used
- **Shapiro-Wilk test** for normality testing
- **Spearman’s rank correlation coefficient**
- **Kruskal-Wallis test**
- **Dunn’s post-hoc test** with Bonferroni correction
- **Multivariate regression analysis**
- **Gini coefficient analysis** for spatial concentration
- **Global Warming Potential (GWP) analysis**

Source: [Project report](https://www.genspark.ai/api/files/s/3gWmglc2)

---

## Main Findings

Key findings reported in the project:

- Greenhouse gas emissions explain **78.2%** of temperature variation.
- **CO2 contributes 54.3%** of the explanatory power in the regression model.
- **CO2 accounts for 69.4%** of GWP-weighted climate impact.
- The **top 10 emitting countries account for 74.6%** of total global greenhouse gas emissions.
- **CO2 and CH4 together account for 88.1%** of total climate impact.

Source: [Project report](https://www.genspark.ai/api/files/s/3gWmglc2)

---

## Repository Structure

```text
ghg-temperature-statistical-analysis/
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
│
├── data/
│   ├── raw/
│   │   ├── un_ghg_emissions.csv
│   │   └── fao_temperature_data.csv
│   ├── interim/
│   └── processed/
│       └── merged_clean_dataset.csv
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_exploratory_data_analysis.ipynb
│   ├── 03_normality_tests.ipynb
│   ├── 04_correlation_analysis.ipynb
│   ├── 05_group_comparison_tests.ipynb
│   ├── 06_regression_analysis.ipynb
│   └── 07_gwp_gini_analysis.ipynb
│
├── src/
│   ├── __init__.py
│   ├── load_data.py
│   ├── clean_data.py
│   ├── merge_data.py
│   ├── stats_tests.py
│   ├── regression.py
│   ├── gini.py
│   ├── gwp.py
│   ├── plots.py
│   └── utils.py
│
├── outputs/
│   ├── figures/
│   ├── tables/
│   └── model_outputs/
│
└── reports/
    └── final_report.pdf
