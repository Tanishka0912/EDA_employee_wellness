# Employee Wellness Dataset — Data Cleaning & EDA

Exploratory Data Analysis on a Mental Health in Tech survey dataset from **XYZ Technical Solutions**. The project cleans a raw, messy survey export and then tells a data story about mental health treatment patterns in the tech workplace through univariate, bivariate, and multivariate visualizations.

## 📌 Project Overview

The dataset captures employee responses about mental health, workplace policies, and treatment-seeking behavior. This project is split into two phases:

1. **Data Cleaning & Pre-processing** — fixing duplicates, invalid values, inconsistent categories, and missing data across 24 columns.
2. **Exploratory Data Analysis** — a storytelling walkthrough (Univariate → Bivariate → Multivariate) answering specific business questions with charts and inferences.

## 📂 Dataset

- **File:** `employee_wellness_dataset.csv`
- **Rows (after cleaning):** 1,047
- **Columns (after cleaning):** 24

Key fields include `Age`, `Gender`, `self_employed`, `family_history`, `treatment`, `work_interfere`, `no_employees`, `remote_work`, `tech_company`, `benefits`, `care_options`, `wellness_program`, `seek_help`, `anonymity`, `leave`, `mental_health_consequence`, `phys_health_consequence`, `coworkers`, `supervisor`, `mental_health_interview`, `phys_health_interview`, `mental_vs_physical`, and `obs_consequence`.

Columns dropped during cleaning: `comments` (87% missing), `state` (mostly non-US respondents), `Timestamp` (not relevant to analysis).

## 🧹 Data Cleaning Steps

1. **Removed exact duplicate rows** across the full dataset.
2. **Dropped `comments`, `state`, `Timestamp`** — too sparse or irrelevant.
3. **`Age`** — coerced to numeric; unrealistic values (<18 or >100) set to NaN.
4. **`Gender`** — standardized free-text entries into `Gender_clean` (Male/Female/Other).
5. **`self_employed`** — missing values filled with `"No"`.
6. **`treatment`, `family_history`** — checked for consistency (no missing values).
7. **`work_interfere`** — missing values filled with `"Not applicable"`.
8. **`no_employees`** — fixed corrupted date-like entries, filled missing with mode.
9. **`Country`, `benefits`, `tech_company`, `remote_work`** — missing values filled with mode.
10. **`care_options`, `wellness_program`, `seek_help`, `anonymity`** — missing values filled with mode.
11. **`leave`, `mental_health_consequence`, `phys_health_consequence`, `coworkers`, `supervisor`, `mental_health_interview`, `phys_health_interview`, `mental_vs_physical`, `obs_consequence`** — missing values filled with mode (or `"Don't know"` for `leave`).

## 📊 EDA — Key Charts

1. **Overall Treatment Need** (Pie chart, univariate) — What share of employees need mental health treatment?
2. **Employer Benefits vs Treatment-Seeking** (Countplot, bivariate) — Does knowing about mental health benefits drive more treatment-seeking?
3. **Family History vs Seeking Treatment** (Grouped bar from crosstab, bivariate) — Does a family history of mental illness predict treatment-seeking?
4. **Work Interference vs Treatment, by Gender** (Countplot with hue, multivariate) — How does work interference vary by gender?
5. **Correlation Heatmap** (multivariate) — Relationships between age, treatment, family history, and workplace factors.

## 🔑 Key Findings

- **48.8%** of employees (511 of 1,047) reported needing mental health treatment.
- Employees **with a family history** of mental illness sought treatment at a much higher rate (**73.0%**) than those without (**33.6%**).
- Treatment-seeking increases with the frequency of work interference — most respondents report interference as "Sometimes" rather than "Often," suggesting an everyday background strain rather than rare crises.
- Awareness of employer-provided mental health benefits correlates with higher treatment-seeking, but many employees simply **don't know** what their employer offers — pointing to a communication gap rather than a policy gap.
- Correlation ≠ causation: family history correlates with treatment (0.38), but this doesn't prove causation.

## 🎯 Recommendations

- Improve internal communication of existing mental health benefits and policies.
- Provide confidential, accessible support channels.
- Encourage regular mental health check-ins, especially for employees reporting work interference.

## 🛠️ Tech Stack

- Python
- pandas, numpy
- matplotlib, seaborn, plotly

## 🚀 Getting Started

```bash
git clone <repo-url>
cd <repo-folder>
pip install pandas numpy matplotlib seaborn plotly jupyter
jupyter notebook EDA_project.ipynb
```

Make sure `employee_wellness_dataset.csv` is in the same directory as the notebook before running.

## 📁 Repository Structure

```
.
├── EDA_project.ipynb              # Main notebook: cleaning + EDA
├── employee_wellness_dataset.csv  # Raw survey data
└── README.md
```

## 👥 Contributors

Chart-specific contributions noted in the notebook: Chandana, Tanishka, Swara.

## 📄 License

Add a license of your choice (e.g., MIT) here.
