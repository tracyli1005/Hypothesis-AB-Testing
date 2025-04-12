# A/B Test Analysis for Web Page Conversion Rates

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Libraries](https://img.shields.io/badge/Libraries-pandas%7Cnumpy%7Cmatplotlib%7Csklearn-lightgrey)

This Jupyter Notebook analyzes the effectiveness of a &zwnj;**new webpage design**&zwnj; compared to an old version through rigorous A/B testing. The analysis combines statistical methods (hypothesis testing, simulations) and data science techniques to determine if the new page improves user conversion rates.

---

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Key Analysis Steps](#-key-analysis-steps)
- [Results & Conclusions](#-results--conclusions)
- [How to Use](#-how-to-use)
- [Libraries Used](#-libraries-used)

---

## 🎯 Project Overview
&zwnj;**Objective**&zwnj;:  
Evaluate whether a new webpage design (`new_page`) leads to statistically significant improvements in user conversion rates compared to the old design (`old_page`).

&zwnj;**Dataset**&zwnj;:  
`ab_data.csv` containing:
- `user_id`: Unique user identifier
- `timestamp`: Event time
- `group`: Treatment/Control group
- `landing_page`: Page version (new/old)
- `converted`: Binary conversion status (0/1)

---

## 🔍 Key Analysis Steps

### 1. Data Exploration & Cleaning
- ✅ Loaded 294,478 rows of user interaction data
- ✅ Identified and removed &zwnj;**3,894 misaligned rows**&zwnj; (treatment group users seeing old page / control group users seeing new page)
- ✅ Removed 1 duplicate user entry
- ✅ Verified &zwnj;**no missing values**&zwnj;

### 2. Descriptive Statistics
| Metric | Value |
|--------|-------|
| Overall Conversion Rate | 11.96% |
| Control Group (Old Page) Conversion | 12.04% |
| Treatment Group (New Page) Conversion | 11.88% |
| Probability of Receiving New Page | 50.02% |

### 3. Hypothesis Testing
- &zwnj;**Null Hypothesis (H₀)**&zwnj;: Old page conversion rate ≥ New page conversion rate  
- &zwnj;**Alternative Hypothesis (H₁)**&zwnj;: New page conversion rate > Old page conversion rate  

&zwnj;**Methodology**&zwnj;:
- Simulated 10,000 A/B test iterations under the null hypothesis
- Calculated p-value from sampling distribution of conversion rate differences

---

## 📈 Results & Conclusions
- &zwnj;**Observed Difference**&zwnj;: -0.16% (New Page underperformed Old Page)
- &zwnj;**Statistical Significance**&zwnj;:
  - p-value = 0.906 (>0.05 significance level)
- &zwnj;**Conclusion**&zwnj;:  
  Failed to reject the null hypothesis. &zwnj;**No sufficient evidence**&zwnj; to claim the new page improves conversions.

---
