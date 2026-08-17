# 📊 A/B Testing Analysis Project

[![Python](https://img.shields.io/badge/Python-3.10-blue)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0+-yellow)](https://pandas.pydata.org/)
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-orange)](https://powerbi.microsoft.com/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## 📝 Project Overview

This project is a comprehensive **A/B testing analysis** designed to evaluate the impact of a website design change on user **Click-Through Rate (CTR)**. The main objective is to determine whether the new version (treatment group) performs better than the current version (control group).

## 📁 Dataset

This project uses the **A/B Testing Dataset** from Kaggle, which contains 200,020 user sessions with the following columns:
- `click`: Binary indicator (1 = clicked, 0 = did not click)
- `group`: Control or Treatment group
- `session_time`: Session duration in minutes
- `click_time`: Timestamp of the click
- `device_type`: Mobile or Desktop
- `referral_source`: Source of traffic (Email, Search, Social, Direct, Ads)

### Key Features

- ✅ Data cleaning and validation
- ✅ Exploratory Data Analysis (EDA)
- ✅ Statistical hypothesis testing (Z-Test)
- ✅ Segmentation analysis (device type & referral source)
- ✅ Professional visualizations
- ✅ Interactive Power BI dashboard

---

## 🗂️ Project Structure

```text

AB_Testing_Project/
├── data/
│ ├── ab_test_dataset.csv # Raw dataset
│ └── cleaned_ab_test_data.csv # Cleaned dataset
├── notebooks/
│ └── 01_ab_test_analysis.ipynb # Main analysis notebook
├── src/
│ └── 01_ab_test_analysis.py # Python script
├── reports/
│ ├── images/
│ │ ├── eda/ # EDA visualizations
│ │ │ ├── group_distribution.png
│ │ │ ├── ctr_by_group.png
│ │ │ ├── device_distribution.png
│ │ │ └── session_time_analysis.png
│ │ └── final/ # Final report visualizations
│ │ ├── combined_ab_test_results.png
│ │ ├── ctr_comparison.png
│ │ ├── confidence_intervals.png
│ │ ├── lift_chart.png
│ │ └── device_segmentation.png
│ ├── summary_results.csv # Summary metrics
│ └── device_segmentation_results.csv
├── dashboard/
│ └── ab_test_dashboard.pbix # Power BI dashboard file
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt

```


---

## 🚀 Prerequisites & Installation

### Required Libraries

Install the required Python libraries using:

```bash
pip install -r requirements.txt
```

---

## 📊 How to Run

### 1. Run Python Script (Terminal)

```bash
python src/01_ab_test_analysis.py
```

### 2. Run Jupyter Notebook

```bash
jupyter notebook notebooks/01_ab_test_analysis.ipynb
```

# 📈 Key Results

## Statistical Summary

| Metric | Value |
| :--- | :--- |
| **Control Group CTR** | 20.08% |
| **Treatment Group CTR** | 49.65% |
| **Lift (Improvement)** | 147.29% |
| **Z-statistic** | 132.98 |
| **P-Value** | < 0.0001 |
| **95% Confidence Interval (Treatment)** | [0.4933, 0.4998] |

---

## Statistical Conclusion

With **P-Value < 0.05**, we reject the null hypothesis and conclude that:

> **The new design has a statistically significant positive effect on CTR.**

The **147% lift** indicates that the treatment group's CTR more than doubled compared to the control group.

---

## Segmentation Analysis

| Segment | Lift (Improvement) | P-Value |
| :--- | :--- | :--- |
| **Mobile Users** | 147.75% | < 0.0001 |
| **Desktop Users** | 146.24% | < 0.0001 |
| **Email** | Significant | < 0.0001 |
| **Search** | Significant | < 0.0001 |
| **Social Media** | Significant | < 0.0001 |
| **Direct** | Significant | < 0.0001 |

---

## 📊 Visualizations

### EDA (Exploratory Data Analysis) Charts

| Chart Name | Description |
| :--- | :--- |
| `group_distribution.png` | User distribution across control and treatment groups |
| `ctr_by_group.png` | CTR comparison with 95% confidence intervals |
| `device_distribution.png` | Device type distribution across groups |
| `session_time_analysis.png` | Session time distribution and boxplot analysis |

### Final Report Charts

| Chart Name | Description |
| :--- | :--- |
| `combined_ab_test_results.png` | Combined view of 4 key charts (one-page summary) |
| `ctr_comparison.png` | CTR comparison between control and treatment groups |
| `confidence_intervals.png` | 95% confidence intervals for each group |
| `lift_chart.png` | Lift (improvement) visualization |
| `device_segmentation.png` | Device-based segmentation analysis |

---

## 🖥️ Power BI Dashboard

An **interactive Power BI dashboard** with three pages:

### Page 1: Executive Summary
- **KPI Cards**: Display Control CTR, Treatment CTR, Lift, and P-Value
- **Bar Chart**: Visual comparison of CTR with confidence intervals
- **Slicer**: Filter by device type (Mobile / Desktop)

### Page 2: Segmentation Analysis
- **Grouped Bar Chart**: CTR by device type and group
- **Table**: CTR by referral source (Email, Search, Social, Direct, Ads)
- **Slicer**: Filter by device type

### Page 3: Trends & Details
- **Line Chart**: Daily CTR trend for each group over time
- **Slicers**: Date range, group, and device type filters
- **Data Table**: Raw data for detailed inspection and search

---

## 🛠️ Tools & Libraries Used

| Tool / Library | Purpose |
| :--- | :--- |
| **Python 3.10** | Primary programming language |
| **Pandas** | Data manipulation and processing |
| **NumPy** | Numerical computing |
| **Matplotlib & Seaborn** | Data visualization |
| **SciPy & Statsmodels** | Statistical analysis and hypothesis testing |
| **Power BI** | Interactive dashboard creation |


## ⚠️ Limitations and Future Work

- The experiment duration was limited to a specific timeframe; long-term effects are not yet measured.
- The dataset is simulated; real-world application may require additional validation.
- Future work could include:
  - Measuring the impact on **Revenue per User** and **Customer Lifetime Value**.
  - Analyzing the effect on **different user segments** (e.g., new vs. returning users).
  - Running the experiment on a **larger sample size** to detect smaller effects.

## 💡 Business Recommendations

Based on the A/B test results, we recommend:

1. **Deploy the new design to all users immediately**, as it significantly improves CTR by 147%.
2. **Prioritize mobile optimization**, since mobile users show the highest lift (147.75%).
3. **Run follow-up experiments** to test the new design on other key metrics (e.g., conversion rate, revenue per user).
4. **Monitor performance over time** using the Power BI dashboard to ensure the effect remains stable.
