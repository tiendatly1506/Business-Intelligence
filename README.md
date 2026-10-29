# Business Intelligence

Power BI projects from my Bachelor of Business Analytics (course 2030AFE: Business Intelligence), covering dashboard design, data modelling and DAX. Each project has the working file (Power BI `.pbix` or Excel `.xlsx`) and a PDF, so the work can be viewed without opening the software.

| Project | Power BI file | PDF export |
|---|---|---|
| 1. ABC International: executive sales report | [ABC International.pbix](./ABC%20International.pbix) | [ABC International.pdf](./ABC%20International.pdf) |
| 2. Office World: business problem dashboard | [OfficeWorld.pbix](./OfficeWorld.pbix) | [OfficeWorld.pdf](./OfficeWorld.pdf) |
| 3. Laptop Sales: advanced DAX analysis | [DAX.pbix](./DAX.pbix) | [DAX.pdf](./DAX.pdf) |
| 4. Tourism: predictive modelling in Excel | [Tourism Regression Model.xlsx](./Tourism%20Regression%20Model.xlsx) | [Predictive Modelling.pdf](./Predictive%20Modelling.pdf) |

---

## 1. ABC International: Executive Sales and Performance Report

**Scenario:** As lead business analyst for ABC International, a global manufacturer and distributor of premium bicycles and accessories, I turned raw data from several departments into a four-page interactive Power BI report. The executive wanted insights on customers, sales, production costs and regional performance, including year-to-date figures for both the calendar and financial year.

**What I built**
- Cleaned and transformed the sales and customer datasets in Power Query, then modelled them as a star schema.
- Built a four-page report with slicers (Year, Region) and navigation buttons:

| Page | Focus |
|---|---|
| Sale & Profitability Overview | Calendar-year and financial-year YTD KPIs, monthly sales, sales vs. costs, profitability scatter by year, customer acquisition trend |
| Sale & Product Analysis | Sales by category and sub-category, top 25 products with profit margin, top 5 sub-categories |
| Regional & Customer Analysis | Sales by country (map) and region, customer marital status, education and gender profile |
| Regional & Product Details | Total sales and costs KPIs, monthly sales trend, order-level detail table |

**Key insights**
- **Growth with controlled costs:** Sales and costs rose steadily from 2014 to 2016, with a notable sales peak in June. Customer acquisition followed the same upward pattern, especially in the later months of each year. Sales YTD reached $16.47M in the latest year against $9.66M in costs.
- **Bikes dominate:** Bikes generate about $28M in sales, roughly 97% of the $29.31M total. Road Bikes lead at $14.52M, followed by Mountain Bikes ($9.95M) and Touring Bikes ($3.84M). Accessories and clothing contribute very little.
- **Most profitable products:** The Mountain-200 series earns margins of about 45.6% and the Road-150 series about 39.3%. The top 25 products are all bikes.
- **Regional concentration:** Australia is the leading market by sales and costs, followed by the Southwest and Northwest. Several regions (Southeast, Northeast, Central) show very little activity and are worth investigating.
- **Customer profile:** The customer base is well educated (Bachelors and Partial College are the largest groups) and split almost evenly by marital status (54.18% married, 45.82% single).

**Recommendations:** Protect and grow the Mountain and Road bike lines, review why accessories and clothing contribute so little, and investigate the low-activity regions for expansion or withdrawal.

**Skills and tools:** Power BI, Power Query, star schema modelling, interactive dashboard design, KPI design (calendar vs. financial year YTD), executive reporting.

---

## 2. Office World: Data-Driven Business Problem Analysis

**Scenario:** Acting as a data analyst, I built a one-page interactive dashboard on four years of retail sales (2014 to 2017) and used it to diagnose a business problem and recommend actions.

**What I built**
- Cleaned the data in Power Query and structured it as a star schema.
- Designed a dashboard with KPI cards (Total Sales, Total Profit, Quantity, Profit Margin) and slicers for **Region, Category, Segment and Year**.
- Visuals include sales by month and category, sales and profit by sub-category, profit and sales by category, and a top 10 customers table.

**Headline numbers:** $2.30M in sales, $286.40K in profit, a 12% profit margin, and about 38K units sold. The top 10 customers contributed $153.81K in sales.

**The business problem:** How can Office World stabilise its sales flow and lift profit from weak categories, rather than depending on seasonal peaks and one dominant product line?

**Key insights**

| Dimension | Finding |
|---|---|
| Seasonality | Sales peak sharply in the last months of the year and lag in Q1, which points to uneven cash flow and resource use. |
| Time | Sales grew from $484.25K (2014) to $733.22K (2017). Sales dipped in 2015, but margin improved from 10% to 13% and held at 13% in 2016 and 2017. |
| Region | West is strongest ($725.46K sales, 15% margin). Central is the problem region ($501.24K sales, only 8% margin), with Furniture making a loss there. |
| Category | Technology ($836.15K sales, $145.45K profit, 17% margin) and Office Supplies ($719.05K, $122.49K, 17%) drive profit. Furniture has $742.00K in sales but only $18.45K in profit (2% margin). |
| Sub-category | Phones lead, while Labels and Fasteners contribute very little. |
| Segment | Consumer is largest ($1.16M) but has the lowest margin (12%). Home Office is smallest ($429.65K) but most efficient (14%). Corporate sits at 13%. |

**Recommendations**
1. Review Furniture pricing, operating costs and vendor agreements, starting with the Central region.
2. Invest in Technology and Office Supplies to expand market share and product depth.
3. Review pricing and promotions for the Consumer segment, aiming to reach Corporate-level margins.
4. Investigate the causes of the 2015 sales dip and plan to smooth Q1 demand.

**Skills and tools:** Power BI, Power Query, star schema modelling, slicer-driven exploration, business problem framing, data storytelling and recommendations.

---

## 3. Laptop Sales: Advanced DAX Analysis

**Scenario:** A laptop sales dataset analysed using DAX only (no slicers or manual filters), to show that calculations are driven by formulas rather than report interactions.

**What I built**
- **Calculated columns:** Cost of Goods Sold (unit cost × units sold) and Profit (revenue − COGS) for every record.
- **Regional profit measures:** Total online profit for the combined North and South regions, shown in a pie chart with both absolute values and percentage share.
- **Conditional sales-rep logic:** A table of West region sales representatives who sold both ProBook and Ultrabook with a combined sales value above 25,000, plus a separate measure and card visual counting the representatives who qualify.
- **Ranking measure:** All sales representatives ranked by total profit, from highest to lowest.

**Results**
- **North vs. South online profit:** North contributes $15.57M (55.36%) and South $12.56M (44.64%), a combined $28.13M.
- **Rep performance is tightly clustered:** The top named representatives, Jamie Williams ($3.21M), Sawyer Ramirez ($3.16M) and Gray Lopez ($3.15M), are only a few percent ahead of the 25th-ranked rep ($2.99M), which suggests consistent performance across the team rather than reliance on a few stars.
- **Qualifying reps card:** 43 representatives are counted by the card visual.

**Skills and tools:** DAX, calculated columns vs. measures, filter context, conditional counting, ranking measures, Power BI visuals (pie, table, card).

---

## 4. Tourism Revenue: Predictive Modelling in Excel

**Scenario:** A tourism hotel operator wants to predict local government tax revenue from hotel stays. I analysed 45 years of annual data (1980 to 2024) on guest nights and tax revenue in Excel using correlation analysis and simple linear regression.

**What I did**
- Built the analysis in Excel with live formulas (correlation, regression statistics, ANOVA, coefficients) and a forecast calculator where any guest night figure returns predicted tax revenue.
- Measured the strength and direction of the relationship with a correlation coefficient.
- Visualised it with a scatter plot and linear trendline.
- Built a simple linear regression model (tax revenue as a function of guest nights), then assessed its fit and significance.

**Key results**

| Measure | Result |
|---|---|
| Correlation | 0.8988 (very strong, positive) |
| Regression equation | Tax Revenue = 33.5545 + 0.1492 x Guest Nights |
| Slope meaning | Every extra 1,000 guest nights adds about $0.1492m in tax revenue |
| R Square | 0.8078 (guest nights explain about 81% of the variation in tax revenue) |
| Significance | p-value of 5.33E-17, so the relationship is highly statistically significant |

**Application:** The model can forecast tax revenue from projected guest nights to support budgeting, and estimate the return on tourism growth initiatives.

**Limitations:** It ignores other drivers such as tax rate changes and economic conditions, and it should not be used to predict far outside the observed range of guest nights.

**Skills and tools:** Excel, correlation analysis, simple linear regression, model interpretation, forecasting and limitations analysis.
