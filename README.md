# DATA-ANALYST-INTERNSHIP-Elevate-Labs-Task-11
---

## Objective
To determine whether the **treatment group (new landing page)** results in a statistically significant increase in **conversion rate** compared to the **control group (old landing page)**.

---

## Dataset
**Source:** Kaggle – Ecommerce AB Testing 2022 Dataset  
**Primary File:** `ab_data.csv`

### Dataset Description
| Column Name | Description |
|------------|------------|
| user_id | Unique identifier for each user |
| group | Experiment group (control / treatment) |
| landing_page | Page shown to the user (old_page / new_page) |
| converted | Conversion outcome (1 = Yes, 0 = No) |

---

## A/B Testing Methodology

### 1. Group Identification
- **Control Group:** Users who viewed the old landing page
- **Treatment Group:** Users who viewed the new landing page

---

### 2. Hypothesis Definition
- **Null Hypothesis (H₀):**  
  Conversion rate of the new landing page is equal to the old landing page.

- **Alternative Hypothesis (H₁):**  
  Conversion rate of the new landing page is different from the old landing page.

- **Significance Level (α):** 0.05

---

### 3. Metrics Calculated
- Total users per group
- Total conversions
- Conversion rate

Results stored in: `ab_test_summary.csv`

---

### 4. Statistical Test
- **Chi-Square Test of Independence**
- Appropriate for binary outcome variables (converted / not converted)

---

### 5. Results Summary
- Control conversion rate ≈ **12.04%**
- Treatment conversion rate ≈ **11.89%**
- **p-value > 0.05**

---

### 6. Confidence Interval
A 95% confidence interval for the difference in conversion rates includes **0**, indicating no statistically significant difference between groups.

---

## Visualization
- Bar chart comparing conversion rates of control and treatment groups
- Visual inspection supports statistical findings

---

## Final Conclusion
- The null hypothesis cannot be rejected
- The new landing page does **not** provide a statistically significant improvement in conversion rate

---

## Business Recommendation
Do not deploy the new landing page in production.

### Recommended Next Steps:
- Test alternative page designs
- Perform segmented analysis (country, device, traffic source)
- Increase test duration for stronger statistical power

├── ab_test_summary.csv
├── README.md
