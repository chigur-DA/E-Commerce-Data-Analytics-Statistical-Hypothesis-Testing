# E-Commerce-Data-Analytics-Statistical-Hypothesis-Testing
# 🛒 End-to-End E-Commerce Data Analytics & Statistical Hypothesis Testing

![Python](https://img.shields.io/badge/Python-3873A3?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-Google%20BigQuery-412991?style=for-the-badge&logo=googlecloud&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![Statsmodels](https://img.shields.io/badge/Statsmodels-00599C?style=for-the-badge&logo=python&logoColor=white)

##  Executive Summary
This project presents an **end-to-end data analytics solution** examining e-commerce user sessions, purchase behaviors, marketing performance, and statistical relationships[cite: 1]. The dataset covers **349,545 unique web sessions** spanning from **November 1, 2020, to January 31, 2021**[cite: 1].

The main goal of this analysis is to identify key revenue drivers, evaluate user segmentation (registered vs. guest users), assess device/channel effectiveness, and rigorously test statistical hypotheses to optimize marketing budgets and improve conversion rates[cite: 1].


##  Interactive Visualization
**[View Full Interactive Tableau Dashboard](https://public.tableau.com/app/profile/.17026898/viz/_17837689433070/Dashboard1?publish=yes)**[cite: 1]


## Tech Stack & Methodology
* **Data Extraction & Transformation:** Google BigQuery SQL (joining multiple transactional and session tables via `LEFT JOIN`)[cite: 1].
* **Data Wrangling & Processing:** Python (`pandas`, `numpy`)[cite: 1].
* **Exploratory Data Analysis (EDA) & Visualization:** `matplotlib`, `seaborn`[cite: 1].
* **Statistical Testing:** `scipy.stats` (Pearson correlation, Shapiro-Wilk, Mann-Whitney U, Kruskal-Wallis, Chi-Square, Paired T-Test) & `statsmodels` (Two-sample Z-test)[cite: 1].
* **Business Intelligence:** Tableau Public[cite: 1].
##  Detailed Data Insights & EDA Findings

### 1. Conversion & Funnel Overview
* **Low Baseline Conversion:** Out of 349,545 total sessions, **only 33,538 (~9.6%) resulted in a successful purchase**[cite: 1]. Over 90.4% of sessions were non-converting visits[cite: 1].
* **User Authentication Breakdown:** Over **92% of all sessions** were performed by guest (unauthenticated) users[cite: 1]. Guest users generate **91.91% of total daily sales**, whereas registered account holders generate only **8.09%**[cite: 1].

### 2. Geographic & Product Performance
* **Top Continents by Revenue:** Americas > Asia > Europe[cite: 1].
* **Top 5 Countries:** United States, India, Canada, United Kingdom, France[cite: 1].
* **Top Product Categories (Global & US):** 
  1. *Apparel* ($837,212)[cite: 1]
  2. *Office Supplies* ($381,208)[cite: 1]
  3. *Drinkware* ($272,333)[cite: 1]
* **Big-Ticket Items (Dashboard Data):** Categories like *Sofas & Armchairs* (> $8M revenue), *Chairs*, and *Beds* drive significant overall GMV due to higher average order values (AOV)[cite: 1].

### 3. Channels & Devices Analysis
* **Device Share:** Desktop dominates sales volume (**59%**), followed by Mobile (**38.7%**) and Tablet (**2.3%**)[cite: 1].
* **Traffic Channels:** **Organic Search** (~37%) and **Paid Search** (~26%) generate the bulk of user acquisitions and sales revenue[cite: 1]. **Social Search** underperforms significantly compared to other acquisition channels[cite: 1].

## Statistical Hypothesis Testing & Rigorous Analysis

| Research Question / Hypothesis | Statistical Test Used | Key Test Metric | P-Value | Statistical Conclusion & Business Interpretation |
| :--- | :--- | :--- | :--- | :--- |
| **Relationship between Daily Traffic and Sales** | Pearson Correlation | $r = 0.9300$ | $p < 0.001$ | **Statistically Significant.** Strong linear relationship showing that traffic volume directly translates into daily revenue[cite: 1]. |
| **Revenue Difference: Registered vs. Guest Users** | Mann-Whitney U Test | $U = \text{stat}$ | $p < 0.001$ | **Statistically Significant.** Unregistered/guest users generate significantly higher total daily revenue volumes compared to registered users[cite: 1]. |
| **Session Differences Across Traffic Channels** | Kruskal-Wallis Test | $H = \text{stat}$ | $p < 0.001$ | **Statistically Significant.** Session distribution across channels is non-uniform; Organic Search leads by a wide margin[cite: 1]. |
| **Device Type vs. Purchase Conversion Probability** | Chi-Square ($\chi^2$) Contingency Test | $\chi^2 = \text{stat}$ | $p = 0.3800$ ($p > 0.05$) | **Not Significant.** Device type (Desktop vs. Mobile vs. Tablet) has no statistically significant influence on whether a user completes a purchase[cite: 1]. |
| **Organic Traffic Share: Americas vs. Europe** | Two-Sample Z-Test for Proportions | $Z = \text{stat}$ | $p = 0.9200$ ($p > 0.05$) | **Not Significant.** The proportion of organic sessions in Americas (35.61%) and Europe (35.55%) shows no meaningful statistical difference[cite: 1]. |
| **Sales Patterns Across Weekdays (Mon vs. Tue)** | Paired T-Test | $t = \text{stat}$ | $p < 0.05$ | **Statistically Significant.** Tuesdays consistently demonstrate higher sales revenue than Mondays, indicating weekly purchasing cycles[cite: 1]. |


##  Strategic Business Recommendations

1. **Optimize Guest-to-Member Retention Funnel:**
   * Since **91.91% of revenue comes from non-registered users**, the business is heavily reliant on one-off purchases[cite: 1]. Implementing a post-purchase guest checkout incentive (e.g., 10% off the next order upon email registration) can increase customer lifetime value (LTV).

2. **Mobile UX & Cross-Device Optimization:**
   * While Desktop accounts for **59% of revenue**, the Chi-Square test confirms that mobile users convert at similar rates[cite: 1]. Enhancing mobile checkout flow and introducing mobile-exclusive promotions can boost Mobile AOV.

3. **Reallocate Marketing Budget:**
   * **Organic and Paid Search** demonstrate a strong synergistic relationship and drive the highest revenue[cite: 1]. Budget should be shifted away from underperforming **Social Search** toward scaling SEO and high-intent Paid Search campaigns[cite: 1].

4. **Capitalize on Day-of-Week Seasonality:**
   * Higher Tuesday revenue indicates strong mid-week intent[cite: 1]. Promotional email blasts and retargeting ads should be scheduled for late Monday or early Tuesday to maximize conversion rates[cite: 1].
