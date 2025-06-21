
# nflendzoneData

<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
[![License:
CC-BY-4.0](https://img.shields.io/badge/License-CC--BY--4.0-blue.svg)](LICENSE.md)

<!-- badges: end -->

This repository contains automated data releases for `nflendzone`,
published via GitHub Actions and Releases. Download and query data using
R, Python, or other tools.

## 🔧 Usage

- Download manually from the [Releases
  page](https://github.com/TylerPollard410/nflendzoneData/releases).
- Or programmatically in R:

``` r
# Download the latest season_standings data
url <- sprintf("https://github.com/TylerPollard410/nflendzoneData/releases/download/season_standings/season_standings.rds")
download.file(url, "season_standings_latest.rds")
data <- readr::read_rds("season_standings_latest.rds")
```

You can similarly load data in Python or other languages by URL.

## 📊 Automation Status

The table below shows which data sets are available and when they were
last updated:

    #> 
    #> Attaching package: 'dplyr'
    #> The following objects are masked from 'package:stats':
    #> 
    #>     filter, lag
    #> The following objects are masked from 'package:base':
    #> 
    #>     intersect, setdiff, setequal, union

| Dataset | Description | Status | Last Updated |
|:---|:---|:---|:---|
| season_standings | Season standings (by season) | ![season_standings_status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzonePipeline/update_data.yml?label=season_standings&style=flat-square) | [![season_standings_updated](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=updated&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/season_standings/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/season_standings) |
| weekly_standings | Weekly standings | ![weekly_standings_status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzonePipeline/update_data.yml?label=weekly_standings&style=flat-square) | [![weekly_standings_updated](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=updated&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/weekly_standings/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/weekly_standings) |
| elo | ELO ratings by season | ![elo_status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzonePipeline/update_data.yml?label=elo&style=flat-square) | [![elo_updated](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=updated&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/elo/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/elo) |
| srs | SRS ratings by season | ![srs_status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzonePipeline/update_data.yml?label=srs&style=flat-square) | [![srs_updated](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=updated&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/srs/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/srs) |
| epa | Season EPA summaries | ![epa_status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzonePipeline/update_data.yml?label=epa&style=flat-square) | [![epa_updated](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=updated&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/epa/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/epa) |
| scores | Game scores (all years) | ![scores_status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzonePipeline/update_data.yml?label=scores&style=flat-square) | [![scores_updated](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=updated&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/scores/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/scores) |
| series | Series-level summaries | ![series_status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzonePipeline/update_data.yml?label=series&style=flat-square) | [![series_updated](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=updated&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/series/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/series) |
| turnover | Turnover stats | ![turnover_status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzonePipeline/update_data.yml?label=turnover&style=flat-square) | [![turnover_updated](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=updated&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/turnover/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/turnover) |
| redzone | Red zone efficiency | ![redzone_status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzonePipeline/update_data.yml?label=redzone&style=flat-square) | [![redzone_updated](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=updated&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/redzone/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/redzone) |
| model_data_long | Long-form model data | ![model_data_long_status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzonePipeline/update_data.yml?label=model_data_long&style=flat-square) | [![model_data_long_updated](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=updated&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/model_data_long/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/model_data_long) |
| model_data | Model-ready dataset | ![model_data_status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzonePipeline/update_data.yml?label=model_data&style=flat-square) | [![model_data_updated](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=updated&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/model_data/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/model_data) |

Automation status for nflendzone data releases.

## About the Data

| Tag                | Description                             |
|--------------------|-----------------------------------------|
| `season_standings` | Finalised standings for each NFL season |
| `weekly_standings` | Standings updated weekly                |
| `elo`              | Season-by-season ELO ratings            |
| `srs`              | Season-by-season SRS ratings            |
| `epa`              | Season expected points added summaries  |
| `scores`           | Game-level scores across all seasons    |
| `series`           | Head-to-head series stats               |
| `turnover`         | Turnovers by team/season                |
| `redzone`          | Red-zone efficiency metrics             |
| `model_data_long`  | Long-form dataset ready for modeling    |
| `model_data`       | Compact model-ready dataset             |

*(Update or expand description as needed.)*

## 🗓️ Update Schedule

Data updates are triggered daily at 4 AM Eastern during the NFL season
(September–February) via GitHub Actions in the `nflendzonePipeline`
repo.

## ⚖️ License

All data is released under [CC‑BY‑4.0](LICENSE.md). If you use this
data, please cite the repository and include a link to the corresponding
release tag.
