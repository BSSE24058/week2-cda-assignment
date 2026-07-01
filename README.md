# Week 1 — Data Science Internship Assignment

**Name:** Muhammad Abdul Rafay Khan
**Dataset used:** [COVID-19 Country Stats — Our World in Data](https://ourworldindata.org/coronavirus)
(pulled from the OWID public GitHub mirror: `owid/covid-19-data`)

## What's in this repo
- `week1_covid_eda.ipynb` — Full Google Colab notebook with:
  - Section 1: Dataset introduction
  - Section 2: The 7-command First-Look Protocol (`shape`, `dtypes`, `info()`, `describe()`, `isnull().sum()`, `value_counts()`, `duplicated().sum()`)
  - Section 3: 20+ additional EDA commands (head/tail/sample, nunique, unique, corr + heatmap, histograms, groupby, pivot_table, skew/kurt/cov, filtering, etc.) each with a written interpretation
  - Section 4: Three key findings in plain English

## How to run it
Open `week1_covid_eda.ipynb` in Google Colab and run all cells — the notebook downloads the dataset itself
directly from OWID's GitHub mirror (`raw.githubusercontent.com/owid/covid-19-data/master/public/data/owid-covid-data.csv`),
so no manual download or Kaggle login is needed.
