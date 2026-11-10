# Applied Data Science Capstone - SpaceX Falcon 9 First Stage Landing Prediction

Goal: predict whether the Falcon 9 first stage will land successfully, because a reusable first stage is
the main reason SpaceX can advertise launches at ~$62M vs. $165M+ from other providers.

## Repository structure

| Folder | Content |
|---|---|
| `Modulo 1/` | Data collection (SpaceX REST API and Wikipedia web scraping) and data wrangling notebooks, plus `dataset_part_1.csv` |
| `Modulo 2/` | EDA with SQL (SQLite) and EDA with data visualization (matplotlib / seaborn) notebooks |
| `Modulo 3/` | Interactive map with Folium notebook and the Plotly Dash application (`dash/spacex-dash-app.py`) |
| `Modulo 4/` | Machine learning prediction notebook (logistic regression, SVM, decision tree, KNN) |

## Notebooks and code

1. `Modulo 1/1_CollectingData_SpaceX-DataCollectionAPI.ipynb` - data collection with the SpaceX API
2. `Modulo 1/1_CollectingData_Qebscraping.ipynb` - web scraping with BeautifulSoup
3. `Modulo 1/2_Data wrangling_v2.ipynb` - data wrangling and landing label (`Class`)
4. `Modulo 2/1_labs_ed_sql_sqllite.ipynb` - EDA with SQL
5. `Modulo 2/2_labs_eda_dataviz.ipynb` - EDA with data visualization and feature engineering
6. `Modulo 3/lab_launch_site_location.ipynb` - launch site locations and proximities with Folium
7. `Modulo 3/dash/spacex-dash-app.py` - Plotly Dash dashboard
8. `Modulo 4/1_SpaceX_Machine_Learning_Prediction_Part5.ipynb` - classification models

## Run the dashboard

```bash
pip install dash pandas plotly
python "Modulo 3/dash/spacex-dash-app.py"
```

Then open http://127.0.0.1:8050.

## Key results

- 90 Falcon 9 launches, 66.7% landed; success rate rose from 0% (2010-2013) to 86% (2019-2020).
- KSC LC-39A is the most successful launch site (77%).
- Logistic regression, SVM, decision tree and KNN all reach 83.3% test accuracy (15 of 18); the decision
  tree has the best cross-validated accuracy (87.5%).
