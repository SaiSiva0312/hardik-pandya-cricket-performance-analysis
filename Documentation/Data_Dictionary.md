# 📖 Data Dictionary

## Project

**Hardik Pandya Cricket Performance Analysis**

This document describes the datasets and fields used in the Power BI dashboard.

---

# 1. Matches Dataset

The Matches table contains match-level information and acts as the parent table in the data model.

| Column | Description |
|---|---|
| Match_ID | Unique identifier for each match |
| Match_Number | Match number/reference |
| Date | Date of the match |
| Year | Year in which the match was played |
| Format | Test, ODI or T20I |
| Opponent | Opposition team |
| Venue | Match venue |
| City | City where the match was played |
| Result | Match result |
| Margin | Winning margin |
| Hardik_Runs | Runs scored by Hardik in the match |
| Hardik_Wickets | Wickets taken by Hardik in the match |

---

# 2. Batting Dataset

The Batting table contains Hardik Pandya's innings-level batting performance.

| Column | Description |
|---|---|
| Match_ID | Identifier linking the innings to the Matches table |
| Innings_No | Batting innings number |
| Format | Match format |
| Opponent | Opposition team |
| Venue | Match venue |
| Runs | Runs scored |
| Fours | Number of fours |
| Sixes | Number of sixes |
| Strike_Rate | Batting strike rate |

---

# 3. Bowling Dataset

The Bowling table contains Hardik Pandya's bowling performance.

| Column | Description |
|---|---|
| Match_ID | Identifier linking the bowling record to the Matches table |
| Date | Match date |
| Format | Match format |
| Innings_No | Bowling innings number |
| Balls_Bowled | Number of balls bowled |
| Maidens | Maiden overs |
| Runs_Conceded | Runs conceded |
| Wickets | Wickets taken |
| Economy | Bowling economy rate |

---

# 🔗 Data Relationships

The datasets are connected using `Match_ID`.

```text
                 Matches
                Match_ID
                   │
              1    │    *
                   │
          ┌────────┴────────┐
          ↓                 ↓
       Batting           Bowling
      Match_ID           Match_ID
