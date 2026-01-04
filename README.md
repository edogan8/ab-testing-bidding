# 🧪 A/B Testing: Bidding Methods Analysis

This project utilizes statistical A/B testing to compare two bidding strategies ("Maximum Bidding" vs. "Average Bidding") for a marketing campaign. The goal is to determine if the new bidding strategy increases conversions or improves cost efficiency.

## 📊 Business Problem
A company introduced a new bidding type, **"Average Bidding"**, as an alternative to the existing **"Maximum Bidding"**. We conducted an A/B test for 30 days to answer:
* **"Does Average Bidding bring more sales?"**
* **"Is it cost-effective?"**

## 🛠️ Methodology
1.  **Data Preparation:** Control Group (Max Bidding) vs. Test Group (Average Bidding).
2.  **Assumption Checks:**
    * **Normality Check (Shapiro-Wilk):** Determining if data follows a normal distribution.
    * **Homogeneity Check (Levene):** Checking variance homogeneity.
3.  **Hypothesis Testing:**
    * Since the data did not follow a normal distribution, **Mann-Whitney U Test (Non-Parametric)** was applied.
4.  **Efficiency Analysis:**
    * Metrics: **Conversion Rate**, **Cost Per Purchase (CPP)**.
    * Visualization: Boxplots to analyze distributions and outliers.

## 📈 Key Findings
| Metric | Control Group (Max Bidding) | Test Group (Average Bidding) | Result |
|--------|-----------------------------|------------------------------|--------|
| **Avg Purchase** | 550.89 | 582.10 | **No Significant Difference (p>0.05)** |
| **Avg Spend** | $2,288 | $2,563 | **Significant Increase (p<0.05) ❌** |
| **Cost Per Purchase** | **$5.05** | **$5.90** | **Test Group is LESS Efficient** |

## 💡 Conclusion & Recommendation
* **Statistical Result:** There is **NO significant difference** in sales numbers between the two methods.
* **Business Insight:** The new method ("Average Bidding") costs significantly more to acquire the same number of customers. The Cost Per Purchase increased by approximately **$0.85 per customer**.
* **Recommendation:** 🛑 **STOP** the new bidding strategy and continue with the existing "Maximum Bidding" to prevent ROI loss.

---
*Analyzed with Python (Pandas, Scipy, Seaborn, Matplotlib)*

*Created by Muhammed Emir Doğan*