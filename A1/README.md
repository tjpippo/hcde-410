#HCDE410
Files for HCDE410 - Assignment A1

Adapted from # cdsw-2020 https://wiki.communitydata.science/Seattle_open_data
A README.md in your A1 folder. Use this template:

# A1 — Working with Open Data

**Dataset:** Burke-Gilman Trail north of NE 70th St Bicycle and Pedestrian Counter
**Source:** https://data.seattle.gov/Transportation/Burke-Gilman-Trail-north-of-NE-70th-St-Bicycle-and/2z5v-ecg8 (pulled 2026-10-13 via the API endpoint `https://data.seattle.gov/resource/2z5v-ecg8.json`)
**License / terms of use:** The dataset page lists its license as Public Domain, with attribution to the City of Seattle. Anyone may use, modify, and share it; I credit the City of Seattle as the source.

## Questions I asked
- Q1. When is the trail busiest, and when is it quietest?
- Q2. Do cyclists and pedestrians use the trail at different times of day?
- Q3. Is there evidence people use the trail to commute, not just for recreation? (weekdays vs. weekends)
- Q4. Does traffic flow mostly one direction in the morning and the other in the evening?

## How to re-run
Open `A1.ipynb` and run all cells (needs `requests`, `pandas`, `matplotlib`).

## AI Use 
- I used claude code to help me plot out the data needed to answer the question
- by giving the AI the dataset and then say what variable I need and what i need to see in the graph
- with some modifications of the prompt I got the result and the insight I wanted 