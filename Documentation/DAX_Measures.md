# 🧮 DAX Measures

## Hardik Pandya Cricket Performance Dashboard

This document contains the key DAX measures used to calculate KPIs and analytical metrics in the Power BI dashboard.

---

DAX Measures

```DAX
Total Matches =
DISTINCTCOUNT(Matches[Match_ID])
-----------------------------------------------------------------
Total Runs =
SUM(Batting[Runs])
-----------------------------------------------------------------
Batting Average =
DIVIDE(
    [Total Runs],
    [Batting Innings]
)
-----------------------------------------------------------------
Batting Strike Rate =
DIVIDE(
    [Total Runs] * 100,
    [Balls Faced]
)
-----------------------------------------------------------------
Total Wickets =
SUM(Bowling[Wickets])
-----------------------------------------------------------------
Bowling Average =
DIVIDE(
    [Runs Conceded],
    [Total Wickets]
)
-----------------------------------------------------------------
Bowling Economy =
DIVIDE(
    [Runs Conceded] * 6,
    [Balls Bowled]
)
-----------------------------------------------------------------
Fifties =
CALCULATE(
    COUNTROWS(Batting),
    Batting[Runs] >= 50,
    Batting[Runs] < 100
)
-----------------------------------------------------------------
Hundreds =
CALCULATE(
    COUNTROWS(Batting),
    Batting[Runs] >= 100
)
-----------------------------------------------------------------
Four Wicket Hauls =
CALCULATE(
    COUNTROWS(Bowling),
    Bowling[Wickets] = 4
)
-----------------------------------------------------------------
Five Wicket Hauls =
CALCULATE(
    COUNTROWS(Bowling),
    Bowling[Wickets] >= 5
)
-----------------------------------------------------------------
Runs + Wickets =
FORMAT([Total Runs], "#,##0")
    & " + " &
FORMAT([Total Wickets], "#,##0")
-----------------------------------------------------------------
All Round Impact =
[Total Runs] + [Total Wickets]
