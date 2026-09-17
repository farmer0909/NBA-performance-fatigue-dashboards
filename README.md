# 🏀 NBA Player Performance & Fatigue Dashboard

Interactive Power BI dashboards analyzing NBA player performance metrics and fatigue trends.

---

## 📊 Overview

Two interconnected Power BI dashboards for comprehensive NBA player analytics:

1. **NBA Player Performance Overview** 
   - Player stats: PTS, TRB, AST, GmSc
   - Player style classification: All-Around, Defender, Playmaker, Rebounder
   - Performance trend analysis
   - Team comparison view

2. **NBA Player Fatigue Dashboard**
   - Fatigue index tracking
   - Fatigue vs. Performance correlation
   - Risk classification (High/Moderate/Low)
   - Trend analysis over season

---

## 📸 Dashboard Preview

### NBA Player Performance Overview
![NBA Player Performance Overview](Images/performance_overview.png)

**Features:**
- 30 NBA team selector (grid layout)
- 4 player style classifications
- Key metrics: PTS, TRB, AST, GmSc
- Performance trend analysis
- Date and player filters

### NBA Player Fatigue Dashboard
![NBA Player Fatigue Dashboard](Images/Player%20fatigue.png)

**Features:**
- Fatigue trend line chart
- Performance vs. Fatigue scatter plot
- Risk classification (High/Moderate/Low)
- Player and team filters

---

## 📦 Data Source

- **Dataset**: NBA Player Stats (Kaggle)
- **Season**: 2024-2025
- **Format**: CSV / Excel
- **Update Frequency**: Weekly
- **Data Points**: 30 teams × ~15 players × game logs

| Source | Link | Status |
|--------|------|--------|
| Kaggle | [NBA Player Stats](https://www.kaggle.com/datasets/search?q=NBA+player) | ✅ Active |

---

## 🎯 Key Metrics

| Metric | Formula / Definition | Interpretation |
|--------|---------------------|-----------------|
| **PTS** | Points per game | Scoring output |
| **TRB** | Offensive + Defensive rebounds | Board control |
| **AST** | Assists per game | Playmaking ability |
| **GmSc** | `PTS + 0.4×FG - 0.7×FGA - 0.4×FTA + 0.7×ORB + 0.3×DRB + STL + 0.7×AST + 0.7×BLK - 0.4×PF - TOV` | Overall efficiency |
| **FatigueRisk** | Minutes played + back-to-back games + performance variance | Injury/burnout risk |

---

## 🖥️ Dashboard Features

### 📈 Performance Overview Dashboard
- **Team Selector** — Filter by all 30 NBA teams
- **Player Comparison** — 4 style classifications
  - All-Around: Balanced scorers & playmakers
  - Defender: Defensive specialists (STL, BLK)
  - Playmaker: Assist-heavy distribution (AST focus)
  - Rebounder: Board dominators (TRB focus)
- **KPI Cards** — Key stats summary
  - PTS, TRB, AST, GmSc averages
- **Performance Trend** — 2024-2025 season progression
  - GmSc trend line
  - PTS trend line
  - PlayerEFF comparison

### 📉 Fatigue Analysis Dashboard
- **Fatigue Trend Chart** — Cumulative fatigue index over time
- **Performance vs. Fatigue Scatter** — GmSc vs. MPG correlation
- **Risk Classification** — High/Moderate/Low categories
- **Filters**
  - Player name (multi-select)
  - Team (multi-select)
  - Time period (Year/Quarter/Month)

---

## 🚀 Quick Start

### Requirements
- Power BI Desktop (free) — [Download here](https://powerbi.microsoft.com/en-us/desktop/)
- Windows or Mac
- ~500MB disk space

### Steps
1. **Download** the `.pbix` file
   ```
   nba.pbix  (Power BI workbook)
   ```

2. **Open in Power BI Desktop**
   ```
   File → Open → Select nba.pbix
   ```

3. **Refresh Data** (if using live data source)
   ```
   Home → Refresh → Refresh Now
   ```

4. **Explore**
   - Click team buttons to filter
   - Use player checkboxes to select
   - Hover over charts for tooltips
   - Click charts to cross-filter

---

## 📁 Project Structure

```
nba-player-dashboard/
├── README.md                          # Main documentation (this file)
├── nba.pbix                           # Power BI workbook (both dashboards)
├── data/
│   └── sample_nba_stats.csv           # Sample data (first 100 rows)
├── docs/
│   ├── methodology.md                 # Metric definitions & calculations
│   └── screenshots/
│       ├── performance_overview.png   # Dashboard preview
│       └── fatigue_dashboard.png      # Dashboard preview
└── .gitignore                         # Git ignore rules
```

---

## 🛠️ Technical Stack

| Component | Technology |
|-----------|------------|
| **BI Tool** | Power BI Desktop |
| **Data Format** | CSV / Excel |
| **Data Source** | Kaggle |
| **Visualizations** | Bar, Line, Scatter, KPI Cards |
| **Interactivity** | Slicers, Cross-filtering, Drill-down |

### Visualizations Used
- 📊 **Bar Charts** — Team comparison, player style distribution
- 📈 **Line Charts** — Trend analysis, performance over time
- 🔵 **Scatter Plots** — Correlation (GmSc vs. Fatigue)
- 📌 **KPI Cards** — PTS, TRB, AST, GmSc summary
- 🎚️ **Hierarchical Slicers** — Date, Team, Player filters

---

## 📊 How to Interpret the Dashboards

### Performance Overview

**Player Style Bars**
- Taller bars = stronger in that category
- Compare across 4 styles to identify player archetype

**Trend Chart (2024-2025)**
- Blue line (GmSc) = Overall efficiency
- Orange line (PTS) = Scoring trend
- Declining trend = fatigue or reduced playing time

### Fatigue Dashboard

**Fatigue Trend (Top)**
- Upward trend = increasing fatigue risk
- Plateaued = consistent workload

**Performance vs. Fatigue (Bottom)**
- Upper-right quadrant = High performer, low fatigue ✅
- Upper-left quadrant = Low performance, high fatigue ⚠️
- Lower-right quadrant = Should watch for decline 👀

---

## 📈 Key Insights from Sample Data

From Adama Sanogo (shown in screenshots):
- **PTS**: 10.23 — Solid scorer
- **GmSc**: 8.37 — Above-average efficiency
- **FatigueRisk**: High — Playing heavy minutes
- **Trend**: GmSc declining from 383→210 (season progression or minutes reduction)

---

## 🔄 Data Refresh Guide

### If Using Live Kaggle Data
1. Download latest dataset from Kaggle
2. In Power BI: `Home` → `Refresh` → `Refresh Now`
3. Data updates in dashboard automatically

### If Using CSV File
1. Update CSV in `/data/` folder
2. Reopen `.pbix` file
3. Power BI prompts to refresh

---

## 🔮 Future Enhancements

- [ ] Add advanced stats (TS%, Usage%, PER)
- [ ] Implement predictive fatigue modeling (ML)
- [ ] Real-time NBA API integration
- [ ] Salary cap analysis
- [ ] Trade recommendations engine
- [ ] Injury probability dashboard
- [ ] Export to Power BI Service (cloud)
- [ ] Mobile-optimized layout

---

## ⚠️ Limitations & Assumptions

1. **Data Lag** — Kaggle dataset may not be same-day updated
2. **Injuries Not Modeled** — Fatigue doesn't account for injury history
3. **Rest Days Not Explicit** — All-Star breaks treated as normal games
4. **Team Context Missing** — Stats are individual, not team-adjusted
5. **Sample Size** — First 5 games unstable (small sample)

---

## 📚 Reference & Methodology

### Metric Sources
- Game Score formula: [John Hollinger (ESPN)](https://www.espn.com/nba/story/_/id/8616896/statistical-column-john-hollinger-exposes-numbers-behind-stats)
- Basketball Reference: [Glossary](https://www.basketball-reference.com/about/glossary.html)

For detailed metric definitions, see [`docs/methodology.md`](./docs/methodology.md)

---

## 👤 Author

**Ming Chuan (Kow Ming Chuan)**
- 📧 Email: mingchuan0909@gmail.com
- 🎓 MSc Business Intelligence & Analytics
- 🏫 Universiti Teknologi Malaysia (UTM)
- 📍 Based in Malaysia

---

## 📝 License

- **Dataset**: Kaggle — [Original License](https://www.kaggle.com/datasets/terms)
- **Dashboard & Code**: MIT License — Free to use, modify, distribute
- **Attribution**: Please credit if you use or modify

---

## 💬 Contributing & Support

**Questions?** Open an issue on GitHub  
**Found a bug?** Create a GitHub issue with details  
**Want to contribute?** Fork → Modify → Pull Request

---

## ⭐ If You Found This Useful...

Please consider:
- ⭐ Starring this repo
- 🔄 Sharing with colleagues
- 💭 Leaving feedback in Issues

---

**Last Updated**: 2026-09-17  
**Power BI Version**: 2.x+  
**Data Refresh**: Weekly
