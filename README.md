[README.md](https://github.com/user-attachments/files/33863584/README.md)
# Automobile Sales During Recessions

**Exploratory data analysis & visualisation | Python · pandas · Matplotlib · Seaborn · Folium**

A portfolio adaptation of my IBM *Data Visualization with Python* final-assignment notebook. I investigate how automobile sales differ across recession and non-recession periods and examine relationships with advertising, GDP, seasonality, consumer confidence, price and unemployment.

The dataset used in the original notebook contains **2,112 records** dated **1980–2023**. It is an IBM-hosted **educational dataset**; the analyses below are descriptive and should not be interpreted as estimates of real-world causal effects.

## Visualisation previews

The images below were saved from the original coursework notebook. Run the improved notebook to generate the current versions of the figures.

![Grouped average automobile sales by vehicle type and economic period](assets/vehicle_sales_comparison.png)

![Non-recession monthly seasonality bubble chart](assets/seasonality_bubble_chart.png)

## Questions explored

| Focus | Approach |
|---|---|
| Yearly automobile sales | pandas grouped means, Matplotlib line chart |
| Advertising expenditure vs sales | Annual trends with two y-axes; Pearson correlation |
| Recession vs non-recession sales | Seaborn grouped bar plots by vehicle type |
| GDP and economic conditions | Side-by-side yearly line charts |
| Seasonal sales patterns | Month-level Seaborn bubble chart |
| Consumer confidence and vehicle price | Recession-period scatter plots |
| Advertising allocation | Total-expenditure pie charts and monthly-normalised comparison |
| Unemployment and vehicle sales | Grouped mean sales and Seaborn line charts |
| Geographic distribution | Folium choropleth with state-name matching checks |

## Key observations

- The vehicle-type comparison in the original notebook shows **lower average automobile sales during recession periods** across the displayed categories.
- Average vehicle sales, advertising expenditure and macroeconomic indicators vary over time; these are **associations rather than causal estimates**.
- Non-recession records account for a larger share of total recorded advertising expenditure in the original pie chart. That figure **does not adjust for unequal time spent in recession and non-recession conditions**.
- The `City` field contains state-like labels in the source sample (e.g., Georgia, New York). The geographic visualisation validates labels against the state boundary GeoJSON and reports mismatches.

## Project structure

```text
automobile-sales-recession-analysis/
├── notebooks/
│   └── automobile_sales_analysis.ipynb
├── assets/
│   ├── vehicle_sales_comparison.png
│   ├── seasonality_bubble_chart.png
│   └── recession_advertising_share.png
├── requirements.txt
├── .gitignore
└── README.md
```

## Run locally

Requires **Python 3.10 or later**, Jupyter and an internet connection (for the remote CSV and US-states GeoJSON).

```bash
python -m venv .venv
source .venv/bin/activate  # macOS/Linux; on Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab
```

Open `notebooks/automobile_sales_analysis.ipynb` and choose **Run All Cells**. The notebook downloads the teaching data at execution time; it is not bundled in this repository.

## Data source & attribution

- [IBM/Skills Network automobile-sales.csv](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/d51iMGfp_t0QpO30Lym-dw/automobile-sales.csv)
- [IBM/Skills Network US-states GeoJSON](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DV0101EN-SkillsNetwork/Data%20Files/us-states.json)
- Based on the IBM Skills Network final assignment from the *Data Visualization with Python* course. The original notebook credits **Dr. Pooja** and includes **© 2023 IBM Corporation. All rights reserved.** This is an educational portfolio adaptation, not an independent dataset or an original research study.

## Notes on reproducibility

The code has been syntax-checked but **has not been rerun against the remote dataset in this packaged version**. The online source URLs must be available when executed. The preview figures are retained from the uploaded notebook and might differ visually from freshly generated outputs.
