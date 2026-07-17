<h1 align="center">🌍 Climate Change & Global Warming — ML Forecast to 2050</h1>

<p align="center">
  <a href="https://doi.org/10.5281/zenodo.21305984"><img src="https://img.shields.io/badge/DOI-10.5281%2Fzenodo.21305984-blue"></a>
  <img src="https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/-scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white">
  <img src="https://img.shields.io/badge/-Google%20Colab-F9AB00?style=flat&logo=googlecolab&logoColor=white">
</p>

<p align="center">
A machine learning study on 265 years of climate data — forecasting global land temperature to 2050 and identifying the fastest-warming regions on Earth.
</p>

> 📄 **Published:** This project is published as an open-access preprint on Zenodo — [DOI: 10.5281/zenodo.21305984](https://doi.org/10.5281/zenodo.21305984)

---

## 📖 Overview

This project uses the **Berkeley Earth Surface Temperature** dataset and the **Our World in Data CO₂ Emissions** dataset to build a scientifically valid forecasting model. Five candidate models were tested; **Ridge Regression** was selected as the final model based on accuracy, stability, and its ability to extrapolate to 2050.

## 🏆 Key Results

| Metric | Value |
|---|---|
| Final model | Ridge Regression (alpha=10) |
| Test R² | 0.9927 |
| MAE | 0.2805°C |
| RMSE | 0.3535°C |
| Cross-validation std | 0.0005 (5-fold TimeSeriesSplit) |
| **2050 forecast** | **10.18°C** absolute land temperature (+2.28°C since 1850) |
| Fastest-warming country | Mongolia (+1.836°C) |
| Fastest-warming city | Ulan Ude, Russia (+1.970°C) |

## 🗂 Data Sources

- Berkeley Earth Surface Temperature Dataset (Kaggle)
- Our World in Data — CO₂ & Greenhouse Gas Emissions Dataset (Kaggle)
- 📎 [Full datasets folder](https://drive.google.com/drive/folders/1IMbxsfS_X8Z1uAvAZ4kFAO3lvjf4dKyR?usp=sharing)

## 🔬 Methodology

1. Cleaned four raw CSV files independently
2. Merged Berkeley and OWID data at monthly resolution (1,992 records)
3. Engineered six features: `co2`, `Month_sin`, `Month_cos`, `Temp_lag12`, `co2_cumulative`, `Decade`
4. Used a strict chronological train-test split to avoid data leakage
5. Compared five models using `TimeSeriesSplit` cross-validation
6. Generated a 2050 forecast via sequential monthly iteration

## 🛠 Tech Stack

Python · pandas · numpy · scikit-learn · matplotlib · seaborn · Google Colab

## 📂 Repository Contents

```
├── Climate_Change_&_Global_Warming_climate_change_Project.ipynb   # full analysis + modeling pipeline
├── Project Report_Paper1.0/                                        # full written project report
└── README.md
```

## 👥 Authors

**Binyameen (Binz)** — Project Lead
M. Qasim · Abdul Mubeen · M. Hammad

University of Narowal — BS Computer Science, CSC 351 (Machine Learning)

## 📚 Citation

If you reference this work, please cite:

> Binyameen et al. (2026). *Climate Change and Global Warming: A Machine Learning Study Forecasting Global Land Temperature to 2050.* Zenodo. https://doi.org/10.5281/zenodo.21305984

## 📄 License

This project is for academic purposes. Data sources retain their original licenses (Kaggle / Berkeley Earth / OWID).

---

<p align="center"><i>📫 binyameen.binz@gmail.com · <a href="https://linkedin.com/in/binz1486">LinkedIn</a> · <a href="https://orcid.org/0009-0009-6395-063X">ORCID</a></i></p>
