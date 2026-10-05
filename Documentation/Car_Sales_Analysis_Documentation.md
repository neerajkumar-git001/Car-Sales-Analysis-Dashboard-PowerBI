# Car Sales Analysis Dashboard Documentation

## 1. Project Overview

The **Car Sales Analysis Dashboard** is a business intelligence project developed to analyze vehicle sales performance and identify the key factors driving revenue growth.

The project transforms raw car sales data into an interactive Power BI solution covering revenue, sales volume, average selling price, brand performance, body style, color, dealer performance, customer information, and regional trends.

The primary focus is **business decision-making**, not only visualization.

---

## 2. Business Objective

The objective is to help sales and management teams understand:

- Revenue and sales-volume performance
- Whether growth is driven by price or volume
- Brand and product-category contribution
- Dealer and regional performance
- Year-over-year performance
- Opportunities to improve pricing and sales strategy

---

## 3. Business Problem

Raw transactional data contains valuable information, but it does not immediately explain what is driving business performance.

The business needs a centralized analytical solution to answer:

- Which brands generate the most revenue?
- Is revenue growth coming from higher prices or more cars sold?
- Which body styles and colors have the strongest demand?
- Which dealers and regions perform strongly?
- How does current performance compare with the previous year?

---

## 4. Business Solution

The Power BI solution provides:

- Executive sales KPIs
- YTD and MTD analysis
- Previous-year comparison
- Sales and volume growth
- Average selling price analysis
- Brand performance
- Body-style analysis
- Color analysis
- Dealer and regional analysis
- Customer-level details
- Interactive filters
- Business insight reporting

The solution connects **data → metrics → trends → insights → recommendations**.

---

## 5. Dataset

The project uses transaction-level car sales data.

### Main Fields

- Car ID
- Date
- Customer Name
- Gender
- Annual Income
- Dealer Name
- Company
- Model
- Engine
- Transmission
- Color
- Price
- Dealer Number
- Body Style
- Phone
- Dealer Region

### Dataset

[Car Sales Dataset](../Data%20Set/Car_Sales_Data.xlsx)

---

## 6. Data Preparation

The data preparation process includes:

1. Data-type validation
2. Missing-value and consistency checks
3. Categorical-field standardization
4. Date preparation
5. Calendar-table creation
6. Date relationship setup
7. DAX measure creation
8. KPI validation

---

## 7. Data Model

A dedicated **Calendar Table** is used as the primary date dimension for:

- Year analysis
- Month analysis
- Week analysis
- YTD calculations
- MTD calculations
- Previous-year comparisons
- Growth calculations
- Trend analysis

[Calendar Table DAX Documentation](../Dax%20Formula's/Calender_Table_Measures.md)

---

## 8. DAX Measures

### Sales Measures

[Sales Measures](../Dax%20Formula's/Sales_Measures.md)

Includes Total Sales, YTD Sales, PYTD Sales, Sales Growth %, MTD Sales, MTD Sales KPI, and peak-sales analysis.

### Average Sales Measures

[Average Sales Measures](../Dax%20Formula's/Avg_Sales_Measures.md)

Includes average selling price and related time-intelligence calculations.

### Car Sold Measures

[Car Sold Measures](../Dax%20Formula's/Car_sold_Measures.md)

Includes total cars sold, YTD cars sold, PYTD cars sold, growth, MTD cars sold, and KPI calculations.

---

## 9. Key KPIs

| KPI | Business Meaning |
|---|---|
| YTD Total Sales | Revenue generated from the beginning of the year |
| YTD Average Sales | Average selling value during the year |
| YTD Cars Sold | Sales volume during the year |
| Car Brands | Number of unique car brands |
| Sales Growth % | Year-over-year revenue growth |
| Car Sold Growth % | Year-over-year volume growth |
| MTD Sales | Current-month revenue performance |
| MTD Cars Sold | Current-month sales volume |

---

## 10. Dashboard Overview

The Overview page provides an executive view of sales performance.

### Main Components

- YTD Total Sales
- YTD Average Sales
- YTD Cars Sold
- Car Brands
- Sales trend
- Sales by body style
- Sales by color
- Top 10 companies
- Dealer-region sales
- Company performance table
- Key business insights

[Dashboard Overview Preview](../Overview/Car_Sales_Analysis_Dashboard_Overview_Preview.png)

---

## 11. Dashboard Details

The Details page provides transaction-level analysis.

### Available Fields

- Car ID
- Customer Name
- Gender
- Dealer Name
- Company
- Color
- Model
- Transmission
- Total Sales

### Interactive Filters

- Body Style
- Dealer Name
- Engine
- Transmission
- Company
- Gender

[Dashboard Details Preview](../Overview/Car_Sales_Analysis_Dashboard_Details_Preview.png)

---

## 12. Key Business Findings

### Revenue Growth

YTD sales reached approximately **$371.19M**, representing **23.59% growth** compared with the previous year.

### Sales Volume

Approximately **13.26K cars** were sold, with car volume increasing by **9.27%**.

### Average Selling Price

Average sales were approximately **$27.99K**, with a **0.79% decline** compared with the previous year.

### Brand Performance

**Chevrolet** was the leading brand in the displayed company analysis.

### Body Style

**SUVs** were the strongest body-style category by sales.

### Color Performance

**Pale White** generated the highest sales among the analyzed color categories.

---


## 13. Business Problem, Solution, and Business Improvement

### 13.1 Business Problem

The business had a large volume of car sales transactions, but raw transactional data made it difficult to quickly understand overall performance and identify the reasons behind revenue changes.

The main business challenges were:

- Sales performance was spread across thousands of individual transactions.
- Management could not quickly identify the strongest brands and product categories.
- Revenue growth could not easily be separated into **volume growth versus average selling-price movement**.
- Comparing current performance with the previous year required manual analysis.
- Dealer and regional performance was difficult to compare at a management level.
- Important KPIs such as revenue, cars sold, average sales, and growth were not available in one interactive view.
- Detailed customer and transaction information existed, but it was difficult to investigate without filtering and segmentation.

### 13.2 How I Solved the Problem

I converted the raw sales dataset into an interactive Power BI business intelligence solution.

The solution process was:

1. **Prepared the raw data** using Power Query for analysis.
2. **Created a dedicated Calendar Table** to support reliable time-based analysis.
3. **Built DAX measures** for total sales, YTD sales, previous-year sales, sales growth, MTD sales, cars sold, average sales, and other KPIs.
4. **Created an interactive data model** to connect transaction-level sales with time-based analysis.
5. **Designed executive KPIs** so management can understand performance quickly.
6. **Added trend and category analysis** to identify changes in sales performance.
7. **Added brand, body-style, color, dealer, and regional analysis** to identify business drivers.
8. **Created a detailed transaction page** so users can move from high-level performance to individual records.
9. **Added interactive filters** so users can investigate specific segments instead of relying only on static reports.
10. **Converted analytical results into business insights and recommendations**.

### 13.3 What the Dashboard Reveals

The dashboard identifies an important business pattern:

- **YTD Sales:** $371.19M
- **Sales Growth:** +23.59%
- **Cars Sold:** 13.26K
- **Cars Sold Growth:** +9.27%
- **Average Sales:** $27.99K
- **Average Sales Change:** -0.79%
- **Car Brands:** 30

The key insight is that **revenue is growing strongly while average selling price is slightly declining**.

This indicates that **sales volume is an important driver of revenue growth**.

Therefore, management should not evaluate growth only through revenue. It should also monitor sales volume, average transaction value, product mix, and pricing together.

### 13.4 How the Dashboard Can Improve the Business

#### Revenue Improvement

Management can identify the brands, products, and regions contributing the most revenue and allocate resources toward high-performing areas.

#### Sales Volume Improvement

The dashboard highlights sales-volume trends and high-performing body styles, helping the business plan inventory and promotional campaigns around customer demand.

#### Pricing Improvement

The decline in average sales creates a pricing signal. Management can investigate discounts, product mix, and dealer-level pricing to determine whether revenue growth is being achieved at the expense of transaction value.

#### Brand Strategy

Brand-level performance helps management identify leading brands and investigate why they outperform other brands.

#### Dealer Performance

Dealer and regional analysis can identify strong dealers and weaker markets, supporting targeted sales strategies and performance improvement programs.

#### Inventory Planning

High-demand body styles, colors, and brands can be used as signals for better inventory allocation.

#### Regional Strategy

Regional sales patterns help management identify markets with strong demand and markets that require additional sales attention.

#### Executive Decision-Making

Instead of manually analyzing raw transactions, management can use the dashboard to monitor KPIs, investigate performance drivers, and make faster data-driven decisions.

### 13.5 Before vs After

| Before the Dashboard | After the Dashboard |
|---|---|
| Raw transactional data | Interactive business intelligence solution |
| Manual performance analysis | Automated KPI analysis |
| Difficult year-over-year comparison | YTD and previous-year comparison |
| Revenue viewed in isolation | Revenue, volume, and average sales analyzed together |
| Difficult brand comparison | Brand performance ranking |
| Limited regional visibility | Dealer and regional analysis |
| Difficult transaction investigation | Filterable transaction-level details |
| Static data review | Interactive decision-support dashboard |
| Data without clear business story | Insights and business recommendations |

### 13.6 Business Decision Framework

The dashboard supports a four-step decision process:

**Measure → Compare → Diagnose → Act**

**Measure:** Track revenue, cars sold, average sales, and brand performance.

**Compare:** Evaluate current performance against the previous year.

**Diagnose:** Break down performance by brand, model, body style, color, dealer, region, transmission, and customer characteristics.

**Act:** Use the findings to improve pricing, inventory allocation, dealer strategy, regional targeting, and sales performance.

### 13.7 Business Impact

The dashboard can help the business:

- Reduce manual reporting effort.
- Improve visibility into sales performance.
- Identify revenue and volume growth drivers.
- Detect pricing pressure earlier.
- Prioritize high-performing products and brands.
- Improve dealer and regional decision-making.
- Support more informed inventory planning.
- Enable faster management decisions.

The dashboard should be treated as a **decision-support system**, not simply a reporting interface.

---

## 14. Business Interpretation

Revenue increased by **23.59%**, while cars sold increased by **9.27%** and average sales declined by **0.79%**.

This indicates that business growth was strongly supported by **higher sales volume rather than higher average selling prices**.

The key management question is:

> Can the business maintain volume growth while improving average transaction value?

---

## 15. Business Recommendations

### 1. Protect High-Volume Segments

Continue supporting high-demand body styles such as SUVs through inventory planning and targeted sales campaigns.

### 2. Analyze Chevrolet's Success

Investigate Chevrolet's models, pricing, dealers, and regions to identify successful strategies that can be applied to other brands.

### 3. Monitor Pricing Pressure

Because average sales declined while revenue increased, monitor discounts, pricing strategy, and product mix.

### 4. Improve Regional Performance

Use dealer-region analysis to identify underperforming markets and develop targeted sales strategies.

### 5. Increase Average Transaction Value

Use premium models, accessories, financing products, and targeted upselling to increase transaction value without sacrificing sales volume.

---

## 16. Proposed Business Improvements

### Profitability Analysis

Add vehicle cost, gross margin, net margin, dealer margin, and profit by brand or dealer.

### Customer Analytics

Add customer segmentation, repeat-customer analysis, customer lifetime value, and income-based purchasing analysis.

### Dealer Performance

Add dealer target vs actual, dealer growth, dealer ranking, and conversion performance.

### Forecasting

Add monthly sales forecasting, demand forecasting, brand-level forecasting, and regional forecasting.

### Advanced BI

Future versions can include:

- Automated refresh
- What-if pricing analysis
- AI-powered insights
- Anomaly detection
- Prescriptive recommendations
- Automated executive reporting

---

## 17. Dashboard Assets

### KPI Images

[Average Sales KPI](../KPI's%20Image/Avg._Sales.png)

[Car Brands KPI](../KPI's%20Image/Car_Brands.png)

[Cars Sold KPI](../KPI's%20Image/Car_sold.png)

[Header Line](../KPI's%20Image/Header_Line.png)

[Total Sales KPI](../KPI's%20Image/Total_Sales.png)

---

## 18. Power BI Dashboard

[Open Power BI Dashboard](../Car_Sales_Analysis_Dashboard.pbix)

---

## 19. Project Workflow

```text
Raw Sales Data
      ↓
Data Validation
      ↓
Data Preparation
      ↓
Calendar Table
      ↓
Data Modeling
      ↓
DAX Measures
      ↓
KPI Development
      ↓
Interactive Dashboard
      ↓
Business Analysis
      ↓
Insights
      ↓
Business Recommendations
```

---

## 20. Tools & Technologies

- Power BI
- DAX
- Power Query
- Microsoft Excel
- Data Modeling
- Business Intelligence
- Data Visualization
- Sales Analytics
- Time Intelligence
- Business Storytelling

---

## 21. Limitations

The dashboard focuses mainly on sales performance and does not provide complete profitability analysis.

The current dataset does not include all cost information required to calculate:

- Gross profit
- Net profit
- Dealer margin
- Customer acquisition cost
- Inventory carrying cost
- Marketing ROI

Therefore, revenue growth should not automatically be interpreted as profit growth.

---

---


## 22. Business Analysis Framework

This project follows a practical business analytics framework:

### 1. Performance

Measure the current business position using:

- Revenue
- Cars sold
- Average selling price
- Brand contribution
- Regional contribution

### 2. Comparison

Compare current performance with the previous year using:

- YTD performance
- PYTD performance
- Sales Growth %
- Car Sold Growth %
- Average Sales Growth %

### 3. Diagnosis

Break down performance by:

- Company
- Model
- Body Style
- Color
- Dealer
- Dealer Region
- Transmission
- Gender

### 4. Decision Support

Translate the findings into actions related to:

- Inventory allocation
- Pricing
- Product mix
- Dealer performance
- Regional sales strategy
- Revenue growth

---

## 23. Technical Skills Demonstrated

This project demonstrates the following practical technical capabilities:

### Power BI

- Interactive dashboard development
- KPI card design
- Drill-down analysis
- Interactive filtering
- Business-oriented visual design
- Executive dashboard development

### DAX

- `SUM`
- `AVERAGE`
- `COUNT`
- `DISTINCTCOUNT`
- `CALCULATE`
- `TOTALYTD`
- `TOTALMTD`
- `SAMEPERIODLASTYEAR`
- `DATESYTD`
- `DATESMTD`
- `DIVIDE`
- `FORMAT`
- `CONCATENATE`
- `MAXX`
- `ALLSELECTED`
- Conditional logic using `IF`

These calculations support sales KPIs, time intelligence, growth analysis, dynamic KPI labels, and peak-value identification.

### Power Query

- Data cleaning
- Data-type management
- Data preparation
- Transformation of raw source data
- Preparing analytical data for the Power BI model

### Data Modeling

- Dedicated Calendar table
- Date-based analysis
- Time-intelligence structure
- Relationship-driven reporting
- Separation of transactional data and date dimension

### Data Visualization

- KPI design
- Trend analysis
- Category comparison
- Top-N analysis
- Geographic sales analysis
- Detail-level reporting
- Visual storytelling

### Business Analytics

- KPI interpretation
- Year-over-year analysis
- Growth-driver analysis
- Product and brand analysis
- Regional performance analysis
- Pricing analysis
- Business recommendation development

---

## 24. Technical-to-Business Mapping

| Technical Capability | Business Application |
|---|---|
| DAX Time Intelligence | Compare current performance with previous periods |
| Calendar Table | Enable reliable time-based reporting |
| YTD Measures | Monitor cumulative annual performance |
| MTD Measures | Monitor current-month performance |
| Growth Measures | Identify business acceleration or decline |
| Distinct Count | Measure brand coverage |
| KPI Design | Provide fast executive performance monitoring |
| Interactive Filters | Allow managers to investigate performance drivers |
| Trend Analysis | Identify changes in sales performance |
| Regional Analysis | Identify strong and weak markets |
| Product Analysis | Understand customer demand |
| Data Modeling | Build a reliable analytical reporting structure |

---

## 25. Technical Architecture

The project follows this analytical architecture:

```text
Car Sales Excel Dataset
          ↓
     Data Preparation
          ↓
      Power Query
          ↓
    Power BI Data Model
          ↓
     Calendar Table
          ↓
       DAX Measures
          ↓
     KPI Calculations
          ↓
 Interactive Dashboard
          ↓
 Business Analysis
          ↓
 Insights & Recommendations
```

The architecture separates **data preparation, modeling, calculation, visualization, and business interpretation**, making the solution easier to maintain and extend.

---

## 26. Data Quality & Validation

Before using the dashboard for decision-making, key outputs should be validated against the source dataset.

Validation areas include:

- Total transaction count
- Total sales amount
- Unique brand count
- Date coverage
- Missing values
- Duplicate records
- Category consistency
- KPI reconciliation
- YTD and previous-year calculations

This validation reduces the risk of presenting incorrect business information to decision-makers.

---

## 27. Business Impact

The dashboard can support management in four major areas:

### Revenue Management

Identify which brands, products, and regions contribute most to revenue.

### Sales Volume Management

Track whether growth is coming from increased vehicle volume.

### Pricing Management

Monitor average selling price and identify potential pricing pressure.

### Resource Allocation

Use brand, dealer, product, and regional performance to prioritize sales and inventory resources.

---

## 28. Decision-Making Example

### Business Signal

Revenue increased by **23.59%**, while cars sold increased by **9.27%** and average sales declined by **0.79%**.

### Business Interpretation

The company is generating more revenue primarily through stronger sales volume rather than higher average selling prices.

### Management Question

Is the business achieving sustainable growth, or is it relying on volume and potentially lower pricing?

### Recommended Action

Analyze discounts, product mix, premium-model sales, and dealer-level pricing to determine whether average transaction value can be improved without reducing sales volume.

This demonstrates how the dashboard moves beyond reporting into **business diagnosis and decision support**.

---

## 29. Future Technical Improvements

Future versions can strengthen the technical architecture by adding:

- Star-schema optimization
- Dedicated dimension tables
- More robust date hierarchy
- Calculation groups
- Dynamic titles
- Field parameters
- Advanced drill-through pages
- Row-level security
- Automated refresh
- Deployment through Power BI Service
- Performance optimization using DAX Studio
- Model optimization using VertiPaq Analyzer
- Automated data-quality checks

---

## 30. Future Business Intelligence Improvements

Future versions can extend the project from descriptive analytics toward advanced decision intelligence:

### Descriptive Analytics

What happened?

- Revenue
- Volume
- Average sales
- Brand performance
- Regional performance

### Diagnostic Analytics

Why did it happen?

- Product mix
- Dealer performance
- Pricing
- Body style
- Region
- Customer characteristics

### Predictive Analytics

What could happen?

- Sales forecasting
- Demand forecasting
- Regional forecasting
- Brand-level forecasting

### Prescriptive Analytics

What should the business do?

- Optimize inventory
- Adjust pricing
- Prioritize high-potential regions
- Promote high-value products
- Improve dealer performance

---

## 31. Professional Project Positioning

This project should be positioned as a **Business Intelligence and Sales Analytics solution**, rather than simply a Power BI dashboard.

The technical implementation demonstrates the ability to build the analytical system, while the business analysis demonstrates the ability to interpret results and translate them into decisions.

The strongest project narrative is:

> **Raw data → Reliable model → Business KPIs → Performance analysis → Root-cause investigation → Business recommendations**


## 32. Conclusion

The Car Sales Analysis Dashboard transforms transactional sales data into a decision-oriented business intelligence solution.

The analysis shows that **volume growth is a major contributor to revenue growth**, while the decline in average selling price creates an opportunity to improve pricing, product mix, and transaction value.

The next stage should connect sales performance with **profitability, customer behavior, dealer performance, forecasting, and prescriptive decision-making**.
