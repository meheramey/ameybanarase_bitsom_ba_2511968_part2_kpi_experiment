# Statistical Validation & Hypothesis Testing

## 1. Experimental Setup
* **Methodology:** One-tailed Two-Sample Z-Test for Proportions.
* **Confidence Level:** 95% ($\alpha = 0.05$)

## 2. Hypotheses Definitions
* **Null Hypothesis ($H_0$):** $P_{\text{treatment}} \le P_{\text{control}}$
  * *Interpretation:* The new onboarding and activation campaign does not improve the conversion rate, or it performs worse than the existing experience. Any observed increase is purely due to random sampling variation.
* **Alternative Hypothesis ($H_1$):** $P_{\text{treatment}} > P_{\text{control}}$
  * *Interpretation:* The new onboarding campaign significantly improves the paid conversion rate compared to the existing control setup.

---

## 3. Statistical Calculations & Core Metrics

Using the captured data points from the experiment sheet, we establish the following variables:

$$N_{\text{control}} = 693, \quad X_{\text{control}} = 22 \implies P_{\text{control}} = 3.17\%$$
$$N_{\text{treatment}} = 715, \quad X_{\text{treatment}} = 50 \implies P_{\text{treatment}} = 6.99\%$$

### Calculated Statistical Outputs:
* **Pooled Proportion ($p_c$):** $0.0511$
* **Standard Error ($SE$):** $0.0118$
* **Calculated Z-Score:** $3.24$
* **Resulting P-Value:** $0.0006$

---

## 4. Statistical Decision & Operational Interpretation

### Decision:
Since the calculated **P-Value ($0.0006$)** is significantly lower than the established significance threshold **$\alpha (0.05)$**, we strictly **Reject the Null Hypothesis ($H_0$)**.

### Operational Justification:
The difference between the Control conversion rate ($3.17\%$) and the Treatment conversion rate ($6.99\%$) is highly statistically significant. The probability that this massive lift happened by random chance is less than $0.06\%$. Therefore, we can state with high statistical confidence that the new onboarding and activation campaign is inherently more effective at driving user monetization.

---

## 5. Guardrail Metric Conflict Analysis
While the primary metric (Paid Conversion Rate) is a clear success, the guardrail metrics reveal a strong operational bottleneck:
1. **Support Ticket Volume:** Spiked from **14.72%** to **24.76%** under the treatment group.
2. **Segment Distress:** Pivot analysis confirms this operational friction is heavily concentrated among **Mobile Users**, where support queries reached critical thresholds. 

Therefore, despite statistical validation, a blind global launch poses severe customer satisfaction and infrastructure risks.