# A-B-Testing-Regression-Analysis-Project-Marketing-Campaign-Analysis-Data-Analysis-Project
⭐ Starting from a business problem and research question 
⭐ Helping a marketing agency to select best platform to run ad campaigns 
⭐ Analysing and Visualising data to compare campaigns performance 
⭐ A/B Testing to select the best ad campaign platform to run ads 
⭐ Regression Analysis to get the expected conversions

# 🚀 Marketing Campaign Performance: A/B Testing & Predictive Analysis

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Manipulation-150458?logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-Hypothesis%20Testing-8CAAE6?logo=scipy&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Regression-F7931E?logo=scikit-learn&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0)

## 📌 Project Overview
As a data-driven marketing agency, maximizing **Return on Investment (ROI)** and minimizing **Customer Acquisition Cost (CAC)** are critical to scaling client growth. This project evaluates **1,000 parallel campaign records** spanning **December 22, 2021 – December 20, 2024**, comparing the effectiveness of **Facebook Ads** against **Google AdWords**.

Using **Exploratory Data Analysis (EDA)**, **Two-Sample Independent A/B Testing ($t$-test)**, **Linear Regression**, and **Monthly Time-Series Tracking**, this analysis uncovers which platform drives superior conversion efficiency and provides actionable budget reallocation strategies.

---

## 🎯 Business Problem & Research Questions
Leadership needs statistically validated evidence—beyond surface-level impressions and clicks—to allocate future digital advertising budgets effectively.

1. **Conversion & Cost Efficiency:** Which platform (**Facebook Ads** vs. **Google AdWords**) delivers higher conversion volume, conversion rate, and lower acquisition cost?
2. **Statistical Significance (A/B Testing):** Does hypothesis testing ($\alpha = 0.05$) confirm a statistically significant difference in mean daily conversions between the two platforms?
3. **Predictive Modeling (Regression):** How strongly do daily ad clicks and ad spend linearly predict daily conversions?
4. **Seasonality & Trends:** How do monthly conversion trends evolve across both platforms over the multi-year period?

---

## 📊 Dataset Schema
The dataset (`A_B_testing_dataset.csv`) contains **1,000 daily campaign records** across **17 features**:

| Feature Category | Facebook Columns | Google AdWords Columns | Description |
| :--- | :--- | :--- | :--- |
| **Date** | `date_of_campaign` | `date_of_campaign` | Daily campaign timestamp (`2021-12-22` to `2024-12-20`) |
| **Impressions** | `facebook_ad_views` | `adword_ad_views` | Total ad views/impressions |
| **Engagement** | `facebook_ad_clicks` | `adword_ad_clicks` | Total user clicks generated |
| **Conversions** | `facebook_ad_conversions` | `adword_ad_conversions` | Total completed target actions/sales |
| **Ad Spend** | `facebook_cost_per_ad` | `adword_cost_per_ad` | Total daily ad expenditure ($) |
| **Efficiency KPIs** | `facebook_ctr`, `facebook_conversion_rate`, `facebook_cost_per_click` | `adword_ctr`, `adword_conversion_rate`, `adword_cost_per_click` | Click-Through Rate (%), Conversion Rate (%), and Cost Per Click ($) |

---

## 📈 Key Results & Statistical Findings

### 1. Platform Performance Comparison (EDA)
| Metric | Facebook Ads | Google AdWords | Winner / Insight |
| :--- | :---: | :---: | :--- |
| **Total Views** | 2,152,031 | **4,771,438** | AdWords generated **2.2x** more reach |
| **Total Clicks** | 44,196 | **60,128** | AdWords drove **36%** more clicks |
| **Total Conversions** | **11,975** | 5,933 | **Facebook delivered >2x conversions** |
| **Total Ad Spend** | $156,610 | **$124,741** | Lower total outlay on AdWords |
| **Average CTR (%)** | **2.28%** | 1.28% | Higher click engagement on Facebook |
| **Avg Conversion Rate (%)** | **32.70%** | 10.81% | **Facebook converted at a 3x higher rate** |
| **Average CPC ($)** | $4.31 | **$2.27** | Cheaper clicks on AdWords |
| **Effective CPA ($/Conv.)** | **$13.08** | $21.02 | **38% lower acquisition cost on Facebook** |

### 2. A/B Testing (Independent Two-Sample T-Test)
* **Null Hypothesis ($H_0$):** $\mu_{\text{Facebook}} = \mu_{\text{AdWords}}$ (No significant difference in mean daily conversions).
* **Alternative Hypothesis ($H_1$):** $\mu_{\text{Facebook}} \neq \mu_{\text{AdWords}}$ (Statistically significant difference exists).
* **Test Results:**
  * **$t$-Statistic:** `40.2591`
  * **$p$-Value:** `6.8864e-237` ($p < 0.0001$)
  * **Conclusion:** **Reject $H_0$.** Facebook's higher conversion output is overwhelmingly statistically significant (>99.9% confidence).

### 3. Linear Regression Analysis
* **Features ($X$):** `facebook_ad_clicks`, `facebook_cost_per_ad` $\rightarrow$ **Target ($y$):** `facebook_ad_conversions`
* **$R^2$ Score:** `0.0001` | **RMSE:** `4.2961`
* **Insight:** Daily clicks and raw spend alone exhibit near-zero linear correlation with daily conversions, proving that **audience targeting quality, creative relevance, and external seasonality** drive conversions rather than raw click volume.

---

## 💡 Business Recommendations
1. **Reallocate Primary Ad Spend:** Shift **65%–70% of the conversion-focused ad budget** to **Facebook Ads** to capitalize on its `32.70%` conversion rate and lower Customer Acquisition Cost (`$13.08` vs. `$21.02`).
2. **Optimize the Google AdWords Funnel:** Audit AdWords landing pages, ad copy, and keyword intent to address the drop-off between high click volume (`60,128` clicks) and low conversion rate (`10.81%`). Leverage AdWords primarily for top-of-funnel brand visibility where its `$2.27` CPC excels.
3. **Enhance Predictive Modeling:** Incorporate granular features—such as audience demographics, ad formats, and day-of-week seasonality—to build non-linear forecasting models (e.g., Random Forest or Gradient Boosting).

---

## 🛠️ Tech Stack & Repository Structure
* **Language:** Python 3
* **Libraries:** `pandas`, `numpy`, `scipy`, `scikit-learn`, `matplotlib`, `seaborn`
* **Environment:** Jupyter Notebook

```text
├── A B Testing & Regression Analysis Project-Marketing Campaign Analysis-Data Analysis Project.ipynb
├── A_B_testing_dataset.csv
└── README.md
