# SASS Customer Churn Intelligence

A Python notebook for exploring customer churn across a synthetic SaaS customer dataset. The analysis uses **pandas**, **matplotlib**, and **seaborn** to review data quality, summarize churn, and identify industries with the highest churn counts.

## Key findings

- **50,000** customer records across **18 fields**
- **916** records marked churned (**1.83%** of the dataset)
- No duplicate rows or missing values were reported in the notebook
- Highest churn counts: **EdTech (128)**, **DevTools (121)**, **Logistics (119)**, **MarTech (113)**, and **CyberSecurity (112)**
- Churned accounts averaged **4.97 support tickets** in the prior 30 days, compared with **3.35** across all accounts
- Churned accounts averaged **24.8 active seats**, compared with **50.8** across all accounts

These are descriptive results. Industry counts are not industry-specific churn rates, and the comparisons do not establish causes of churn.

## Project contents

- `Untitled9.ipynb` - exploratory analysis notebook
- `MP_Synthetics_50000_Rows.csv` - input dataset (not included here)

## Requirements

Python 3.10 or later, with:

```bash
pip install pandas matplotlib seaborn jupyter
```

## Run the notebook

1. Place `MP_Synthetics_50000_Rows.csv` in a local data folder.
2. Open `Untitled9.ipynb` in Jupyter Notebook or JupyterLab.
3. Update the `path` variable near the start of the notebook to the CSV's location.
4. Run the notebook cells from top to bottom.

```python
path = r"data/MP_Synthetics_50000_Rows.csv"
df = pd.read_csv(path)
```

## Analysis workflow

1. Load and inspect the customer table.
2. Check duplicate rows, missing values, column types, and churn labels.
3. Summarize the full customer base and filter churned accounts.
4. Rank industries by churned-customer count and visualize the top five.

## Suggested next steps

Compare churn **rates** by industry, plan, billing cycle, tenure, feature adoption, and payment status. Test whether support volume, product activity, or seat utilization changes before churn, then validate any retention actions against later cohorts.
