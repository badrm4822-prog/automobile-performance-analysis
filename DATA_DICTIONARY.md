# Data Dictionary

| Field | Description |
|---|---|
| `car` | Vehicle make/model name |
| `mpg` | Fuel efficiency in miles per gallon; source zeros are treated as missing |
| `cylinders` | Engine cylinder count |
| `displacement` | Engine displacement |
| `horsepower` | Engine horsepower; source zeros are treated as missing |
| `weight` | Vehicle weight in pounds |
| `acceleration` | Time-based acceleration measure in seconds; lower is quicker |
| `model_year` | Vehicle model year, converted from 70-82 to 1970-1982 |
| `origin` | Manufacturing origin: US, Europe, or Japan |
| `origin_model` | Redundant source field combining origin and two-digit model year; excluded from the cleaned analytical dataset |
| `horsepower_per_1000_lb` | Derived horsepower-to-weight metric used for exploratory analysis |

## Missing-value rule
The raw file encodes unavailable MPG and horsepower observations as numeric zero. The analytical notebook converts these placeholders to `NaN` instead of imputing them in descriptive analysis. The optional baseline model uses median horsepower imputation inside its pipeline only.
