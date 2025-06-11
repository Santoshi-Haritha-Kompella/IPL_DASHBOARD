# 🏏 IPL Power BI Dashboard Project

This project is an interactive data analytics dashboard built in **Power BI** to visualize and explore Indian Premier League (IPL) statistics. It leverages match-level and ball-by-ball data to provide powerful insights into player performance, team success, and seasonal trends.

---

## 📊 Features

- 💥 **Total Runs, Matches & Wickets KPIs**
- 🏆 **Top Batsmen** by total runs
- 📈 **Season-wise Total Runs Trend (Line Chart)**
- 🥇 **Team-wise Match Wins (Bar Chart)**
- 🧠 **Win Margin Category Distribution (Pie Chart)**
- 🎛 **Interactive Slicers** by:
  - Season
  - Team
  - Venue

---

## 📁 Dataset Used

The dashboard uses two CSV datasets:

- `matches.csv` — Contains match-level details (id, season, teams, winner, venue, win margins).
- `deliveries.csv` — Contains ball-by-ball details (match_id, batsman, bowler, runs, dismissal type).

---

## 🧮 Key DAX Measures

```dax
Total Runs = SUM(deliveries[runs_total])

Total Matches = DISTINCTCOUNT(matches[id])

Total Wickets = 
COUNTROWS(
    FILTER(deliveries, NOT(ISBLANK(deliveries[dismissal_kind])))
)

Total Balls = COUNTROWS(deliveries)

## 🖼️ Images of IPL Dashboards
https://ibb.co/0ycdwJfR


