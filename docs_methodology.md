# Methodology & Metric Definitions

## Player Performance Metrics

### Basic Stats
- **PTS (Points)** — Total points scored per game
- **TRB (Total Rebounds)** — Offensive + Defensive rebounds per game
- **AST (Assists)** — Player passes leading to made baskets per game
- **FG** — Field Goals made
- **FGA** — Field Goals attempted
- **3P%** — Three-point percentage

### Efficiency Metrics

#### Game Score (GmSc)
A composite metric that estimates points produced by a player:

```
GmSc = PTS + 0.4×FG - 0.7×FGA - 0.4×FTA + 0.7×ORB + 0.3×DRB + STL + 0.7×AST + 0.7×BLK - 0.4×PF - TOV
```

**Interpretation**: Higher GmSc indicates better overall efficiency and contribution.

#### Player Efficiency Rating (PER)
Estimates overall productivity per minute played (advanced stat).

## Player Style Classification

Players are categorized into 4 main archetypes:

| Style | Characteristics | Key Metrics |
|-------|-----------------|------------|
| **All-Around** | Balanced scorers and playmakers | High PTS & AST |
| **Defender** | Defensive specialists | High STL, BLK, Lower PTS |
| **Playmaker** | Assist-heavy players | High AST, Lower PTS/TRB |
| **Rebounder** | Board dominators | High TRB, Moderate PTS |

## Fatigue Analysis

### Fatigue Risk Score
Combines multiple factors to assess player fatigue:

1. **Workload** — Minutes played (% of team)
2. **Game Frequency** — Back-to-back games indicator
3. **Performance Consistency** — Variation in GmSc across recent games
4. **Season Progression** — Cumulative minutes / fatigue accumulation

### Fatigue Risk Categories
- **High** — Fatigue score > 75th percentile (likely to underperform)
- **Moderate** — 25th-75th percentile (normal range)
- **Low** — Fatigue score < 25th percentile (fresh, high performance potential)

## Dashboard Calculations

### Performance Trend Over Time
Shows rolling averages of GmSc and PTS across the season:
- **Blue line** — GmSc (smoothed over 5-game rolling window)
- **Orange line** — PTS (smoothed over 5-game rolling window)

### Performance vs. Fatigue Scatter
X-axis: GmSc (average)  
Y-axis: Player Overall Contribution (PER estimate)  
Point color: Fatigue Risk (High/Moderate/Low)

**Insight**: Points in the upper-right quadrant represent high performers with low fatigue.

## Data Quality Notes

- **Missing Values** — Handled by forward-fill or team average imputation
- **Outliers** — Extreme performances kept (represent actual performance variance)
- **Season Updates** — Dashboard updated weekly via Kaggle dataset refresh

## Limitations

1. **Sample Size** — Early season data (first 5 games) may be unstable
2. **Injuries** — Fatigue doesn't account for injury history
3. **Rest Days** — All-Star breaks and scheduled rest not explicitly modeled
4. **Team Context** — Individual stats don't account for team chemistry

## References

- [Basketball Reference Glossary](https://www.basketball-reference.com/about/glossary.html)
- Game Score formula from [John Hollinger](https://www.espn.com/nba/story/_/id/8616896/statistical-column-john-hollinger-exposes-numbers-behind-stats)
- PER research: Basketball Reference advanced stats documentation
