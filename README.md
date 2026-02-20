# Instacart Customer Segmentation & Revenue Optimization

**Python-based behavioral analytics across 32.4M transactions to identify high-value customer segments and optimize marketing allocation for an online grocery platform.**

[![View Report](https://img.shields.io/badge/Excel-Final_Analysis_Report-2B5329?style=flat-square&logo=microsoftexcel&logoColor=white)](reports/05%20Sent%20to%20clients/A4_final_report_Jessica_Duong.xlsx)
[![View Notebooks](https://img.shields.io/badge/Jupyter-Python_Notebooks-6AAB73?style=flat-square&logo=jupyter&logoColor=white)](scripts/03%20Scripts/)
[![View Visualizations](https://img.shields.io/badge/Charts-27_Visualizations-C4A84D?style=flat-square&logo=python&logoColor=white)](visualizations/Visualizations/)

---

## Project Background

Instacart is an online grocery delivery app with strong existing sales but limited visibility into which customer segments drive the most value. The marketing team needed a data-driven segmentation strategy to move from one-size-fits-all campaigns to targeted outreach based on who customers are, what they buy, and when they shop.

This analysis cleaned, merged, and analyzed 32.4 million order-product records across 206,000+ customers and 5 datasets to build a customer segmentation framework identifying high-value personas, revenue concentration patterns, and actionable marketing recommendations.

## Data Structure

Five datasets were merged into a single analytical frame using pandas: orders, products, order-products (the 32.4M transaction-level table), departments, and a customer demographics dataset. Behavioral flags, loyalty tiers, spending tiers, and revenue classifications were derived to enable multi-dimensional customer profiling.

**Datasets merged:** Orders (3.4M) · Products (49,693 across 21 departments) · Order-Products (32.4M records) · Departments · Customer Demographics (206,209 customers)

**Segmentation framework built:**
- **Loyalty tiers:** New (≤10 orders), Regular (11–40), Loyal (>40)
- **Spending tiers:** Low spender (≤$10 avg), High spender (>$10 avg)
- **Revenue tiers:** Tier-1 Core (47.9%), Tier-2 Add-ons (27.6%), Tier-3 Long-tail (24.5%)

## Executive Summary

Revenue is heavily concentrated in a narrow customer profile: **older adult family households buying grocery staples.** This group funds nearly 80% of top-tier revenue, and the product mix is dominated by Produce and Dairy rather than premium items. Meanwhile, high-income customers are significantly undermonetized, and regional differences are essentially flat, meaning marketing can scale nationally without costly customization.

### Top Findings

**1. Adults 56+ generate 79.5% of Tier-1 revenue despite representing 40.5% of customers.**
This demographic is the single most important segment for Instacart's core business. Middle-aged and young adults together account for only about 20% of top-tier revenue, making the 56+ group the clear priority for retention and loyalty investment.

**2. Family households account for 87% of order volume, making them the core revenue engine.**
Families generate roughly 75% of both orders and spending. Single-person households are a small minority of activity. Any marketing strategy that doesn't prioritize family shoppers is misallocating resources.

**3. High-income customers ($120K+) spend the same per order as middle-income customers.**
Despite having significantly more purchasing power, high earners spend only about 1.08% of income on Instacart versus 2.35% for low-income customers. This represents a large untapped upsell opportunity through premium offerings, bulk options, and subscription tiers.

**4. Product mix and revenue efficiency are virtually identical across all four U.S. regions.**
Produce holds ~30% of revenue share in every region, with all other departments within 1 percentage point of each other. Regional customization adds cost without meaningful lift. National campaigns perform just as well.

## Insights Deep Dive

### Revenue Concentration

Instacart's revenue is structurally dependent on older adult households. The 56+ age group funds nearly 80% of Tier-1 revenue, while middle-aged and young adults contribute roughly 11% and 10% respectively. This concentration means retention of the 56+ segment is critical, and any churn in this group would disproportionately impact the business.

![Tier-1 Revenue by Age Group](visualizations/Visualizations/instacart-findings.jpg)

### Spending Gap

High-income customers represent a significant growth opportunity. Despite earning $120K+, their mean order value is comparable to middle-income shoppers across all regions. The scatter plot below shows spending is flat regardless of income level, suggesting Instacart hasn't given high earners a compelling reason to spend more. Bulk options, premium assortments, and subscription models could unlock this segment.

![Income vs Spending by Region](visualizations/Visualizations/instacart-constraints.jpg)

### Regional Consistency

The product mix heatmap reveals virtually no regional differentiation in purchasing behavior. Every region allocates roughly the same share of revenue to the same departments in the same order. This is a strategic advantage: Instacart can run centralized national campaigns without sacrificing performance, avoiding the cost and complexity of regional customization.

![Regional Department Mix](visualizations/Visualizations/instacart-deliverables.jpg)

## Recommendations

**Protect the Core Revenue Engine**
Prioritize family households and 56+ adults with loyalty programs, subscription discounts, and recurring order reminders. Produce and Dairy drive over 70% of Tier-1 revenue, so position Instacart as a staples-first platform rather than a premium or specialty service.

**Activate High-Income Customers**
Launch bulk and premium product offerings targeting the $120K+ segment. Their spending is flat relative to income, creating room for upsell through curated premium bundles, wholesale-style options, and higher-tier subscription plans.

**Simplify Marketing with National Campaigns**
Revenue efficiency is flat (~1.0x) across all regions and product mix is nearly identical. Skip regional customization and run centralized campaigns, reallocating the saved budget to low-utilization time windows (12am–6am Tue–Wed) to capture incremental demand.

**Build a Tier-2 Add-On Strategy**
Tier-2 add-on products (snacks, beverages, bakery, prepared meals) represent 27.6% of revenue with room to grow. Deploy dynamic cross-sell recommendations at checkout and persona-specific bundles to increase average order value.

## Tools & Skills

| Tool | Use |
|------|-----|
| Python (pandas, NumPy) | Data cleaning, merging, segmentation framework, behavioral flagging |
| matplotlib, seaborn | 27 visualizations for stakeholder reporting |
| Jupyter Notebook | Analysis pipeline across 14 notebooks |
| Excel | Final report delivery to stakeholders |

**Analytical techniques demonstrated:** Large-scale data wrangling (32M+ rows) · Multi-dimensional customer segmentation · Revenue concentration analysis · Behavioral flagging and derived variables · Customer persona development · Regional efficiency benchmarking

## Deliverables

| Document | Description |
|----------|-------------|
| [Final Analysis Report](reports/05%20Sent%20to%20clients/) | Complete findings with 15 business questions answered and strategic recommendations |
| [Python Notebooks](scripts/03%20Scripts/) | 14 Jupyter notebooks covering the full analysis pipeline |
| [Visualizations](visualizations/Visualizations/) | 27 charts analyzing ordering patterns, demographics, and revenue distribution |

## Author

**Jessica Duong**

Data Analyst | [LinkedIn](https://www.linkedin.com/in/jess-duong/) | [Portfolio](https://jess-duong.github.io/) | duong.t.jess@gmail.com

---

*Data source: "The Instacart Online Grocery Shopping Dataset 2017", accessed via [Kaggle](https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis). Customer demographics are synthetic data provided for educational purposes.*

## Acknowledgments
AI tools were used to support portions of this project, including documentation and presentation. All analysis, interpretation, and recommendations are my own.
