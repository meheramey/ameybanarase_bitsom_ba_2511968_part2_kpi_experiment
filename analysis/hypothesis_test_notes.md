# Task 6: Hypothesis Testing Notes

This document establishes the statistical framework used to evaluate the onboarding and activation experiment. The goal is to determine whether the changes observed in the treatment group are mathematically significant or just a result of random chance, directly guiding our product rollout decision.

---

## 1. Experiment Parameter Setup

* **Metric Being Tested:** Paid Conversion Rate (The proportion of unique signed-up users who convert to a paid subscription plan within 30 days).
* **Significance Level ($\alpha$):** 0.05 (95% Confidence Level). This is the standard threshold in product analytics to control Type I error (the risk of falsely claiming a feature is successful).
* **Test Type:** One-tailed Z-Test for Two Independent Proportions.
  * *Why One-tailed?* Because the new onboarding flow was engineered explicitly to reduce friction and improve activation. We are testing for directional improvement (Treatment > Control), not just any arbitrary change.

---

## 2. Hypothesis Formulation

* **Null Hypothesis ($H_0$):** $p_{\text{treatment}} \le p_{\text{control}}$
  The new onboarding and activation campaign has no positive effect on the Paid Conversion Rate. The conversion rate of the Treatment group is less than or equal to the Control group.
  
* **Alternative Hypothesis ($H_1$):** $p_{\text{treatment}} > p_{\text{control}}$
  The new onboarding and activation campaign significantly increases the Paid Conversion Rate compared to the existing experience.

---

## 3. Reason for Choosing Paid Conversion Rate

While the experiment tracks multiple funnel steps (landing page visits, trial starts, and onboarding completions), the **Paid Conversion Rate** was chosen as the primary testing metric because:
1. **Direct Alignment with Business Growth:** Early-funnel metrics like landing page clicks can spike due to curiosity, but paid conversion represents real user validation and financial sustainability.
2. **Mitigation of Feature Friction:** The core business problem stated that users were dropping off after signup. This metric tells us if the new onboarding experience successfully built enough product value to push users past the paywall.

---

## 4. Interpretation Logic & Business Decision Connection

To make a final product decision, we apply the following mathematical criteria:

1. **If $p\text{-value} < \alpha$ (0.05) and $Z_{\text{stat}} > 1.645$ (Critical Z-Value):**
   * **Logic:** We reject the Null Hypothesis ($H_0$). The lift is statistically sound.
   * **Business Decision:** Roll out the new onboarding flow to 100% of traffic, provided guardrail metrics (like support tickets or refunds) are within manageable operational limits.

2. **If $p\text{-value} \ge \alpha$ (0.05) or $Z_{\text{stat}} \le 1.645$:**
   * **Logic:** We fail to reject the Null Hypothesis ($H_0$). The observed difference could be a random fluke.
   * **Business Decision:** Do not roll out the campaign. Retain the Control flow and iterate on the onboarding product strategy.

---

## 📊 Experimental Statistical Output

After structural deduplication and cleaning, the final data inputs generated the following outputs:
* **Control Group:** $N = 690$, Converted = 22, $p_1 = 3.19\%$
* **Treatment Group:** $N = 710$, Converted = 50, $p_2 = 7.04\%$
* **Calculated Z-Statistic:** 3.235
* **Calculated p-Value:** 0.0006

**Final Statistical Conclusion:** Since the $p\text{-value}$ (0.0006) is far below our significance level ($\alpha = 0.05$), we **Reject the Null Hypothesis ($H_0$)**. The absolute lift of 3.85% in conversion is highly significant, confirming that the new onboarding sequence structurally drives user monetization.