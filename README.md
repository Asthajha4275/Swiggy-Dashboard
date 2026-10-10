# Swiggy Sales Analysis Dashboard

> An Excel dashboard analysing 197,430 Swiggy food-order records across 28 states (Jan-Aug 2025) to track sales, ratings, order volume and average order value by time, city, state and food type.

## Business Problem
Swiggy needs a single view of how its food-delivery business is performing. This project follows a Business Requirements Document (BRD) that asks for five KPIs and seven charts, so the business can see where revenue comes from, how it changes over time, and how satisfied customers are.

## Dataset
- **Source:** Swiggy order dataset (`Swiggy_Raw_Data_Excel.xlsx`, sheet `Swiggy Data`)
- **Size:** 197,430 rows x 14 columns
- **Period:** 1 Jan 2025 to 31 Aug 2025
- **Coverage:** 28 states, 28 cities, 993 restaurants
- **Columns:** State, City, Order Date, Day, Quarter, Week, Restaurant Name, Location, Category, Dish Name, Food Type (Veg / Non-Veg), Price (INR), Rating, Rating Count

## Tools Used
Microsoft Excel (Pivot Tables, Pivot Charts, Slicers, map chart)

## KPIs (from the BRD)
| KPI | Value |
|---|---|
| Total Sales | ₹5.30 crore (₹53,012,505.77) |
| Total Orders | 197,430 |
| Average Order Value (AOV) | ₹268.51 |
| Average Rating | 4.34 |
| Ratings Count | 5,591,574 |

## Charts Built
1. Monthly Sales Trend
2. Daily Sales Trend (by day of the week)
3. Total Sales by Food Type (Veg vs Non-Veg)
4. Total Sales by State (map)
5. Quarterly Performance Summary (sales, ratings and orders)
6. Top 5 Cities by Sales
7. Weekly Trend Analysis

## Approach
1. Reviewed the BRD and defined the KPIs and charts to build
2. Checked the dataset: no missing values; 26 fully duplicate rows (about 0.01%) were left in
3. Created pivot tables for each KPI and chart
4. Built the charts and combined them into one dashboard with slicers
5. Wrote up insights from the results

## Key Insights
| Theme | Finding |
|---|---|
| **Food type** | Veg dishes bring in 64.5% of sales (₹3.42 crore) against 35.5% for Non-Veg (₹1.88 crore). Veg also has a slightly higher average rating (4.35 vs 4.32). |
| **Top cities** | Bengaluru leads with ₹54.6 lakh (10.3% of sales), followed by Lucknow (₹31.2 lakh), Hyderabad (₹30.2 lakh), Mumbai (₹30.2 lakh) and New Delhi (₹28.3 lakh). |
| **Monthly trend** | Sales stay in a narrow range of ₹62.7 lakh to ₹68.3 lakh a month. January is the highest and February the lowest (a shorter month). |
| **Day of week** | Saturday is the best day (14.7% of sales) and Tuesday the weakest (13.9%). Weekday and weekend sales are very close. |
| **Quarters** | Q2 has the highest sales (₹1.99 crore, 37.5%), just ahead of Q1 (₹1.97 crore). Q3 looks lower only because the data stops at 31 August. |
| **Weekly trend** | Week 8 is the peak week (about ₹17.6 lakh). The last week (week 36) is low because it is only partly covered. |
| **Customer satisfaction** | Ratings are steady at about 4.3 across days, quarters and food types, so satisfaction is consistently high. |

## Recommendations
- Grow Non-Veg offerings and promotions, since Veg already dominates and Non-Veg has room to grow.
- Run weekday offers, especially on Tuesday and Monday, to lift the lowest days.
- Study what drove the Week 8 peak (campaign, event or offer) and repeat it.
- Strengthen supply in the top cities and test marketing in the weaker states.

## Data Notes
- "Total Orders" is the count of dish-level records in the dataset.
- About 40% of rows (79,094) have a Rating Count of 0, which likely means new or unrated items.
- Q3 and the final week are partial because the data ends on 31 Aug 2025.

## Repository Structure
```
├── data/
│   └── Swiggy_Raw_Data_Excel.xlsx   # raw data + pivot tables + dashboard
├── docs/
│   └── Problem_Statement_BRD.pdf    # KPIs and chart requirements
├── images/
│   └── dashboard.png
└── README.md
```

## How to Run
Open `Swiggy_Raw_Data_Excel.xlsx` in Excel. The `Swiggy Data` sheet holds the raw data, `Sheet1` and `Sheet2` hold the KPI and chart pivots, and the `Dashboard` sheet shows the final view with slicers.
