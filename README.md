# workload-mental-health-ols

> Modeling the relationship between academic workload and mental health  
> in university students using OLS linear regression built from scratch with NumPy.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square)
![NumPy](https://img.shields.io/badge/NumPy-OLS%20from%20scratch-teal?style=flat-square)
![Course](https://img.shields.io/badge/CSE303-Statistics%20for%20Data%20Science-green?style=flat-square)
![n](https://img.shields.io/badge/n-205%20students-orange?style=flat-square)

---

## Overview

This project investigates how academic workload factors — course load, study hours,
deadlines, and extracurricular commitments — affect mental health outcomes (stress,
anxiety, sleep quality) among university students.

Three OLS linear regression models were implemented manually using NumPy (no sklearn
or statsmodels), and evaluated using R², RMSE, F-statistic, and p-value.

---

## Dataset

| Property | Detail |
|---|---|
| Total records | 205 students |
| Real responses | 55 (survey) |
| Synthetic records | 150 (generated to augment) |
| Collection method | Google Forms survey |
| Target variable | Mental health score (anxiety / stress / sleep) |

---

## Project Structure

```
workload-mental-health-ols/
├── Project-Data/
│   ├── survey_responses_auto_generated_data.csv          # Generated 150 survey responses
│   └── survey_responses_real_data.csv   # original 55-record dataset
├── Project-materials/
│   └── Presentation_Slide
|   └── Project_Report
|   └── Project Idea
|   └── Report-Template
├── Figures/
|   └── activities_stress
|   └── boxplot_gender
|   └── boxplot_year
|   └── correlation
|   └── demographics
|   └── distributions
|   └── model1
|   └── model2
|   └── model3
|   └── r2_comparison
├── workload_mental_health_analysis.ipnyb
└── README.md
```

---

## Methods

### Data Preprocessing
- Handled missing values via mean/mode imputation
- Label-encoded categorical variables (gender, major, year)
- Scaled continuous features for comparability

### Exploratory Data Analysis
- Distribution plots for all features
- Boxplots by stress/anxiety levels
- Pearson correlation heatmap

### OLS Linear Regression (NumPy, from scratch)

β = (XᵀX)⁻¹ Xᵀy

Three models were built and compared:

| Model | Predictor(s) | Target | R² |
|---|---|---|---|
| M1 | Study hours | Stress score | ~0.18 |
| M2 | Number of courses | Anxiety score | ~0.21 |
| M3 | Study hours + courses + sleep | Mental health index | ~0.29 |

### Evaluation Metrics
- R² (coefficient of determination)
- RMSE (root mean squared error)
- F-statistic and p-value for overall model significance

---

## Key Findings

- Course count and weekly study hours are the strongest predictors of mental health outcomes.
- Students enrolled in 5+ courses reported significantly higher anxiety levels.
- Sleep quality partially mediates the workload–stress relationship.
- Best model: **M2** (Courses → Anxiety, R² = 0.214)

---

## Requirements

```
numpy
pandas
matplotlib
seaborn
jupyter
```

Install with:

```bash
pip install -r requirements.txt
```

---

## Usage

```bash
git clone https://github.com/yourusername/workload-mental-health-ols.git
cd workload-mental-health-ols
jupyter notebook notebooks/
```

---

## Authors

| Name | Student ID |
|---|---|
| Belal Hossain | 2023-2-60-010 |
| Github | [ht](https://github.com/itsme-belal/) |
| Linkdin | [ht](https://linkdin.in/itsme-belal/) |

---

## License

Belal Hossain own it.
