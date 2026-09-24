# Bryce Young QB Tracker

A Carolina Panthers-themed, browser-based dashboard comparing Bryce Young with every NFL quarterback.

## Data
The page loads current player stats from nflverse's `nflverse-data` releases and aggregates weekly rows into season totals. Bryce Young is highlighted in Panthers blue.

## View on the web
This repo is ready for GitHub Pages. In **Settings → Pages**, choose **Deploy from a branch**, then select **main** and **/(root)**.

The site entry point is `index.html`.

## Features
- Season selector (2023-current)
- Regular/postseason selector
- Search by QB/team
- Sortable QB table
- Bryce Young summary cards and QB ranks
- Passing, rushing, EPA, sacks, air yards, YAC, first downs, and fantasy stats

Data source: https://github.com/nflverse/nflverse-data


## Automatic data refresh
A GitHub Actions workflow downloads nflverse QB statistics every 6 hours and writes browser-friendly JSON files into `data/`. The webpage reads those local files instead of requesting nflverse directly, avoiding browser/CORS issues.
