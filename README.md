# DecodeLabs Data Analytics Internship — Projects

This repository contains my weekly project milestones from the DecodeLabs Data Analytics Internship (Cohort 2026). Each project builds on a core data analytics skill, using the same underlying e-commerce dataset.

## Repository Structure

| File | Project | Description |
|---|---|---|
| `raw_dataset.xlsx` | — | Original, unmodified e-commerce dataset (1,201 rows, 14 columns) used across all projects |
| `week1-data-cleaning/cleaned_dataset.xlsx` | Project 1 | Data cleaning and preparation — Excel, Power Query |
| `week2-eda/eda_dataset.xlsx` | Project 2 | Exploratory Data Analysis (EDA) — descriptive statistics, distribution/outlier analysis, revenue trend investigation |
| `week3-sql/queries.sql` | Project 3 | SQL Data Analysis — SELECT, WHERE, GROUP BY, and aggregations in SQL Server |

## Project Summaries

### Project 1 — Data Cleaning & Preparation
Cleaned a raw dataset with 1201 rows (14 columns: OrderID, Date, CustomerID, Product, Quantity, UnitPrice, ShippingAddress, PaymentMethod, OrderStatus, TrackingNumber, ItemsInCart, CouponCode, ReferralSource, TotalPrice). No duplicate records were found. Identified 309 blank entries in the CouponCode column and determined these represent transactions where no coupon was used, rather than missing data — labeled explicitly as "No Coupon" to remove ambiguity for downstream analysis. Standardized inconsistent number formatting in the UnitPrice and TotalPrice columns. Investigated an unusual pattern where UnitPrice varied significantly across transactions for the same product (e.g., "Monitor"); confirmed via distinct-value analysis that UnitPrice carries a near-unique value per transaction across the dataset (163 distinct prices across 163 Monitor orders), ruling out coupon usage, customer tier, and time-based pricing as explanations, and documenting this as a dataset characteristic rather than a data quality error.

**Tools Used:** Excel, Power Query

### Project 2 — Exploratory Data Analysis
Performed EDA across payment methods, products, referral sources, and revenue trends. Found Online as the most-used payment method (21.5% of transactions), with Printer and Tablet as the most-ordered products. Instagram was the top revenue-generating referral source (259 orders, $275K+), ahead of Email — however, closer investigation showed Printer and Tablet's revenue was driven more heavily by the Email channel specifically, despite Instagram leading overall; this finding is flagged for further verification given the UnitPrice randomness identified in Project 1. Found 2023 generated higher total revenue than 2024 ($552K vs. $480.2K) despite June 2024 being the single highest-revenue month in the dataset ($68K) — surrounding months are still being investigated for a possible explanation (coupon activity, delivery patterns). A box-and-whisker plot of TotalPrice showed a right-skewed distribution, with whiskers sitting noticeably apart from the median and quartiles, indicating outliers are pulling the distribution away from symmetry.

**Tools Used:** Excel (formulas, conditional formatting, PivotTables, box-and-whisker/distribution charts)

### Project 3 — SQL Data Analysis 
Imported the cleaned dataset into SQL Server. Checked for data types, constraints and column headers to ensure accurate and successful import of the file. Extracted business insights based on KPIs including sales performance, customer behaviour, product performance, Referral channel performance and Monthly/Yearly trend. Used SQL statements SELECT, WHERE, GROUP BY, HAVING, including aggregate and scalar functions (COUNT, SUM, AVG, ROUND). 

**Tools Used:** SQL Server, SQL Server Management Studio (SSMS)

## How to Navigate
1. Start with `raw_dataset.xlsx` to see the original, unmodified data.
2. Open the Project 1 file to see the cleaning process and documented data quality decisions.
3. Open the Project 2 file for the statistical analysis, distribution charts, and revenue trend investigation.
4. Open the Project 3 `.sql` file in SQL Server Management Studio to run the queries.

## Skills Demonstrated
Data cleaning, Power Query, structured data investigation and hypothesis testing, PivotTables, descriptive statistics, distribution/outlier analysis, revenue trend analysis, SQL fundamentals (filtering, sorting, grouping, aggregation).

---
*Part of the DecodeLabs Data Analytics Internship — Batch 2026.*
