# Neuromuscular Predictors of Technical Performance in Conventional and Para Youth Table Tennis Players: An Exploratory Cross-Sectional Study

This repository contains the full dataset, source code, and statistical reports for the study: **"Neuromuscular Predictors of Technical Performance in Conventional and Para Youth Table Tennis Players: An Exploratory Cross-Sectional Study"**.

---

## 📂 1. Data Availability

The dataset is fully anonymized and hosted directly in this repository within the `data/` folder.

| File Name | Format | Description |
| :--- | :--- | :--- |
| **Data_TableTennis** | `.csv` | **Primary Dataset:** The original anonymized data from field tests (Semicolon `;` separator). This file is the direct input for all statistical models in the pipeline. |

---

## 💻 2. Reproducibility Pipeline

To replicate the study, run the Jupyter Notebook in the `notebooks/` folder. The analytical workflow is self-contained and modular:

### **Analytical Workflow (`MAIN_ANALYSIS.ipynb`)**
1. **Standardized Preprocessing:** Numeric cleaning, decimal comma handling, and automated header standardization.
2. **Reliability Analysis:** Calculation of **ICC (3,1)** (Two-way mixed, consistency) and **CV%** derived from Typical Error of Measurement (%TEM).
3. **Group Comparisons:** Independent T-tests with **Welch’s correction** and **Hedges’ g** effect sizes for small sample bias.
4. **RSI Optimization (ANOVA):** **Repeated Measures ANOVA** across 15cm, 30cm, and 45cm drop heights to identify optimal mechanical loads.
5. **Predictive Modeling:** **Spearman Correlations** and **Simple Linear Regression (OLS)** to determine performance predictors.

---

## 📊 3. Key Findings Summary

The following results were generated directly from the analytical pipeline:

### **RSI Optimization (ANOVA)**
- **Insight:** 30cm was identified as the descriptive peak of performance for both groups. 
- **Stats:** Conventional ($F=1.36, p=0.269$); Para-athlete ($F=1.71, p=0.206$). Despite the lack of omnibus significance, 30cm was selected for regression models as the optimal mechanical load.

### **Predictive Modeling (Regression)**
- **Conventional Group:** 10m Sprint significantly predicts **36%** of Peak Ball Velocity ($R^2=0.36, p=0.007$).
- **Para-athlete Group:** RSI at 30cm explains **26%** of Technical Efficiency ($R^2=0.26, p=0.106$), showing a moderate trend despite the small sample size ($n=11$).

### **Inter-group Differences**
- **Insight:** Conventional athletes show significantly higher RSI at 30cm ($p=0.0068$) with a **Large** effect size (**$g=1.08$**).

---

## ⚙️ Requirements

Install the necessary Python stack using:

```bash
pip install pandas numpy scipy statsmodels matplotlib seaborn

📞 Contact
Corresponding Author listed on the manuscript.
