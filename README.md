# Part 2: KPI Framework, Business Experiment Analysis & Decision Recommendation

## 📊 Task 1: Business Problem Statement

### 1. What Decision Needs to Be Made?
The leadership team needs to decide whether to permanently roll out and launch the new onboarding and activation campaign experience (Treatment group) to 100% of the user base, or retain the existing onboarding experience (Control group).

### 2. Who the Decision Impacts?
This decision directly impacts:
* **New Users:** Their first-time experience, onboarding journey, and initial friction with the product change completely.
* **Product & Marketing Teams:** Defines the future baseline for user acquisition journeys and multi-channel campaign strategies.
* **Customer Support Team:** Changes in customer onboarding flows can directly increase or decrease the volume of support tickets.
* **Company Leadership/Stakeholders:** Direct impact on corporate revenue, user growth metrics, and customer lifetime value (LTV).

### 3. What Metric Should Improve?
The primary goal is to maximize the **Paid Conversion Rate** (Users converted to paid / total users), which serves as our North Star Metric. Supporting metrics like *Trial Start Rate*, *Onboarding Completion Rate*, and *Average Engagement Score* are also expected to see a statistically significant upward trend.

### 4. What Risks Must Be Monitored?
While optimizing for conversion, we must closely observe our **Guardrail Metrics** to ensure long-term business health is not compromised:
* **Refund Rate:** A pushy onboarding flow might increase instant sign-ups but lead to high post-conversion refunds.
* **Support Ticket Rate:** Confusing or broken steps in the new campaign could frustrate users and spike support volumes.
* **Average Days to Convert:** If the campaign unnecessarily lengthens the decision cycle, it delays cash flows.
* **Segment-Level Decline:** The campaign might work globally but severely damage performance in specific regions or on particular device types.

### 5. What Evidence is Required Before Making a Recommendation?
A definitive recommendation to launch requires a three-layered validation approach:
1. **Statistical Significance:** A rigorous hypothesis test (A/B testing analysis) confirming that the improvement in the Paid Conversion Rate is statistically significant ($p\text{-value} < 0.05$) and not a result of random chance.
2. **Guardrail Stability:** Empiric data showing that guardrail metrics (Refunds, Tickets) remain stable, or change within acceptable operational thresholds.
3. **Segment Consistency:** Analysis confirming that the treatment does not cause severe negative deviations in key demographic or technical segments (e.g., specific regions or device types).
---

## 📈 Task 2: Define the North Star Metric

### 1. Selected North Star Metric
* **Metric Name:** Paid Conversion Rate (%)
* **Formula:** `(Total Users Converted to Paid / Total Users in Group) * 100`

### 2. Business Justification
* **Main Success Metric:** As a subscription-based digital product company, real business growth and revenue sustainability directly depend on turning free or trial users into paying customers. Paid Conversion Rate is the ultimate indicator of whether the onboarding journey successfully demonstrates the product's premium value.
* **Why Supporting Metrics are not North Star:** Metrics like *Trial Start Rate* or *Onboarding Completion Rate* are useful operational signposts, but they are top/mid-funnel metrics. A user can complete onboarding or start a trial but drop out before paying. Optimizing solely for those would mask the true bottom-line performance.
* **Connection to Business Growth:** Higher conversion directly drives Monthly Recurring Revenue (MRR), lowers Customer Acquisition Cost (CAC) payback periods, and increases Customer Lifetime Value (LTV).
* **Risk of Blind Optimization:** If we blindly optimize for Paid Conversion Rate, the campaign might use aggressive, misleading, or hyper-pushy conversion tactics. This would artificially inflate sales short-term but cause a massive spike in subsequent customer refunds and support complaints.

---

## 🌳 Task 3: KPI Tree & Metric Drivers

### 1. Primary KPI Drivers (Level 1)
To successfully impact the North Star Metric, the onboarding campaign must drive three primary levers:
* **L1 Driver 1: Trial Start Rate (%)** – Measures initial user intent and interest in exploring premium features.
* **L1 Driver 2: Onboarding Completion Rate (%)** – Measures active activation and product setup success, reducing initial product friction.
* **L1 Driver 3: Average Engagement Score** – Measures user interaction depth and early habit formation within the app during the critical first week.

### 2. Sub-Drivers (Level 2)
Each primary driver breaks down into granular sub-drivers:
* **Under Trial Start Rate:**
  * *Landing Page Visit Rate (%):* Users who successfully land on the experience.
  * *Sign-up Click Rate (%):* Percentage of visitors clicking the call-to-action (CTA).
* **Under Onboarding Completion Rate:**
  * *Profile Setup Rate (%):* Users completing the vital identity setup step.
  * *Tutorial Video Watch Rate (%):* Users interacting with educational onboarding assets.
* **Under Average Engagement Score:**
  * *Daily Active Days (First Week):* Average number of days a user returns in week 1.
  * *Feature Adoption Rate (%):* Volume of key platform features utilized by the user.

### 3. Guardrail Metrics
To ensure operational stability and revenue quality, the following three metrics are actively monitored:
* **Refund Rate (%):** To track if the campaign causes buyer's remorse or accidental sign-ups.
* **Support Ticket Rate (%):** To ensure the new onboarding flow is seamless and doesn't trigger customer confusion.
* **Average Days to Convert:** To monitor if the design delays user purchase decision cycles.

### 4. Visual KPI Tree Preview
*(The visual diagram mapped to this logic is maintained inside the repository folders as required)*.
* **File Path:** `outputs/kpi_tree.png`
* **Screenshot Path:** `screenshots/kpi_tree_preview.png`
