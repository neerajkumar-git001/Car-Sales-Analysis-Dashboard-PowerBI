# Sales Measures

This document contains the DAX measures used to analyze total sales, year-to-date performance, previous-year performance, sales growth, month-to-date performance, and KPI reporting across the Car Sales Analysis Dashboard.

---

## 1. Total Sales

```DAX:
Total Sales =
SUM('Cars Sales Data'[Price ($)])
```
Description: Calculates the total sales revenue generated from all car sales transactions.

---

## 2. YTD Total Sales

```DAX:
YTD Total Sales =
TOTALYTD(
    [Total Sales],
    'Caledar Table'[Date]
)
```
Description: Calculates cumulative sales from the beginning of the year up to the selected date.

---

## 3. PYTD Sales

```DAX:
PYTD Sales =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR('Caledar Table'[Date])
)
```
Description: Calculates sales for the corresponding period in the previous year for year-over-year comparison.

---

## 4. Sales Growth %

```DAX:
Sales Growth % =
DIVIDE(
    [YTD Total Sales] - [PYTD Sales],
    [PYTD Sales],
    0
)
```
Description: Calculates the percentage growth or decline in YTD sales compared with the previous year.

---

## 5. MTD Total Sales

```DAX:
MTD Total Sales =
TOTALMTD(
    [Total Sales],
    'Caledar Table'[Date]
)
```
Description: Calculates cumulative sales from the beginning of the selected month up to the selected date.

---

## 6. MTD Sales KPIs

```DAX:
MTD Sales Kpis =
CONCATENATE(
    "MTD Total Sales : ",
    FORMAT(
        [MTD Total Sales] / 1000000,
        "$0.00M"
    )
)
```
Description: Converts MTD sales into a formatted KPI text showing the monthly sales value in millions.
