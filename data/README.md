# Data directory

This project uses one team-season as its primary analytical unit.

- `raw/` contains unchanged downloaded source data. Files here are immutable and must never be edited in place.
- `processed/game_level/` contains cleaned individual-game tables used for aggregation and verification.
- `processed/team_season/` contains the main one-row-per-team-season study inputs.
- `processed/analysis/` will contain joined modeling and dashboard datasets.
- `reference/` contains lookups, samples, source workbooks, and supporting documentation.
- `qa/` contains validation results.
- `archive/` contains superseded versions retained for recovery.

Only files under `processed/` should normally be loaded into the final analysis and dashboard.

## Main team-season inputs

- `processed/team_season/nfl_regular_team_seasons_1995_2025.csv`
- `processed/team_season/nfl_preseason_team_seasons_1995_2025.csv` (future canonical output)
- `processed/team_season/nfl_team_season_outcomes_1995_2025.csv` (pending export from the reference workbook)

## Reserved future canonical files

These files will be produced later; no empty placeholders are stored in the project.

- `processed/game_level/nfl_preseason_games_1995_2025.csv`
- `processed/team_season/nfl_preseason_team_seasons_1995_2025.csv`
- `processed/analysis/nfl_preseason_regular_analysis_1995_2025.csv`

The final analysis table will contain one row per team-season with preseason results, regular-season results, division finish, playoff qualification, and Super Bowl outcome.
