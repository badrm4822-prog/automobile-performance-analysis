# Automobile Performance Analysis - Executive Report

## Objective
Analyze historical automobile specifications to explain fuel-efficiency differences, identify long-term engineering trends, compare origins, and surface vehicles with unusual acceleration behavior.

## Data Quality
- Source rows: **406**
- MPG zero placeholders converted to missing: **8**
- Horsepower zero placeholders converted to missing: **6**
- Duplicate rows: **0**
- Historical period: **1970-1982**

## Main Findings
1. **Weight is the strongest simple MPG relationship** (correlation **-0.83**).
2. Engine displacement (**-0.80**) and horsepower (**-0.78**) are also strongly negatively associated with MPG.
3. **Japan** leads origin-level average MPG at **30.45 MPG**.
4. Average MPG improved by **79.3%** between 1970 and 1982, while average weight changed by **-28.7%**.
5. Using linear trend slope, **US** shows the fastest MPG improvement at about **1.13 MPG per year**.
6. **19 vehicles** have acceleration times more than two residual standard deviations from the displacement-based expectation.
7. A compact Ridge baseline explains the data well enough to validate the EDA: **test R² 0.85**, **MAE 2.28 MPG**.

## Interpretation
The dataset shows a strong historical trade-off between vehicle mass/engine intensity and fuel economy. Later model years are substantially more fuel-efficient and generally lighter with smaller, less powerful engines. Origin-level comparisons are useful as descriptive segments but should not be interpreted causally because vehicle mix differs by origin and year.

## Key Charts

### Weight vs MPG
![Weight vs MPG](../outputs/charts/04_weight_vs_mpg.png)

### MPG Trend
![MPG Trend](../outputs/charts/08_mpg_trend_over_time.png)

### Correlation Matrix
![Correlation Heatmap](../outputs/charts/07_correlation_heatmap.png)

### Baseline Model Importance
![Model Importance](../outputs/charts/12_mpg_model_permutation_importance.png)

## Deliverables
The `outputs/` directory contains the cleaned dataset, KPI summary, origin/cylinder/year summaries, trend tables, outlier records, model metrics, feature importance, and all charts.
