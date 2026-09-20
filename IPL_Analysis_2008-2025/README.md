# 🏏 IPL Analysis Dashboard (2008 – 2025) | Power BI

An interactive, end-to-end **Power BI** analytics dashboard exploring 18 seasons of the **Indian Premier League (IPL)** from its inaugural season in 2008 through 2025.

---

## 📊 Dashboard Overview

This dashboard delivers an executive-level summary and granular analytical insights for every IPL season. Users can dynamically filter by any season to evaluate team standings, champion/runner-up outcomes, tournament-wide batting and bowling milestones, individual player accolades, and boundary counts.

---

## 🌟 Key Features & Visual Insights

### 1. 🏆 Tournament Champions & Finalists
- **Season Winner**: Displays the champion franchise name along with the official team logo.
- **Runner-Up**: Displays the finalist franchise name and logo.

### 2. 📈 Key Performance Indicators (KPIs)
- **Total Matches Played** (1,169+ matches analyzed across 18 seasons)
- **Total Participating Teams**
- **Total Venues Hosted**
- **Total Sixes & Fours** hit in the season
- **Milestones**: Season total **Centuries (100s)** and **Half-Centuries (50s)**

### 3. 🎖️ Individual Player Accolades
- **🟠 Orange Cap Holder**:
  - Top run-scorer of the selected season
  - Total runs scored, team affiliation, and player headshot
- **🟣 Purple Cap Holder**:
  - Leading wicket-taker of the selected season
  - Total wickets taken, team affiliation, and player headshot
- **💥 Boundary Kings**:
  - Player with the **Most Fours (4s)** in the season
  - Player with the **Most Sixes (6s)** in the season

### 4. 📋 Season Points Table & Standings
- Complete standings table featuring:
  - Franchise official logo & team name
  - Matches Played (P)
  - Matches Won (W)
  - Matches Lost (L)
  - Matches Tied / No Result (NR)
  - Total Points earned

### 5. 🎛️ Interactive Season Slicer
- A single-select / multi-select slicer allowing immediate recalculation of all KPIs, visuals, accolades, and standings for any season from **2008 to 2025**.

---

## 📂 Project Structure

```text
IPL_Analysis_2008-2025/
├── .gitignore                      # Git ignore rules for Power BI & temporary files
├── IPL_ANALYSIS(2008-2025).pbix    # Main Power BI Report file
├── README.md                       # Project documentation
├── IPL Data/                       # Datasets used in the data model
│   ├── ipl_matches_data.csv        # Match metadata, results, toss, venues (2008-2025)
│   ├── ball_by_ball_data.csv       # Ball-by-ball delivery-level records
│   ├── players-data-updated.csv    # Player profiles, batting/bowling style & image URLs
│   └── teams_data.csv              # Team names, short codes & official logo URLs
└── Images Used/                    # Visual assets, caps, badges & social logos
    ├── Orange Cap.png
    ├── Purple Cap.png
    ├── tata_ipl-logo_brandlogos.net_k2ryd (1).png
    ├── Cricbuzz-Logo.png
    └── ...
```

---

## 🗄️ Dataset Details

| Dataset | Records | Description |
| :--- | :--- | :--- |
| **`ipl_matches_data.csv`** | 1,169 matches | Comprehensive match summaries including season, teams, toss decisions, winner, margin of victory, player of the match, and venue. |
| **`ball_by_ball_data.csv`** | 260,000+ balls | Granular ball-by-ball logs containing batsman, bowler, runs scored, extra runs, dismissals, and dismissal types. |
| **`players-data-updated.csv`** | 700+ players | Master player list with player full name, playing styles (batting/bowling), and official image CDN URLs. |
| **`teams_data.csv`** | 15+ franchises | Franchise reference table with standard team names, abbreviations, and verified logo image URLs. |

---

## 🧮 Data Model & DAX Measures

The project employs a star/snowflake schema relating matches, deliveries, players, and teams:
- Relationships established between `ipl_matches_data` and dimension tables `teams_data` and `players-data-updated`.
- Measures calculated for dynamic KPI cards:
  - Season Champion & Runner-Up detection based on playoff/final stages.
  - Orange Cap runs aggregation and leading batsman lookup.
  - Purple Cap wickets aggregation and leading bowler lookup.
  - Boundary metrics (`Total 4's`, `Total 6's`, player boundary distribution).
  - Points table calculation (`Win * 2`, `No Result * 1`).

---

## 🚀 How to Open and Explore

1. **Prerequisites**: Install [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).
2. **Clone the Repository**:
   ```bash
   git clone https://github.com/irfan-shekh/Power_BI_Projects.git
   ```
3. **Open the Report**:
   - Double click on `IPL_Analysis_2008-2025/IPL_ANALYSIS(2008-2025).pbix`.
4. **Update Data Source Paths** *(if prompted)*:
   - In Power BI Desktop, click **Transform Data** > **Data Source Settings**.
   - Point the file paths to the local `IPL Data/` folder if prompted.
   - Click **Apply Changes**.

---

## 👤 Author

- **Irfan Shekh** – [GitHub Profile](https://github.com/irfan-shekh)
