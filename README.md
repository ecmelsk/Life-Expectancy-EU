# Life Expectancy Prediction in EU Countries (2000–2022)

This repository contains the Python code used in a published study I co-authored on life expectancy prediction across European Union countries. The study examines whether country-level health and economic indicators improve life expectancy prediction by comparing regression and machine learning models.

## Data

The study uses country-level data from 2000 to 2022, sourced primarily from:

- [OECD Data Explorer](https://data-explorer.oecd.org/)
- [World Bank Open Data](https://data.worldbank.org/)

The dataset is not included in this repository.

**Target variable:** Life expectancy (years)

**Predictors:**

- GDP per capita (PPP)
- Physicians per 1,000 population
- Alcohol consumption
- Health expenditure (PPP)
- Population aged 65 and over (%)

## Models

| Model | Approach |
|---|---|
| Linear Regression | Baseline regression model |
| Random Forest | Baseline and manually adjusted hyperparameters |
| Multilayer Perceptron (MLP) | Hyperparameter tuning using GridSearchCV and TimeSeriesSplit |

## Model Evaluation

- Training period: 2000–2018
- Testing period: 2019–2022
- Evaluation metrics: MAE, RMSE and R²
- Log transformation of selected predictors in the MLP model

The notebook also includes exploratory data analysis, country-level prediction errors, and comparisons of actual and predicted life expectancy.

## Repository Structure

```
Life-Expectancy-EU/
├── life_expectancy_eu_main_code.ipynb
└── README.md
```

## Requirements

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- statsmodels
- openpyxl
- jupyter

Install the required packages:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn statsmodels openpyxl jupyter
```

## How to Run

1. Clone or download the repository.
2. Prepare the merged dataset using the sources listed above.
3. Save the dataset as `final_merged_dataset_2000_2022_with_education_over65.xlsx` in the notebook directory.
4. Open `life_expectancy_eu_main_code.ipynb` in Jupyter Notebook or JupyterLab.

The merged dataset is required to reproduce the analysis.

## Related Publication

Kisa, E. S., Liu, Y., & Ren, H. (2026). Do macro-level health and economic indicators improve life expectancy prediction? Evidence from European country-level data. *Journal of Applied Business and Economics, 28*(6), 9–45.
