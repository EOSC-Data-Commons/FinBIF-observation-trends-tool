# Observation Map - Multi-Species Analysis

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/EOSC-Data-Commons/FinBIF-observation-trends-tool/HEAD)
[![Replay](https://img.shields.io/badge/launch-EGI%20Replay-F5A252.svg)](https://replay.notebooks.egi.eu/v2/gh/EOSC-Data-Commons/FinBIF-observation-trends-tool/HEAD)

A Python notebook that analyzes the 5 most common species from FinBIF/GBIF Darwin Core Archives, showing their and geographic distribution.

## Overview

This tool helps you understand biodiversity patterns by:
- Downloading FinBIF occurrence data from Darwin Core Archive URLs
- Mapping species geographic distribution with color-coded species

## Requirements

- Python 3.x
- pandas
- numpy
- requests
- matplotlib
- geopandas
- shapely

Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

1. Open `observation_trends.ipynb` in Jupyter or VS Code
2. In **Step 2**, update the `collection_id` to your desired FinBIF collection
   - Find collection IDs at https://laji.fi/en/theme/dataset-metadata . NOTE: Not all collections are available from DwC archive. You can find available collections from [https://gbif.laji.fi/list](https://gbif.laji.fi/list).
3. Run all cells in sequence
4. Occurrence distribution map is generated with different colors for species

## Notes

- Only records with valid geographic coordinates are displayed on the map
- The 5 most common species are selected by total observation count
- Works with any FinBIF collection that provides occurrence data with species and coordinate information AND is shared with GBIF
