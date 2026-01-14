# A-B-Experiment-Audit-Funnel-Conversion-Impact-Analysis-Recommender-System-Test-
Audit an A/B experiment for data quality and validity, then measure funnel conversion impact (product page → cart → purchase) using proportion tests (z-test) and clear go/no-go recommendations.
## Overview
This project evaluates an A/B experiment conducted by an international e-commerce platform to assess the impact of an improved recommendation system on user conversion.

The analysis goes beyond surface-level results and includes a full **experiment audit** to validate data quality and test integrity before measuring funnel performance and statistical significance.

---

## Business Objective
- Verify whether the A/B test was executed correctly  
- Measure conversion impact across the funnel:
  **product_page → product_cart → purchase**
- Determine whether the new recommendation system delivers a meaningful uplift
- Provide a clear, data-driven go / no-go recommendation

---

## Live Dashboard (Tableau Public)
An interactive dashboard was built to support experiment monitoring and stakeholder review:

🔗 **Tableau A/B Test Dashboard**  
https://public.tableau.com/views/PruebaAB-recommender_system_test/Dashboard?:language=en-GB&publish=yes&:display_count=n&:origin=viz_share_link

The dashboard enables:
- Comparison of funnel conversion by group
- Daily event volume monitoring
- High-level visibility into experiment dynamics

---

## Experiment Design
- Test name: `recommender_system_test`
- Groups:  
  - A — Control  
  - B — New checkout funnel with improved recommendations
- Launch date: 2020-12-07  
- New users stopped: 2020-12-21  
- End date: 2021-01-01  
- Audience: 15% of new EU users  
- Expected outcome: ≥10% uplift at each funnel stage within 14 days  
- Planned sample size: 6,000 users  

---

## Data Sources
- `ab_project_marketing_events_us.csv` — marketing calendar  
- `final_ab_new_users_upd_us.csv` — new user registrations  
- `final_ab_events_upd_us.csv` — user event logs  
- `final_ab_participants_upd_us.csv` — experiment assignment  

Core funnel events:
- `product_page`
- `product_cart`
- `purchase`

---

## Analytical Workflow

### Data Preparation
- Convert date and time fields to datetime
- Identify missing values and duplicates
- Validate EU-only scope and experiment dates

### Experiment Audit
- User and event balance across groups
- Detection of cross-group contamination
- Event distribution over time
- Identification of anomalies or confounding factors

### Funnel Analysis
- Build a 14-day post-signup funnel
- Calculate conversion rates at each stage
- Measure relative uplift (B vs A)

### Statistical Testing
- Two-proportion z-tests for each funnel stage
- Clearly defined null and alternative hypotheses
- Alpha selection and interpretation of p-values

---

## Key Outputs
- Experiment validity assessment
- Funnel conversion comparison (A vs B)
- Statistical significance results
- Interactive Tableau dashboard
- Final recommendation on shipping or revising the change

---

## Tools
- Python  
- pandas  
- matplotlib / plotly  
- scipy / statsmodels  
- Jupyter Notebook  
- Tableau Public  

---

## Conclusion
This project demonstrates a rigorous approach to experimentation, ensuring that decisions are based not only on observed metrics but also on verified data quality and statistical evidence. The results provide clear guidance on whether the recommender system improvement should be released or re-evaluated.

---

## Author
**Erika González**  
MBA | Marketing & Data Analytics  
Focus areas: Experimentation, Funnel Analytics, Statistical Testing
