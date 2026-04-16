# NYC Bus Speed Analysis

Interactive analysis of MTA bus speeds across New York City using 10 years 
of open data (2015–present).

## Project Overview
This project explores how fast buses actually move across New York City by 
analyzing over 158,000 records of MTA bus speed data. The analysis identifies 
the slowest and fastest routes, compares performance across boroughs, examines 
how speeds changed over time, and visualizes the entire bus network on an 
interactive map colored by speed.

## Key Findings

**The slowest buses in NYC barely move faster than walking pace.** The M14A 
and M42 are the two slowest regular routes in the system, averaging under 
4.8 mph. Most of the 10 slowest routes are Manhattan crosstown routes, where 
dense traffic, frequent stops, and short block lengths combine to create 
chronic slowness regardless of time of day.

**Manhattan is the slowest borough, Staten Island the fastest.** Manhattan 
buses average under 5 mph while Staten Island buses move significantly faster, 
benefiting from wider roads, fewer stops, and lower traffic density. The 
difference reflects how street geometry shapes bus performance as much as 
traffic volume does.

**COVID-19 revealed how much traffic slows buses.** Bus speeds increased 
noticeably in 2020 as lockdowns emptied city streets, then declined again as 
the city reopened and congestion returned. This confirms that traffic is a 
primary driver of bus slowness across the network.

**Camera enforcement improved speeds but did not reverse the long term decline.**
The MTA began automated bus lane camera enforcement in 2019, and Hayden AI 
deployed its ABLE camera systems on MTA buses starting in 2022. Analysis of 
the B44 route in Brooklyn — one of the first enforcement corridors — shows 
speeds tracking the citywide decline despite enforcement, suggesting broader 
congestion trends offset the gains from camera enforcement at the route level.

**Structural factors matter as much as congestion.** The 10 slowest peak-hour 
routes show a surprisingly narrow speed difference between rush hour and 
off-peak periods. This suggests that for the slowest corridors, the bottleneck 
is not primarily congestion but rather structural factors like stop density, 
signal timing, and street geometry — pointing to the need for interventions 
beyond bus lane enforcement alone.

## Data Sources
MTA Bus Speeds (2015–present) and MTA Bus Route geometries are both published 
on data.ny.gov as part of the MTA Open Data Program.

## Tools Used
Python, pandas, geopandas, folium, plotly, and Google Colab.

## How to Run
Open the notebook in Google Colab and run all cells from top to bottom. 
All data loads automatically from public URLs — no files need to be downloaded.

## Files
`nyc_bus_speed_analysis.ipynb` contains the full analysis notebook.
`nyc_bus_speeds_map.html` is the interactive route map — download and open 
in any browser to explore all 348 routes colored by average speed.
