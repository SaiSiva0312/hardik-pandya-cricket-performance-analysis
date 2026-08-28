# 🏏 Hardik Pandya — Cricket Performance Dashboard

An interactive Power BI dashboard analyzing Hardik Pandya's batting,
bowling and overall all-round performance across years, formats and
opponents.

## 📊 Dashboard Preview

![Hardik Pandya Dashboard](Screenshots/dashboard.png)

---

## 🎯 Project Objective

The objective of this project was to transform raw cricket match data
into an interactive analytical dashboard using Power BI.

The dashboard helps analyze:

- Batting performance
- Bowling performance
- Year-wise trends
- Runs against opponents
- Wickets against opponents
- All-round impact
- Career highlights

---

## 🗂️ Dataset

The project uses three structured datasets:

### 1. Matches

Contains match-level information such as:

- Match ID
- Date
- Year
- Format
- Opponent
- Venue
- Result
- Margin

### 2. Batting

Contains batting-level statistics:

- Match ID
- Innings
- Runs
- Fours
- Sixes
- Strike Rate
- Format
- Opponent

### 3. Bowling

Contains bowling-level statistics:

- Match ID
- Innings
- Balls Bowled
- Maidens
- Runs Conceded
- Wickets
- Economy
- Format

---

## 🔗 Data Model

The three datasets were connected using `Match_ID`.

Matches acts as the central table:

Matches → Batting  
Matches → Bowling

Relationship:

`One-to-Many`

![Data Model](Screenshots/data-model.png)

---

## 🧮 DAX Measures

Key measures created in Power BI include:

- Total Matches
- Total Runs
- Batting Average
- Batting Strike Rate
- Total Wickets
- Bowling Average
- Bowling Economy
- All-Round Impact Index
- Best Batting
- Best Bowling
- Fifties
- Hundreds
- Four-Wicket Hauls
- Five-Wicket Hauls

---

## 📈 Dashboard Features

### KPI Analysis
- Total Matches
- Total Runs
- Batting Average
- Strike Rate
- Total Wickets
- Bowling Average

### Performance Trends
- Batting performance by year
- Bowling performance by year

### Opponent Analysis
- Runs against opponents
- Wickets against opponents

### All-Round Analysis
- All-round impact by year

### Career Highlights
- Best batting
- Best bowling
- 50s
- 100s
- 4-wicket hauls
- 5-wicket hauls
- Runs + wickets

---

## 🛠️ Tools & Technologies

- Power BI
- DAX
- Data Modeling
- Data Cleaning
- CSV
- Data Visualization

---

## 💡 Key Learning

This project helped me understand the complete analytics workflow:

Raw Data → Data Preparation → Data Modeling → DAX → Visualization → Insights

---

## 📌 Future Improvements

- Add more advanced player-comparison analysis
- Add format-specific performance benchmarking
- Add additional cricket metrics
- Improve automated data refresh
- Expand the dashboard to compare multiple players

---

## 👨‍💻 Author

Sai Siva Sundar Jena

B.Tech — Computer Science & Engineering
