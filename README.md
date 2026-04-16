# NYC Bus Speed Analysis

Interactive analysis of MTA bus speeds across New York City using 
10 years of open data (2015–present).

## Project Overview
This project explores how fast buses actually move across New York City 
by analyzing over 158,000 records of MTA bus speed data. The analysis 
identifies the slowest and fastest routes, compares performance across 
boroughs, examines how speeds changed over time including during COVID-19, 
and visualizes the entire bus network on an interactive map colored by speed.

## Key Findings
- Manhattan has the slowest buses in the city, averaging under 5 mph
- Staten Island has the fastest buses, running on wider roads with less congestion
- M14A and M42 are the two slowest regular routes in the system
- Buses on the slowest Manhattan routes travel barely faster than walking pace
- Bus speeds increased noticeably during 2020 COVID lockdowns as traffic disappeared, 
  then declined again as the city reopened
- The B44 route in Brooklyn tracked the citywide speed decline despite camera 
  enforcement deployment in 2019 and Hayden AI ABLE camera installation in 2022, 
  suggesting broader congestion trends offset enforcement gains at the route level
- The 10 slowest peak-hour routes show minimal speed difference between peak and 
  off-peak periods, suggesting structural factors rather than congestion are the 
  primary cause of slowness on these corridors

## What the Project Does
- Loads 158,000 rows of real MTA bus speed data directly from NY Open Data
- Filters out shuttle replacement buses to focus on regular service
- Calculates average speed per route and per borough
- Analyzes speed trends across 10 years with COVID-19 and Hayden AI deployment markers
- Examines the B44 route specifically against the citywide average
- Compares peak vs off-peak speeds for the slowest routes
- Joins speed data with official MTA route geometries
- Builds an interactive map of all 348 routes colored red to green by speed
- Hovering over any route shows its name, description and average speed

## Key Insight for Transit Policy
The narrow gap between peak and off-peak speeds on the slowest routes suggests 
that for these corridors, bus lane enforcement alone may not dramatically improve 
speeds — structural factors like stop density, signal timing, and street geometry 
play an equal or greater role. This points to the need for complementary 
interventions alongside enforcement.

## Data Sources
- MTA Bus Speeds (2015–present): data.ny.gov/Transportation/MTA-Bus-Speeds-Beginning-2015/cudb-vcni
- MTA Bus Route geometries: data.ny.gov/Transportation/MTA-Bus-Routes/bzwk-3hb4

## Tools Used
- Python
- pandas — data cleaning and analysis
- geopandas — geographic data handling
- folium — interactive map
- plotly — interactive charts
- branca — map color scale
- Google Colab — development environment

## How to Run
1. Open the notebook in Google Colab
2. Run all cells from top to bottom
3. Data loads automatically from public URLs — no files needed

## Files
- `nyc_bus_speed_analysis.ipynb` — full analysis notebook
- `nyc_bus_speeds_map.html` — interactive route map, download and open in browser
