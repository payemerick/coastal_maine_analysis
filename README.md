# Warming Ocean Temperatures in the Gulf of Maine and Impacts on Cold-Water Fish and Migratory Sea Birds
*Capstone project for the YSE Environmental Data Science Certificate.*
*Author: Payton Emerick · Last updated: Nov 2026*
## Project description
The Gulf of Maine is located in the Atlantic Ocean in the Northeast United States, from Massachusetts to Nova Scotia. The Gulf of Maine is warming at a rate 99% faster than the global oceans due to shifting ocean currents, unique underwater geography, and climate change. Various marine species call this ecosystem home, including cold-water fish such as herring, hake, and sand lance. Many seabird species rely on these cold-water fish for food sources during migratory and breeding seasons. This project explores ocean temperature trends in this region and the impact it has on cold-water fish species capture during seasonal trawl surveys and citizen science sitings of seabirds. 
## Research question
**How has ocean warming in the Gulf of Maine since 2000 altered the distribution and abundance of cold-water forage fish, and how have those changes affected the population size, body condition, and nesting success of migratory seabirds?**
## Data
| File | Description | Source |
|------|-------------|--------|
| `MaineDMR_Trawl_Survey_Tow_Data_2026-11-18.csv` | Seasonal Trawl Survey Tow Data with water temperature and coordinate data in latitude and longitude, one row per trawl. | Maine Department of Marine Resources, https://www.maine.gov/dmr/science/ecology-environment/inshore-trawl-survey —
downloaded 11.18.2026 |
| `MaineDMR_Trawl_Survey_Catch_at_Length_Data_2026-11-18.csv` | Seasonal Trawl Survey data with the frequency and length of fish species observed during each trawl event, one row per observation | [Maine Department of Marine Resources, https://www.maine.gov/dmr/science/ecology-environment/inshore-trawl-survey —
downloaded 11.18.2026 |
## Repository structure
```
stream_temp_project/
├── README.md ← you are here
└── scripts/ ← notebooks, numbered in the order they run
├── 0_project_setup.ipynb
└── 1_data_cleaning.ipynb
```
## How to run the code
All scripts are Google Colab notebooks written in R. Run them in number order:
1. `scripts/0_project_setup.ipynb` creates the project folder and subfolders in
Google Drive.
2. `scripts/1_data_cleaning.ipynb` reads both raw files, reshapes and summarizes, and
writes `clean_data/catch_length_filtered.csv` and `clean_data/catch_length_summary.csv`.
## Data cleaning steps (`1_data_clean.ipynb`)
1. **Cleaned the Catch at Length Data** with `filter()`. The Catch at Length data had every fish species observed in the Gulf during each trawl from 2000. Since this project is only interested in 3 fish species, I filtered out everything but the 3 species.
2. **Summarized Catch at Length data** by average length, average frequency, and total frequency per species to ensure there was data for each species.
## Status and next steps
- [x] Set up the project folder and GitHub repository
- [x] Clean and combine the raw data <- in this stage currently.
- [ ] Exploratory plots: temperature by year, fish length size by year, bird sitings by year, mapping the data.
- [ ] Compare temperature, fish, and bird trends.
