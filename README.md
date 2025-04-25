# 🏀 NBA Player Performance Pipeline with Snowflake

## Overview
This project demonstrates how to build a scalable ELT pipeline using Snowflake and Python for NBA player performance analysis. Data is sourced from the NBA API and stored in Snowflake for advanced querying and fan engagement insights.

## Features
- Ingest NBA player stats, team rosters, and game logs via `nba_api`
- Load raw + transformed data into Snowflake
- Dimensional modeling: `dim_players`, `dim_teams`, `fact_player_game_stats`
- Analytical queries: top performers, usage rate, trends over time

## Tech Stack
- Python, Pandas, nba_api, Snowflake (with `snowflake-connector-python`), SQL (for data modeling)


## Setup
1. Create Snowflake account + database
2. Pull data via `nba_api`
3. Load to Snowflake via connector or SQLAlchemy
4. Run transformation scripts
