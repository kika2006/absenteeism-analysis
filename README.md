# Absenteeism at Work: From Exploration to Prediction

**Author:** Francisca (Kika) Freixo  

A two-part analysis of employee absenteeism. Part 1 explores what drives hours missed. Part 2 predicts whether an absence will be long or short and compares classifiers.

**R · ggplot2 · corrplot · caret · class (k-NN) · rpart**

📄 Reports: **[1 – Exploratory analysis](https://kika2006.github.io/reports/absenteeism_eda.html)** · **[2 – Predictive modelling](https://kika2006.github.io/reports/absenteeism_models.html)**

---

## Part 1: Exploratory data analysis
- Data-quality checks (no missing values) and outlier detection with the IQR rule.
- Violin and box plots of absenteeism by season, education, pets, smoking and disciplinary record, plus a correlation heatmap.
- Findings: no single strong driver; disciplinary failure and BMI show the clearest links, and winter has the most absenteeism. The report closes with recommendations for management, such as flexible work in peak seasons and transport support.

## Part 2: Predictive modelling
- Target: absence above or below the median duration (High / Low).
- 70/30 split, checked with t-tests on age and BMI.

| Model | Test accuracy |
|---|---|
| **Decision tree (pruned)** | **80.2%** |
| k-NN, tuned with 10-fold cross-validation (k = 3) | 74.3% |
| k-NN (k = 11) | 73.4% |
| Logistic regression (baseline) | 36.0% |

The pruned decision tree was recommended because it is the most accurate model and is still easy for managers to read.

## Running it
Download the [UCI Absenteeism at Work dataset](https://archive.ics.uci.edu/dataset/445/absenteeism+at+work) into `data/`, then knit the two `.Rmd` files.

*Maastricht University, Knowledge Discovery & Data Visualisation (2024). Pair project.*
