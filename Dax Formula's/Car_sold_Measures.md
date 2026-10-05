# Car Sales Measures

This document contains the DAX measures used to analyze total cars sold, year-to-date performance, previous-year performance, sales growth, month-to-date performance, and KPI reporting across the Car Sales Analysis Dashboard.

---

## 1. Total Car Sold

```DAX:
Total Car Sold =
COUNT('Cars Sales Data'[Car_id])
```
Description: Calculates the total number of cars sold based on the available car transaction records.

---

## 2. YTD Car Sold

```DAX:
YTD Car Sold =
TOTALYTD(
    [Total Car Sold],
    'Caledar Table'[Date]
)
```
Description: Calculates the cumulative number of cars sold from the beginning of the year up to the selected date.

---

## 3. PYTD Car Sold

```DAX:
PYTD Car Sold =
CALCULATE(
    [Total Car Sold],
    SAMEPERIODLASTYEAR('Caledar Table'[Date])
)
```
Description: Calculates the number of cars sold during the corresponding period of the previous year.

---

## 4. Car Sold Growth %

```DAX:
Car Sold Growth % =
DIVIDE(
    [YTD Car Sold] - [PYTD Car Sold],
    [PYTD Car Sold],
    0
)
```
Description: Calculates the percentage growth or decline in cars sold compared with the previous year.

---

## 5. MTD Car Sold

```DAX:
MTD Car Sold =
TOTALMTD(
    [Total Car Sold],
    'Caledar Table'[Date]
)
```
Description: Calculates the cumulative number of cars sold from the beginning of the selected month up to the selected date.

---

## 6. MTD Car KPIs

```DAX:
MTD Car KPIs =
CONCATENATE(
    "MTD Car Sold : ",
    FORMAT(
        [MTD Car Sold] / 1000,
        "0.00K"
    )
)
```
Description: Converts MTD car sales into a formatted KPI text showing the number of cars sold in thousands.
