# Week 2 EDA Assignment — Missing Data, Imputation & Outlier Handling

**Name:** [Your Name Here]
**Program:** Data Science Internship Program (Mentor: Laiba Sattar)
**Dataset:** [New York City Airbnb Open Data (2019)](https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data) — 48,895 listings, 16 columns

## What's in this repo

- `week2_eda_assignment.ipynb` — the full notebook: missing-data diagnosis (MCAR/MAR/MNAR), imputation strategy per column, IQR + Z-score outlier detection, a business-judgment outlier decision tree, and 20 advanced EDA commands, each with a written interpretation.
- `AB_NYC_2019.csv` — the raw dataset (upload alongside the notebook if re-running in Colab).

## 3 Key Findings

1. **Missingness in `last_review` and `reviews_per_month` (~20.6% each) is structural, not random.** A mechanism test confirmed both are missing in exactly the same rows — the ones with zero reviews. These listings simply have no review history yet, which ruled out mean/date imputation in favor of a domain-informed fill plus a `has_review` flag.
2. **Outlier handling turned out to be a judgment call, not a single formula.** The IQR method flagged 6.08% of listings as price outliers vs. only 0.79% for Z-score — IQR is the right choice here because price is extremely right-skewed (skew ≈ 19.1). Within those outliers, 88% were legitimate luxury entire-apartment listings (kept and flagged as a feature), while 11 listings priced at exactly \$0 were clear data-entry errors, corrected and re-imputed by borough + room type.
3. **Location drives price far more than any single numeric feature does.** No numeric column correlates with price above |0.15|, but the pivot table and borough-level medians tell a consistent story: Manhattan has both the highest prices (median \$150 vs. \$65 in the Bronx) and a housing mix skewed toward whole-apartment rentals, while outer boroughs lean toward cheaper private rooms.

## Week 1 Repo

[Link to Week 1 repo here] ← *replace with your actual Week 1 GitHub repo URL*
