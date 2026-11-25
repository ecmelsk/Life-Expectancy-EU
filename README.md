# Life Expectancy Prediction in EU Countries (2000–2022)

This project analyzes and predicts life expectancy across EU countries using regression and machine learning models. The dataset covers the period 2000–2022 and includes socioeconomic and health-related indicators sourced primarily from the OECD Data Explorer and the World Bank.

## Project Overview

Life expectancy is a key indicator of population health. This study examines which factors best explain variation across countries and over time, and compares the predictive performance of different modeling approaches.

**Target variable:** Life expectancy (years)

**Features used:**
- GDP per capita (PPP)
- Physicians per 1,000 population
- Alcohol consumption
- Health expenditure (PPP)
- Population aged 65+ (%)

## Models

| Model | Approach |
|---|---|
| Linear Regression | Baseline regression with sklearn pipeline |
| Random Forest (Tuned) | Ensemble model with GridSearchCV + TimeSeriesSplit |
| MLP (Neural Network) | MLPRegressor with hyperparameter tuning |

- Temporal train/test split: trained on 2000–2018, tested on 2019–2022
- Log transformation applied to skewed features (GDP, health expenditure)

## Repository Structure

```
life-expectancy-eu/
├── life_expectancy_eu_main_code.ipynb    # Main analysis notebook
└── README.md
```
## Data
Data is not included in this repository. Variables were sourced from:

OECD Data Explorer (main source)
World Bank Open Data

## Requirements

```
pandas
numpy
scikit-learn
matplotlib
seaborn
statsmodels
openpyxl
```

Install with:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn statsmodels openpyxl
```

## How to Run

1. Clone the repository
2. Download the dataset from the sources above (and merge) and place it in the same directory as the notebook
3. Open life_expectancy_eu_main_code.ipynb in Jupyter Notebook or JupyterLab
4. Run all cells in order

