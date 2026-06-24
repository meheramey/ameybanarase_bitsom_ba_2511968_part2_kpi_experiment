# Onboarding & Activation Experiment: Statistical Analysis

This document contains the complete analytical framework for both **Task 6 (Hypothesis Framework)** and **Task 7 (A/B Test Execution & Outputs)**.

---

## 📋 Part 1: Hypothesis Formulation (Task 6)

* **Metric Being Tested:** Paid Conversion Rate (Proportion of unique signed-up users converting to a paid plan within 30 days).
* **Significance Level ($\alpha$):** 0.05 (95% Confidence Level).
* **Test Type:** One-tailed Z-Test for Two Independent Proportions (Testing for directional improvement: Treatment > Control).

### Hypotheses:
* **Null Hypothesis ($H_0$):** $p_{\text{treatment}} \le p_{\text{control}}$
  The new onboarding experience has no positive impact on the Paid Conversion Rate.
* **Alternative Hypothesis ($H_1$):** $p_{\text{treatment}} > p_{\text{control}}$
  The new onboarding experience significantly increases the Paid Conversion Rate.

### Reason for Metric Selection:
Paid Conversion Rate directly aligns with company revenue growth and addresses the core problem statement where users were dropping off heavily right after the signup phase.

---

## 📊 Part 2: Statistical Test Outputs & Interpretation (Task 7)

### 1. Summary of Test Inputs
After rigorous structural deduplication and data cleaning, the unique sample sizes and inputs are:
* **Control Group ($N_1$):** 690 users | **Converted ($X_1$):** 22 users | **Conversion Rate ($p_1$):** 3.19%
* **Treatment Group ($N_2$):** 710 users | **Converted ($X_2$):** 50 users | **Conversion Rate ($p_2$):** 7.04%

### 2. Statistical Test Output (Excel Calculations)
* **Pooled Proportion ($p$):** 0.0514 (5.14%)
* **Standard Error (SE):** 0.0118
* **Calculated Z-Statistic ($Z_{\text{stat}}$):** 3.235
* **Critical Z-Value ($Z_{\text{crit}}$):** 1.645
* **Calculated p-Value:** 0.0006

### 3. Decision Rule & Conclusion
* **Decision Rule:** Reject $H_0$ if Calculated $Z_{\text{stat}} > 1.645$ and $p\text{-value} < 0.05$.
* **Statistical Verdict:** Since our Calculated Z-Statistic (**3.235**) is far greater than 1.645, and the $p\text{-value}$ (**0.0006**) is drastically below our significance threshold ($\alpha = 0.05$), we officially **Reject the Null Hypothesis ($H_0$)**.

### 4. Business Interpretation & Decision Link
* **Relative Performance Lift:** The treatment group showed an absolute lift of **+3.85%**, which is a **120.7% relative increase** over the control baseline.
* **Strategic Product Impact:** The math proves that the new friction-reduced onboarding flow structurally improves activation and drives user conversion. It is not a random fluke.
* **Connection to Business Decision:** This statistical victory justifies a global rollout. However, given that secondary guardrail metrics (support tickets) saw a spike, this rollout will be deployed conditionally alongside quick UI iterations to solve post-signup confusion.