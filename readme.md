# League of Legends Worlds 2026 Analysis

Analysis of the **2026 League of Legends World Championship** using match data from **Oracle's Elixir**.

The project focuses on the Worlds **Swiss Stage and subsequent matches**, with the goal of analyzing game-level, team-level, and player-level performance.

## Project Structure

```text
League_Of_Legends_Herald_Analysis/
│
├── data/
│   ├── raw/
│   │   └── 2026_LoL_esports_match_data_from_OraclesElixir.csv
│   │
│   └── processed/
│       └── worlds_swiss_onward.csv
│
├── notebooks/
│   └── 01_prepare_worlds_data.ipynb
│
└── README.md
```

## Data Source

The primary data source is the publicly available **Oracle's Elixir 2026 League of Legends match dataset**.

The raw CSV is stored in:

```text
data/raw/
```

The original raw dataset is preserved and is not modified by the analysis.

## Dataset Preparation

The current data preparation pipeline is contained in:

```text
notebooks/01_prepare_worlds_data.ipynb
```

The notebook:

1. Loads the Oracle's Elixir 2026 match dataset.
2. Filters the dataset to the 2026 Worlds competition using the `WLDs` league code.
3. Converts match dates to a usable datetime format.
4. Identifies **October 23, 2026** as the beginning of the Worlds Swiss Stage.
5. Excludes the earlier Worlds Play-In matches.
6. Retains the Swiss Stage and all subsequent Worlds matches.
7. Validates the resulting dataset.
8. Saves the processed dataset to `data/processed/`.

### Current Dataset

The resulting dataset contains:

- **72 unique games**
- Player-level records
- Team-level records
- Original Oracle's Elixir match statistics
- Swiss Stage and subsequent Worlds matches

The processed dataset is:

```text
data/processed/worlds_swiss_onward.csv
```

The first Swiss Stage match was **Gen.G vs. Invictus Gaming** on **October 23, 2026**, played on patch **16.20**.

## Analysis Plan

The processed dataset will serve as the foundation for subsequent analysis of the Worlds tournament.

Potential areas of analysis include:

- Team performance
- Player performance
- Champion selections and bans
- Draft patterns
- Game duration
- Objectives and map control
- Gold and experience differences
- Herald-related performance
- Team and player trends across the tournament
- Statistical relationships between in-game events and match outcomes

Additional notebooks will be added as the analysis develops.

## Data Philosophy

The project separates **raw data preparation** from **analysis**.

```text
Oracle's Elixir Raw Data
        │
        ▼
01_prepare_worlds_data.ipynb
        │
        ▼
worlds_swiss_onward.csv
        │
        ▼
Future Analysis
```

The raw Oracle's Elixir dataset should remain unchanged. Analytical transformations should be performed on copies or derived datasets.

## Previous Data Collection Approach

The project originally explored collecting individual match data from **Gol.gg** through web scraping and API-based requests.

That approach has been discontinued.

The project now uses the Oracle's Elixir match dataset as its primary and direct data source. The previous scraping code and downloaded HTML files are no longer part of the active analysis pipeline.

## Environment

The analysis is written in Python and primarily uses:

- Python
- pandas
- Jupyter Notebook
- pathlib

Additional libraries will be added as needed for statistical analysis, visualization, and modeling.