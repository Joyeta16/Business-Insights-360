# Business Insights 360  
## Company Overview  

AtliQ Hardware is a rapidly growing electronics company specializing in hardware products, including PC accessories, printers, and more. Over the years, AtliQ has expanded significantly, establishing a strong global presence in key regions such as APAC, North America, Latin America, and the European Union.

The company distributes its products through two primary sales platforms:
- Brick-and-Mortar Stores – Partnering with physical retail outlets like Croma and Best Buy.
- E-Commerce Platforms – Selling through online giants like Amazon and Flipkart.

Moreover, AtliQ operates through multiple sales channels:
- Retailers – Third-party sellers, both online and offline, that stock and sell AtliQ’s products.
- Direct Stores – AtliQ’s own branded stores, where consumers can purchase directly.
- Distributors – In restricted markets like China and South Korea, AtliQ collaborates with large distributors to ensure product availability.

**Note:** AtliQ’s customers are retailers and distributors, while the consumers are the end users.

## Problem Statement

As a rapidly growing company, AtliQ Hardware's reliance on scattered Excel sheets for analytics has led to inefficient decision-making, resulting in significant losses, particularly during its Latin American expansion. Meanwhile, competitors leveraging advanced data analytics have gained an edge, leaving AtliQ struggling to keep up with outdated methods. To improve transparency in data-driven decisions and stay competitive, AtliQ has launched a data analytics project to enhance decision-making and strategic growth.

## Project Objective

To develop an intuitive dashboard that delivers actionable insights for finance, sales, marketing, and supply chain teams, along with an executive and key performers view. This will enhance transparency, improve data accessibility, and empower stakeholders to make informed, data-driven decisions for strategic growth and efficiency.

## Data Overview

AtliQ Hardware has provided two SQL databases and three Excel files for analysis.  

The three Excel files are:
- Operating Expenses
- Targets (available only for FY 2022)
- Market Share (limited to the Personal Computer division)

The two databases contain the following tables:  

- gdb041:
  - Fact tables: fact_forecast_monthly, fact_sales_monthly
  - Dimension tables: dim_customer, dim_market, dim_product

- gdb056:
  - Contains freight_cost, gross_price, manufacturing_cost, post_invoice_deductions, and pre_invoice_deductions

AtliQ’s fiscal year runs from September to August, and the dataset covers actual sales from September 1, 2017, to December 31, 2021.

**NOTE:** Since this is a bootcamp project, the data files cannot be shared.

## Data Cleaning & Transformation

### Standardized & Trimmed Data:
- Removed leading and trailing spaces from text fields.
- Standardized naming conventions for consistency.

### Data Structuring & Optimization:
- Created a dim_date table for better time-based analysis.
- Merged fact_sales_monthly and fact_forecast_monthly into a single table, fact_actual_estimates, to simplify calculations.
- Added calculated fields in fact_actual_estimates using data from relevant tables (e.g., deriving pre-invoice deductions using percentage values from the pre_invoice_deductions table).
- Disabled load for tables that were used to derive calculations in fact_actual_estimates to optimize performance and reduce the Power BI report size.

## Report Inclusions  
This repository includes a PDF version of the Power BI report hosted on the Power BI Service, along with its underlying data model. Below, you’ll find a screenshot of the data model and a PDF of the report for a quick preview.

## Tools Used:
**Data Visualization:** Power BI
**Data Analysis:** DAX
**Data Cleaning & Transformation:** Power Query

## Insights

### Business Growth & Financial Performance:

- Rapid expansion: Gross Sales grew 260% (FY 2019), 150% (FY 2020), ~200% (FY 2021), and ~350% (FY 2022).
- Net Profit % remains negative due to high operational and marketing expenses, typical for a company in its growth phase.

### Revenue & Market Trends:

- APAC remained the largest market (FY 2019–FY 2022), led by India, while Latin America was the smallest.
- Amazon was the top global customer in all years, while Nova (operating in Austria) was the smallest since FY 2020.
- Notebook segment had the highest Revenue growth in all fiscal years but recorded the most negative Net Profit % in FY 2022, likely due to increased marketing spend.
- Desktop had the lowest growth in FY 2019 & FY 2020, while Networking became the weakest segment in FY 2022.
- USB flash drives underperformed in FY 2021 & FY 2022, signaling product or market challenges.

### Sales & Customer Insights:

- Flat post-discounting model for all products and customers within each market is significantly eroding Gross Margin %. A performance-based discounting strategy per product and customer within each market is recommended to optimize profitability.
- Certain products, like AQ 5000 Series Electron 9 5900X, AQ MB Elite, and AQ Wi Power Dx1, had zero sales in FY 2022, likely due to demand shifts or outdated models.

### Forecast Accuracy & Supply Chain Efficiency:

- Forecast Accuracy (FCA%) dropped from 86% (FY 2019) to 73% (FY 2020) due to COVID-19 disruptions but improved to 80.21% (FY 2021) and 81.17% (FY 2022).
- Excess inventory was a major issue in FY 2019–FY 2020, while stock shortages became a challenge in FY 2021–FY 2022.
- Work-from-home demand surged in FY 2020, leading to stockouts for processors, keyboards, and WiFi extenders.

### Competitive Position & Market Share:

- Atliq’s PC market share grew from ~1% (FY 2021) to ~6% (FY 2022), though Dale remains the dominant player.
- India was the fastest-growing market (~13% share in FY 2022).
- Among subzones, North America had the highest revenue in FY 2022, but Atliq’s market penetration remained only ~5%.

### Operational & Strategic Insights:

- Sales peaked from September to December across all years, likely due to festive and year-end promotions.
- Retailers contributed ~72% of revenue in FY 2022.
- The UK had the highest marketing costs, making it a key area for strategy review, followed by Germany (low revenue, high marketing spend).

## Recommendations

- Optimize costs: Gradually reduce operational and marketing expenses after capturing significant market share to improve Net Profit %.
- Refine discounting strategy: Shift from flat post-discounting to a performance-based model per product & customer in each market.
- Strengthen India & APAC: Expand distribution and targeted marketing in high-growth regions.
Reevaluate pricing or cost structure for the Notebook segment to improve Net Profit %.
Investigate declining performance of USB flash drives—either reposition, discontinue, or introduce improved models.
- Enhance forecasting: Use AI-driven models to minimize stock imbalances and improve supply chain efficiency.
- Boost North America penetration: Develop targeted strategies to improve market share despite high revenue contribution.
- Strengthen PC segment competitiveness: Focus on differentiation to challenge dominant players like Dale.
- Reassess marketing ROI: Optimize spending in the UK & Germany to ensure efficient returns.
- Leverage peak seasonality: Align inventory planning and promotions for the Sep–Dec sales surge.
## Skills Gained
