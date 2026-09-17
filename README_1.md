# NBA Player Performance & Fatigue Dashboard

Interactive Power BI dashboards analyzing NBA player performance metrics and fatigue trends.

## 📊 Overview

This project contains two interconnected Power BI dashboards:

1. **NBA Player Performance Overview** — Comprehensive view of player stats (PTS, TRB, AST, GmSc) with player style classification (All-Around, Defender, Playmaker, Rebounder)
2. **NBA Player Fatigue Dashboard** — Tracks player fatigue index and its correlation with performance metrics

## 📦 Data Source

- **Dataset**: [NBA Player Stats](https://www.kaggle.com/datasets/) (Kaggle)
- **Season**: 2024-2025
- **Format**: CSV / Excel
- **License**: [Dataset License](https://www.kaggle.com/datasets/terms)

## 🎯 Key Metrics

| Metric | Description |
|--------|-------------|
| **PTS** | Points per game |
| **TRB** | Total rebounds per game |
| **AST** | Assists per game |
| **GmSc** | Game Score (composite efficiency metric) |
| **FatigueRisk** | Player fatigue classification (High/Moderate/Low) |

## 🖥️ Dashboard Features

### Performance Overview
- 🏀 Team selector (30 NBA teams)
- 👥 Player comparison across 4 play styles
- 📈 Performance trend analysis over time
- 📊 Key stat cards with averages

### Fatigue Analysis
- 📉 Fatigue trend line chart
- 🔍 Performance vs. Fatigue scatter plot (GmSc correlation)
- ⚠️ Player fatigue risk classification
- 🗓️ Time-period and team filtering

## 🚀 How to Use

1. Download the `.pbix` file from this repository
2. Open in **Power BI Desktop** ([free version](https://powerbi.microsoft.com/en-us/desktop/))
3. Refresh data connection (File → Options → Data Source Settings)
4. Use slicers to explore by:
   - Team
   - Time period (Year/Quarter/Month)
   - Player name

## 📁 Project Structure

```
nba-dashboard/
├── README.md                          # This file
├── NBA_Performance_Dashboard.pbix      # Main Power BI workbook
├── NBA_Fatigue_Dashboard.pbix         # Fatigue analysis dashboard
├── data/
│   └── nba_player_stats.csv           # Source data from Kaggle
└── docs/
    └── methodology.md                  # Metric definitions & calculations
```

## 🛠️ Technical Stack

- **Tool**: Power BI Desktop
- **Data Source**: Kaggle CSV
- **Visualizations**: 
  - Bar charts (team comparison)
  - Line charts (trend analysis)
  - Scatter plots (correlation analysis)
  - KPI cards (key metrics)
  - Hierarchical slicers (date, team, player)

## 📊 Metric Definitions

### Game Score (GmSc)
Composite efficiency metric combining scoring, rebounds, assists, and efficiency:
```
GmSc = PTS + 0.4×FG - 0.7×FGA - 0.4×FTA + 0.7×ORB + 0.3×DRB + STL + 0.7×AST + 0.7×BLK - 0.4×PF - TOV
```

### Fatigue Risk Score
Based on minutes played, back-to-back games, and performance consistency.

## 🔮 Future Enhancements

- [ ] Add advanced stats (TS%, Usage%, PER — Player Efficiency Rating)
- [ ] Implement predictive fatigue modeling (regression analysis)
- [ ] Connect to live NBA API for real-time updates
- [ ] Add injury/absence correlation analysis
- [ ] Player salary cap analysis integration
- [ ] Team strength of schedule visualization

## 👤 Author

**Ming Chuan (Kow Ming Chuan)**  
📧 mingchuan0909@gmail.com  
🎓 MSc Business Intelligence & Analytics, Universiti Teknologi Malaysia (UTM)

## 📝 License

This project uses data from Kaggle. Please respect the original dataset's license terms.

For the dashboard and documentation: [Choose MIT / CC0 / CC-BY-4.0]

---

**Have questions or found a bug?**  
✉️ Open an issue or reach out!  
⭐ If you found this useful, please star the repo!
