# CDC Sleep Duration and Health Analysis

**Project Title:** Relationship Between Sleep Duration and Health Outcomes in the U.S.  
**Author:** Yashkirat Singh  
**Date:** May 2025 - July 2025
**Repository:** cdc-sleep-duration-health-analysis
**Tools:** Python · Pandas · NumPy · Matplotlib · Plotly · BeautifulSoup · Requests

---

## Overview

This repository contains data, Jupyter notebooks, reports, and visualizations from a project that explores the relationship between sleep duration and both mental and physical health outcomes in the United States. The data was obtained from the Centers for Disease Control and Prevention (CDC) and includes the 2022 Behavioral Risk Factor Surveillance System (BRFSS) survey dataset, the CDC BRFSS Codebook (HTML), and the CDC Chronic Disease Indicators API (JSON). The goal of this project was to identify patterns linking sleep duration to variables such as depression, obesity, BMI, and education level in order to visualize how these trends vary across the U.S.

---

## Repository Structure
```
cdc-sleep-duration-health-analysis/
├─ data/
│  ├─ raw/ # placeholder for large raw CDC BRFSS data (not tracked)
│  │  └─ README.md
│  └─ processed/ # cleaned datasets used in analysis
│     ├─ cleaned_brfss_data.csv
│     ├─ cleaned_json_data.csv
│     └─ parsed_codebook_data.csv
│
├─ notebooks/ # Jupyter notebooks with code for cleaning and analysis
│  ├─ 02_data_cleaning.ipynb
│  └─ 03_data_analysis_and_visualization.ipynb
│
├─ reports/ # summary and presentation materials
│  ├─ One-Pager.pdf
│  └─ Slide_Deck.pdf
│
├─ visuals/ # exported graphs and figures
│  ├─ visualization1.png
│  ├─ visualization2.png
│  └─ visualization3.png
│
├─ requirements.txt
├─ .gitignore
└─ README.md
```
---

## Data Sources

All datasets were obtained from the Centers for Disease Control and Prevention (CDC):

| Source | Format | Description |
|---------|---------|-------------|
| [Behavioral Risk Factor Surveillance System (BRFSS) 2022](https://www.cdc.gov/brfss/annual_data/2022/files/LLCP2022ASC.zip) | Fixed-width text | Individual survey responses on health behaviors, such as sleep duration, BMI, and mental health. |
| [CDC BRFSS Codebook](https://www.cdc.gov/brfss/annual_data/2022/zip/codebook22_llcp-v2-508.zip) | HTML | Metadata to parse and interpret codes from the BRFSS dataset. |
| [CDC Chronic Disease Indicators](https://data.cdc.gov/resource/hksd-2xuw.json) | JSON API | State-level health and sleep statistics. |

> Note: The raw BRFSS data (~900MB) is not included in this repository due to file size and licensing. Instructions for obtaining it are provided in `data/raw/README.md`.

---

## Methods

- Parsed and cleaned the 2022 BRFSS text file using `pandas.read_fwf()` with selected columns.  
- Used BeautifulSoup to scrape the HTML codebook and interpret coded variables.  
- Retrieved state-level data from the CDC Chronic Disease Indicators API using `requests`.  
- Cleaned and merged datasets in Pandas, handling missing or invalid codes (e.g., 77, 99).  
- Conducted analysis and built visualizations using Matplotlib and Plotly to identify trends.

---

## Key Insights

1. Sleep & Mental Health: Adults sleeping 7–8 hours per night reported the fewest mentally unhealthy days on average.  
2. Education: Short sleep (<6 hours) follows a U-shaped pattern, peaking among those with some high school education.  
3. Income: Sleep duration rises slightly with income, plateauing after $20,000 per year.  
4. BMI: Higher BMI values correspond to slightly shorter sleep durations.  
5. Geography: Short sleep was most prevalent in the Southeast and Ohio River Valley, with Hawaii also among the highest.

---

## Future Improvements

- Incorporate multivariable models to examine multiple variables simultaneously.  
- Apply survey weighting to make national estimates more representative.  

---

*This repository contains all final data, analyses, and figures from the project.*  
*For inquiries, contact Yashkirat Singh at yashksingh43@gmail.com.*
