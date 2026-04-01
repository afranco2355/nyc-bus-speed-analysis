# NYC Bus Speed Analysis

Interactive analysis of MTA bus speeds across New York City using 
10 years of open data (2015–present).

## Project Overview
This project explores how fast buses actually move across New York City 
by analyzing over 158,000 records of MTA bus speed data. The analysis 
identifies the slowest and fastest routes, compares performance across 
boroughs, and visualizes the entire bus network on an interactive map 
colored by speed.

## Key Findings
- Manhattan has the slowest buses in the city, averaging under 5 mph
- Staten Island has the fastest buses, running on wider roads with less congestion
- M14A and M42 are the two slowest regular routes in the system
- Buses on the slowest Manhattan routes travel barely faster than walking pace

## What the Project Does
- Loads 158,000 rows of real MTA bus speed data directly from NY Open Data
- Filters out shuttle replacement buses to focus on regular service
- Calculates average speed per route and per borough
- Joins speed data with official MTA route geometries
- Builds an interactive map of all 348 routes colored red to green by speed
- Hovering over any route shows its name and average speed

## Data Sources
- MTA Bus Speeds (2015–present): data.ny.gov
- MTA Bus Route geometries: data.ny.gov

## Tools Used
- Python
- pandas — data cleaning and analysis
- geopandas — geographic data handling
- folium — interactive map
- matplotlib — charts
- Google Colab — development environment

## How to Run
1. Open the notebook in Google Colab
2. Run all cells from top to bottom
3. Data loads automatically from public URLs — no files needed

## Files
- `nyc_bus_speed_analysis.ipynb` — full analysis notebook
- `nyc_bus_speeds_map.html` — interactive route map, download and open in browser
