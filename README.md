# Climate Change & Global Warming — ML Forecast (2050)

A machine learning project analyzing 265 years of global land temperature 
and CO2 emissions data to forecast global temperature in 2050 and identify 
the fastest-warming regions on Earth.

## Overview

This project uses the Berkeley Earth Surface Temperature dataset and the 
Our World in Data CO2 Emissions dataset to build a scientifically valid 
forecasting model. Five candidate models were tested; Ridge Regression 
was selected as the final model based on accuracy, stability, and its 
ability to extrapolate to 2050.

## Key Results

- Final model: Ridge Regression (alpha=10)
- Test R²: 0.9927 | MAE: 0.2805°C | RMSE: 0.3535°C
- Cross-validation std: 0.0005 (5-fold TimeSeriesSplit)
- 2050 forecast: 10.18°C absolute land temperature (+2.28°C since 1850)
- Fastest-warming country: Mongolia (+1.836°C)
- Fastest-warming city: Ulan Ude, Russia (+1.970°C)

## Data Sources

- Berkeley Earth Surface Temperature Dataset (Kaggle)
- Our World in Data — CO2 & Greenhouse Gas Emissions Dataset (Kaggle)

## Methodology

1. Cleaned four raw CSV files independently
2. Merged Berkeley and OWID data at monthly resolution (1,992 records)
3. Engineered six features: co2, Month_sin, Month_cos, Temp_lag12, 
   co2_cumulative, Decade
4. Used a strict chronological train-test split to avoid data leakage
5. Compared five models using TimeSeriesSplit cross-validation
6. Generated a 2050 forecast via sequential monthly iteration

## Tech Stack

Python, pandas, numpy, scikit-learn, matplotlib, seaborn, Google Colab

## Repository Contents

- `notebook.ipynb` — full analysis and modeling pipeline
- `report.pdf` — full written project report
- `/plots` — key visualizations (temperature trend, CO2 correlation, 
  geographic warming maps)

## Authors

Binyameen (Project Lead), M. Qasim, Abdul Mubeen, M. Hammad
University of Narowal — BS Computer Science, CSC 351 (Machine Learning)

## License

This project is for academic purposes. Data sources retain their 
original licenses (Kaggle/Berkeley Earth/OWID).

## Datasets Details

All Datasets files and related information can be found on https://drive.google.com/drive/folders/1IMbxsfS_X8Z1uAvAZ4kFAO3lvjf4dKyR?usp=sharing
