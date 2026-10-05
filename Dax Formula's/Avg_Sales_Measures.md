# Average Sales Measures

This document contains the DAX measures used to analyze average sales performance, year-to-date average sales, previous-year average sales, average sales growth, month-to-date average sales, and KPI reporting across the Car Sales Analysis Dashboard.

---

## 1. Average Sales

```DAX:
Average Sales =
AVERAGE('Cars Sales Data'[Price ($)])
```
Description: Calculates the average selling price of cars across all sales transactions.

---

## 2. YTD Average Sales

```DAX:
YTD Average Sales =
CALCULATE(
    [Average Sales],
    DATESYTD('Caledar Table'[Date])
)
```
Description: Calculates the average car selling price for the period from the beginning of the year up to the selected date.

---

## 3. PYTD Average Sales

```DAX:
PYTD Average Sales =
CALCULATE(
    [Average Sales],
    SAMEPERIODLASTYEAR('Caledar Table'[Date])
)
```
Description: Calculates the average selling price for the corresponding period in the previous year.

---

## 4. Average Sales Growth %

```DAX:
Average Sales Growth % =
DIVIDE(
    [YTD Average Sales] - [PYTD Average Sales],
    [PYTD Average Sales],
    0
)
```
Description: Calculates the percentage increase or decrease in average sales compared with the previous year.

---

## 5. MTD Average Sales

```DAX:
MTD Average Sales =
CALCULATE(
    [Average Sales],
    DATESMTD('Caledar Table'[Date])
)
```
Description: Calculates the average selling price for the selected month up to the current date.

---

## 6. MTD Average Sales KPI

```DAX:
MTD Average Sales KPI =
CONCATENATE(
    "MTD Average Sales : ",
    FORMAT(
        [MTD Average Sales] / 1000,
        "$0.00K"
    )
)
```
Description: Converts MTD average sales into a formatted KPI text showing the average selling price in thousands.
