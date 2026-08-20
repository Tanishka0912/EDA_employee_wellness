# Employee Wellness Analysis — Mental Health in Tech

Exploratory Data Analysis (EDA) on a mental health in tech workplace survey, covering data cleaning, visualization, and correlation analysis of factors linked to employees seeking treatment.

## Project Overview
This project cleans a raw employee wellness survey dataset and explores relationships between workplace factors (remote work, company benefits, family history, work interference, etc.) and whether employees sought mental health treatment.

## Files
- `EDA_project.ipynb` — full analysis notebook: data cleaning, visualizations, and correlation analysis
- `employee_wellness_dataset.csv` — raw survey dataset
- `requirements.txt` — Python libraries needed to run the notebook

## Key Findings
1. 48.81% of employees reported having sought treatment for a mental health condition.
2. Family history showed a strong link to treatment-seeking (73.02% vs 33.59% without family history).
3. Treatment rates were higher among employees reporting greater work interference from mental health issues.
4. Remote work and age showed little to no correlation with treatment.
5. Findings suggest workplaces should improve mental health awareness, offer confidential support, and encourage regular check-ins.

## How to Run
1. Clone this repository or download the files
2. Install the required libraries:
   ```
   pip install -r requirements.txt
   ```
3. Open `EDA_project.ipynb` in Jupyter Notebook or JupyterLab and run all cells

## Tools Used
- Python (pandas, numpy)
- Matplotlib, Seaborn, Plotly for visualization
