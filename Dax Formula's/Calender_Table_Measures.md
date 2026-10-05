# Calendar Measures

This document contains the DAX calculated table and calculated columns used to create the Calendar table. The table serves as the primary date dimension for enabling time intelligence calculations, filtering, sorting, and trend analysis across the Car Sales Analysis Dashboard.

---

## 1. Calendar Table

```DAX:
Caleder Table =
CALENDAR(
    DATE(2020, 1, 1),
    DATE(2021, 12, 31)
)
```
Description: Creates a continuous calendar table from January 1, 2020 to December 31, 2021. This table acts as the primary date dimension for all time-based analysis.

---

## 2. Year

```DAX:
Year =
YEAR('Caleder Table'[Date])
```
Description: Extracts the year from each date for yearly analysis and filtering.

---

## 3. Month No

```DAX:
Month No =
MONTH('Caleder Table'[Date])
```
Description: Returns the numeric month from 1 to 12 for monthly analysis and chronological sorting.

---

## 4. Month Name

```DAX:
Month Name =
FORMAT('Caleder Table'[Date], "MMM")
```
Description: Returns the abbreviated month name, such as Jan, Feb, and Mar, for report visuals.

---

## 5. Week

```DAX:
Week =
WEEKNUM('Caleder Table'[Date], 1)
```
Description: Returns the week number of the year with Sunday as the first day of the week.
