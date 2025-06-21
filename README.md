
# nflendzoneData

<!-- badges: start -->

<!-- badges: end -->

This repository holds automated data releases for the `mydata` project
(all data is published via GitHub Actions and GitHub Releases).

## Usage

You can download data hosted here directly from the [releases
page](https://github.com/TyleerPollard410/nflendzoneData/releases) or
programmatically via your own R functions.

## Automation Status

The following table shows the current status and last update of all
automated data releases.

| Dataset | Description | Status | Last Updated |
|:---|:---|:---|:---|
| scores | Game scores (all years) | ![status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzoneData/update_scores.yml?label=scores_status&style=flat-square) | [![scores](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=last_updated&style=flat-square&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/scores/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/scores) |
| standings | Season standings | ![status](https://img.shields.io/github/actions/workflow/status/TylerPollard410/nflendzoneData/update_standings.yml?label=standings_status&style=flat-square) | [![standings](https://img.shields.io/badge/dynamic/json?color=blue&label=Last%20Updated&query=last_updated&style=flat-square&url=https://github.com/TylerPollard410/nflendzoneData/releases/download/standings/timestamp.json)](https://github.com/TylerPollard410/nflendzoneData/releases/tag/standings) |

Automation status of all data releases. Click the ‘Last Updated’ badge
to view the release for each dataset.

------------------------------------------------------------------------

## About Each Data Release

- **scores:** Contains final and in-progress scores for every game
  since 2006. *Data release*: The `.parquet` and `.rds` files are
  updated weekly during the season and after each round of games.
- **standings:** Aggregated standings, win/loss/tie records by season
  and division. *Data release*: Standings are updated every week after
  all games have concluded.

<!-- Repeat or update for each of your tags/datasets. Update the captions above as needed for each tag. -->

------------------------------------------------------------------------

## How to Customize Tag Captions

In the status table code chunk, edit the `caption` for each tag to
briefly explain what’s in that dataset/tag, e.g.:

- `"scores", "Game scores (all years)", ...`
- `"model_predictions", "Model output and forecasts", ...`
- `"weekly_props", "Player prop data, weekly", ...`

Use a clear, concise phrase. **The best captions:**

- Identify data type, granularity, or special purpose (e.g.,
  “Full-season EPA summaries” or “Play-by-play with advanced metrics”).

------------------------------------------------------------------------

## Programmatic Access Example (optional)

``` r
# Example R code to download the latest scores file:
download.file(
  url = "https://github.com/TylerPollard410/nflendzoneData/releases/download/scores/scores_2024.rds",
  destfile = "scores_2024.rds"
)
```

------------------------------------------------------------------------

# License

Data and code in this repo are released under the MIT License (or
specify your own license).
