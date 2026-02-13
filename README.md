# Instacart Basket Analysis

**Python-based customer segmentation and purchasing behavior analysis to inform targeted marketing strategies for an online grocery delivery platform.**

[![View Report](https://img.shields.io/badge/View-Analysis_Report-blue)](reports/05%20Sent%20to%20clients/)
[![View Code](https://img.shields.io/badge/View-Python_Notebooks-green)](scripts/03%20Scripts/)

## Project Overview

Instacart, an online grocery delivery platform with strong existing sales, needed to understand customer purchasing patterns to optimize marketing campaigns. This Python analysis examined 32.4 million order-product records across 206,000+ customers to identify high-value segments, peak ordering times, and product category performance.

### Business Questions
- When do customers place orders and what products do they buy?
- Who are Instacart's most valuable customer segments?
- What product categories drive revenue vs represent growth opportunities?
- How should marketing resources be allocated across demographics and regions?

### Key Findings
- **Older adults (56+) generate 80% of Tier-1 revenue** despite representing 40.5% of customers
- **Family households account for 87% of core revenue**: 75% of order volume and spending
- **Produce and Dairy dominate**: 72% of Tier-1 revenue from grocery staples, not premium products
- **High-income customers are undermonetized**: Spending only 1.08% of income vs 2.35% for low-income
- **Regional efficiency is flat (~1.0x)**: Revenue patterns consistent nationwide; skip regional customization

## Tools & Techniques

**Tools**: Python (pandas, NumPy, matplotlib, seaborn), Jupyter Notebook  
**Skills**: Data wrangling, customer segmentation, exploratory data analysis, data visualization, business intelligence

### Analytical Approach
- Cleaned and merged 5 datasets totaling 32.4M records using pandas
- Created customer segmentation framework: Loyalty tiers, spending tiers, order frequency groups
- Derived behavioral flags and categorical variables for profiling
- Built revenue concentration analysis (Tier-1/2/3 product categorization)
- Developed customer personas combining demographics with purchasing patterns
- Created 27 visualizations using matplotlib and seaborn for stakeholder presentation

## Repository Contents
```
├── scripts/03 Scripts/         # 14 Jupyter notebooks (data cleaning, merging, analysis, visualization)
├── visualizations/             # 27 charts covering ordering patterns, demographics, revenue analysis
├── reports/05 Sent to clients/ # Final analysis report with findings and recommendations
├── project-management/         # Project brief and data documentation
└── README.md                   # Project documentation
```

## Strategic Recommendations

### Protect Core Revenue Engine
- **Focus on family households**: 87% of Tier-1 revenue comes from families; launch family savings programs with subscription discounts, bulk bundles, and recurring order reminders
- **Position as staples-first platform**: Produce and Dairy generate >70% of core revenue; emphasize everyday essentials over premium positioning

### Optimize Marketing Efficiency
- **Deploy national campaigns**: Revenue efficiency flat across regions (~1.0x); skip expensive regional customization
- **Target low-utilization windows**: Shift ad spend to 12am-6am Tue-Wed with automated campaigns to capture incremental demand
- **Monetize high-efficiency personas**: Prioritize health-focused families (1.20x efficiency) and stock-up shoppers over snack-only customers

### Unlock Growth Opportunities
- **Build Tier-2 add-on strategy**: Target snacks, beverages, bakery, prepared meals (27.6% of revenue) with persona-specific bundles at checkout
- **Expand bulk offerings**: Bulk department severely underperforming (33,451 orders); capture high-income customers currently shopping Costco/Sam's Club
- **Activate high-income segment**: High earners spend same absolute amount as middle-income (~$1,600) but only 1.08% of income vs 2.35% for low-income; untapped potential for premium subscription tiers

## Data Scope & Methodology

**Dataset**: (https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis) (Kaggle)  
**Size**: 32.4M order-product records, 206,209 customers, 3.4M orders  
**Time Period**: Historical transaction data (2017)  
**Product Coverage**: 49,693 products across 21 departments

### Customer Segmentation Framework
- **Loyalty Tiers**: New (≤10 orders), Regular (11-40), Loyal (>40)
- **Spending Tiers**: Low spender (≤$10 avg/order), High spender (>$10 avg/order)
- **Order Frequency**: Frequent, Regular, Non-frequent based on median days between orders
- **Revenue Tiers**: Tier-1 (Core 47.9%), Tier-2 (Add-ons 27.6%), Tier-3 (Long-tail 24.5%)

### Analytical Findings
- **Peak ordering**: Saturday/Sunday 10am-4pm; lowest Tuesday/Wednesday 2am-6am
- **Demographic concentration**: Middle-income (48.3%), older adults (40.5%), family households (dominant)
- **Geographic patterns**: South leads (33.3%), West (25.6%), Midwest (23.5%), Northeast (17.6%)
- **Product mix**: Consistent nationwide; no regional preference differentiation

### Data Limitations
- **2017 dataset**: Purchasing patterns may have evolved with pandemic and delivery market maturation
- **Customer demographics synthetic**: CareerFoundry educational dataset appended to actual Instacart orders
- **Missing temporal trends**: Snapshot analysis without year-over-year growth metrics
- **No promotional data**: Unable to assess impact of discounts or marketing campaigns on behavior

## Analysis Highlights

### Order Patterns
- Clear weekday vs weekend divide; families shop Saturday/Sunday
- Daytime ordering dominates (10am-4pm); overnight extremely low
- Average order value consistent across time periods (~$10)

### Customer Profiling
- **High-frequency family personas**: ~75% of orders and revenue
- **Health-focused families**: Highest revenue efficiency at 1.20x
- **Stock-up families**: Strong efficiency with bulk purchasing behavior
- **Snack-focused personas**: Lower efficiency; deprioritize in targeting

### Revenue Concentration
- **Grocery staples dominate**: Produce + Dairy = 72% of Tier-1 revenue
- **Add-on categories underperforming**: Snacks, beverages, bakery represent growth opportunity
- **Bulk severely underpenetrated**: Only 33,451 orders vs millions in core departments

## Documentation

- **[Python Analysis Notebooks](scripts/03%20Scripts/)**: 14 Jupyter notebooks covering data wrangling, merging, segmentation, and visualization
- **[Visualizations](visualizations/Visualizations/)**: 27 charts analyzing ordering patterns, demographics, revenue distribution, and customer personas
- **[Final Report](reports/05%20Sent%20to%20clients/)**: Complete findings with strategic recommendations and supporting analysis
- **[Project Brief](project-management/)**: Original business requirements and analytical scope

## Project Context

This project was completed as part of CareerFoundry's Data Analytics program, demonstrating proficiency in:
- Large-scale data manipulation with pandas (32M+ records)
- Customer segmentation and behavioral analysis
- Revenue concentration and product mix analysis
- Data visualization and storytelling with matplotlib/seaborn
- Translating analytical insights into actionable marketing strategy

### Technical Approach
- **Data Pipeline**: Import → Clean → Merge → Derive → Aggregate → Visualize
- **Segmentation Logic**: Multi-dimensional framework combining demographics and behavior
- **Visualization Strategy**: 27 charts designed for non-technical stakeholder presentation
- **Code Organization**: Modular notebooks organized by analytical phase

### Development Notes
Python code development supported by Stack Overflow community solutions and AI-assisted debugging. Visualization narrative structure optimized with AI assistance to enhance stakeholder communication. All data analysis methodology, strategic insights, and business recommendations represent original analytical work.

## Future Analysis Opportunities

### Recommended Enhancements
- **Predictive churn modeling**: Identify at-risk customers before they lapse
- **Market basket analysis**: Build product recommendation engine using association rules
- **Lifetime value forecasting**: Predict customer LTV at acquisition for targeting optimization
- **A/B testing framework**: Design experiments to validate add-on bundling strategies
- **Real-time segmentation**: Deploy dynamic persona assignment for personalized marketing

## Author

**Jess Duong**  
Data Analyst | [LinkedIn](https://www.linkedin.com/in/jess-duong/) | [Portfolio](https://jess-duong.github.io/)| duong.t.jess@gmail.com

---

**Data Citation**: "The Instacart Online Grocery Shopping Dataset 2017", Accessed from (https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis) via Kaggle on December 2025.

*Note: Instacart is a real company and the data used in this project is publicly available. Customer demographics are synthetic data provided by CareerFoundry for educational purposes.*

*For questions about methodology or to discuss this analysis, please reach out via [LinkedIn](https://linkedin.com/in/jessica-duong-35690847/) or open an issue in this repository.*

## Acknowledgments
AI tools were used to support portions of this project, including documentation and presentation. All analysis, interpretation, and recommendations are my own.
