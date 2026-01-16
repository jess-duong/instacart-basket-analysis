# Instacart Grocery Basket Analysis

## Project Overview

Instacart is an online grocery delivery platform with strong existing sales. This project performs an exploratory analysis of customer purchasing behavior to uncover patterns and support targeted marketing strategies. The analysis identifies high-value customer segments, peak ordering times, and product category performance to inform data-driven marketing campaigns.

## Key Questions Answered

1. **When do customers shop?**
   - Peak days: Saturday and Sunday; lowest: Tuesday and Wednesday
   - Peak hours: 10am - 4pm; lowest: 2am - 6am

2. **Who are Instacart's customers?**
   - Older adults (56+) represent 40.5% of customers
   - Middle-income households dominate at 48.3%
   - Family households generate 87% of Tier-1 revenue

3. **What products drive revenue?**
   - Produce and Dairy Eggs account for 72% of Tier-1 revenue
   - Platform is driven by low-to-mid priced grocery staples, not premium products
   - Bulk department is significantly underperforming (only 33,451 orders)

4. **Where does revenue come from geographically?**
   - South region leads (33.3%), followed by West (25.6%) and Midwest (23.5%)
   - Revenue efficiency is flat across all regions (~1.0x)
   - Product mix is consistent nationwide

5. **Who are the most valuable customers?**
   - High-frequency family-based personas generate ~75% of order volume and revenue
   - Health-focused and stock-up family personas have highest revenue efficiency (1.20x)
   - High-income customers ($120k+) spend the same as middle-income (~$1,600) - untapped potential

## Data

- **Source:** [Instacart Online Grocery Shopping Dataset 2017](https://www.instacart.com/datasets/grocery-shopping-2017) via Kaggle
- **Additional Data:** CareerFoundry customer dataset
- **Size:** 32.4 million order-product records across 206,000+ customers

### Datasets Used
| Dataset | Records | Description |
|---------|---------|-------------|
| orders | 3.4M | Order timestamps and customer IDs |
| orders_products_prior | 32.4M | Products in each order |
| products | 49,693 | Product names and departments |
| customers | 206,209 | Customer demographics |
| departments | 21 | Department categories |

## Key Insights

### Customer Segmentation
- **Loyalty Tiers:** New (≤10 orders), Regular (11-40), Loyal (>40)
- **Spending Tiers:** Low spender (≤$10 avg), High spender (>$10 avg)
- **Order Frequency:** Frequent, Regular, Non-frequent based on median days between orders

### Revenue Concentration
- **Tier-1 (Core Revenue):** 47.9% - driven by grocery staples
- **Tier-2 (Growth Opportunity):** 27.6% - add-on purchases like snacks, beverages, bakery
- **Tier-3 (Long-Tail):** 24.5% - niche categories

### Demographic Findings
- Older adult households account for nearly 80% of Tier-1 revenue
- High-income customers spend only 1.08% of income on Instacart vs 2.35% for low-income
- Family households generate 75% of both order frequency and revenue

## Recommendations

1. **Shift ad spend to low-utilization windows** - Deploy automated campaigns between 12am-6am on Tue-Wed to capture incremental demand

2. **Reposition as a staple-first platform** - Produce and Dairy Eggs generate >70% of Tier-1 revenue; focus marketing on everyday essentials

3. **Focus growth on Tier-2 Add-On monetization** - Build persona-specific add-on bundles (snacks, beverages, bakery, prepared meals)

4. **Trigger dynamic "Add to Basket" recommendations** - Target high-value family personas at checkout

5. **Protect family household revenue engine** - Launch family savings programs: subscription discounts, bulk grocery bundles, recurring reorder reminders

6. **Deploy national campaigns** - Revenue efficiency is flat across regions; skip regional customization

7. **Monetize high-efficiency personas** - Prioritize health-focused families and stock-up shoppers over snack-only personas

8. **Expand bulk/wholesale offerings** - Capture high-income customers currently shopping at Costco/Sam's Club; Bulk department has only 33,451 orders

## Tools & Skills

### Python Libraries
- pandas - Data manipulation and analysis
- NumPy - Numerical operations
- matplotlib - Data visualization
- seaborn - Statistical visualizations

### Skills Demonstrated
- Data wrangling and cleaning
- Merging and concatenating large datasets
- Deriving new variables (flags, categories, aggregations)
- Exploratory data analysis (EDA)
- Customer segmentation and profiling
- Data visualization and storytelling

## Project Files

### Scripts (`scripts/03 Scripts/`)

| File | Description |
|------|-------------|
| `4.2 Importing libraries and Python data types.ipynb` | Library imports and data type fundamentals |
| `4.3 Intro to Pandas.ipynb` | DataFrame operations and pandas basics |
| `4.4 Data Wrangling & Subsetting.ipynb` | Data cleaning and filtering techniques |
| `4.5 Data Consistency Checks.ipynb` | Missing values, duplicates, and data validation |
| `4.6a Combing & Exporting Data.ipynb` | Merging datasets and exporting results |
| `4.6b Task for ords_prods_merge.ipynb` | Orders and products merge operations |
| `4.7 Deriving New Variables.ipynb` | Creating flags, categories, and calculated fields |
| `4.8 Grouping Data & Aggregating Variables.ipynb` | GroupBy operations and aggregations |
| `4.8 Practice Notebook_Grouping Data & Aggregating Variables.ipynb` | Additional grouping practice exercises |
| `4.9 _Part 1_Intro to Data Visualization with Python.ipynb` | Matplotlib and seaborn fundamentals |
| `4.9_Part 2_Introduction to Visualization with Python.ipynb` | Advanced visualization techniques |
| `4.10 IC_Customer Profiling_Part 1.ipynb` | Customer segmentation and profiling analysis |
| `4.10_A4_Additional Charts for Income Comparison.ipynb` | Income-based customer analysis |
| `4.10_A4_Charts_Only.ipynb` | Final visualization outputs |

- ### Visualizations (`visualizations/Visualizations/`)

The analysis includes 27 visualizations covering:
- Order patterns by day and hour
- Customer demographics (age, income, family status)
- Department revenue concentration
- Regional performance comparison
- Customer persona profiling
- Loyalty segment analysis

| File | Description |
|------|-------------|
| `F1_bar_orders_days_of_week.png` | Order volume by day of week |
| `F2_hist_orders_hour_of_day.png` | Order distribution by hour |
| `F3_line_avg_spending_by_hour.png` | Average spending patterns by hour |
| `F4_line_avg_spending_by_day.png` | Average spending patterns by day |
| `F5_scatter_age_vs_income.png` | Age and income correlation |
| `F6_line_avg_dependents_by_age_group.png` | Household size by age group |
| `F7_bar_loyalty_distribution.png` | Customer loyalty tier distribution |
| `F8_scatter_prices_outliers.png` | Price distribution and outlier detection |
| `F9_chart_05_department_dominance.png` | Department order volume comparison |
| `F10_chart_01_revenue_concentration.png` | Revenue concentration by tier |
| `F11_chart_06_addon_pareto.png` | Add-on purchase Pareto analysis |
| `F12_chart_07_core_vs_addon.png` | Core vs add-on revenue comparison |
| `F13_chart_02_tier1_demographics.png` | Tier-1 customer demographics |
| `F14_chart_03_family_vs_single.png` | Family vs single household comparison |
| `F15_chart_04_income_split.png` | Revenue by income segment |
| `F16_chart_12_regional_concentration.png` | Regional revenue distribution |
| `F17_chart_13_regional_department_mix.png` | Department preferences by region |
| `F18_chart_14_regional_efficiency.png` | Revenue efficiency by region |
| `F19_chart_08_profile_frequency.png` | Order frequency by customer profile |
| `F20_chart_09_profile_revenue.png` | Revenue by customer profile |
| `F21_chart_10_dumbbell_family_single.png` | Family vs single spending comparison |
| `F22_chart_11_revenue_efficiency_persona.png` | Revenue efficiency by persona |
| `NEW_F2.4_Income_vs_spending_by_region.png` | Income vs spending regional analysis |
| `NEW_F2.5_Age_vs_income.png` | Age and income relationship |
| `NEW_F3.3_dept_by_region_all.png` | Department breakdown by region |
| `NEW_F7.5_top5_depts_loyal_regular.png` | Top departments for loyal customers |
| `NEW_F7.6_bottom5_depts_loyal_regular.png` | Bottom departments for loyal customers |
| `chart_02_tier1_demographics.png` | Tier-1 demographic breakdown |

### Reports (`reports/05 Sent to clients/`)

| File | Description |
|------|-------------|
| `A4_final_report_Jessica_Duong.xlsx` | Final analysis report with all findings and recommendations |

### Project Management (`project-management/`)

| File | Description |
|------|-------------|
| `Instacart_Basket_Analysis_Project_Brief.pdf` | Original project brief and requirements |

## Author
**Jess Duong**  
Aspiring Business Intelligence Analyst  


## Data Citation

"The Instacart Online Grocery Shopping Dataset 2017", Accessed from www.instacart.com/datasets/grocery-shopping-2017 via Kaggle on December 8, 2025.

*Note: Instacart is a real company and the data used in this project is publicly available. The business context and project brief were adapted for academic purposes as part of the CareerFoundry Analytics program.*

