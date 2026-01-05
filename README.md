# IBM Data Science Capstone — SpaceX Falcon 9 Landing Prediction

## Project Overview

This repository contains my **IBM Data Science Professional Certificate Capstone Project**.

The goal of this project is to analyze historical **SpaceX Falcon 9** launch data and build predictive models to determine whether the **first stage successfully lands and can be reused**.

First-stage reusability is a critical factor in reducing launch costs. Accurately predicting landing success provides valuable insights for cost estimation, operational planning, and competitive benchmarking within the commercial space industry.

---

## Project Scope

This project follows an end-to-end data science workflow, progressing from raw data collection to predictive modeling and data-driven insights.

At the current stage, the project covers:

- Data collection (API and web scraping)
- Data wrangling and preprocessing
- Exploratory Data Analysis (EDA)
- Interactive visual analytics

---

## Repository Structure

```
ibm-datascience-capstone-spacex/
│
├─ data/
│ └─ raw/
│   ├─  spacex_launch_geo.csv
│   ├─  spacex_launch_dash.csv
│   └─  spacex.csv
│
│ └─ processed/
│   ├─  dataset_part_1.csv
│   ├─  dataset_part_2.csv
│   ├─  dataset_part_3.csv
│   └─  spacex_web_scraped.csv
│
├─ notebooks/
│ ├─ 01.Data_collection_API_Lab.ipynb
│ ├─ 02.Data_collection_Web_Scraping_Lab.ipynb
│ ├─ 03.Data_Wrangling.ipynb
│ ├─ 04.EDA_with_SQL.ipynb
│ ├─ 05.EDA_with_Visualization_Lab.ipynb
│ ├─ 06.Interactive_Visual_Analytics_with_Folium.ipynb
│ ├─ 07.Interactive_Visual_Analytics_with_Plotly_Dash.py
│ └─ 08.Machine_Learning_Prediction_Lab.ipynb
│
├─ reports/
│ ├─ figures/
│ └─ slides/
│
├─ docs/
│ └─ IBM_Capstone_Report.docx
│
├─ README.md
├─ requirements.txt
└─ .gitignore
```

---

## Notebooks Overview

### 1. Data Collection — API

**Notebook:** `01.Data_collection_API_Lab.ipynb`  

- Data retrieval using REST APIs  
- JSON parsing and transformation into Pandas DataFrames  

### 2. Data Collection — Web Scraping

**Notebook:** `02.Data_collection_Web_Scraping_Lab.ipynb`  

- Web scraping from Wikipedia  
- HTML parsing with BeautifulSoup  
- Extraction of tabular launch data  

### 3. Data Wrangling

**Notebook:** `03.Data_Wrangling.ipynb`  

- Data cleaning and preprocessing  
- Handling missing values and inconsistent formats  
- Feature preparation for exploratory analysis  

### 4. Exploratory Data Analysis (EDA)

**Notebooks:**  

- `04.EDA_with_SQL.ipynb`  
- `05.EDA_with_Visualization_Lab.ipynb`  

Key exploratory insights derived from SQL queries and data visualizations include:

- Launch success rates vary significantly across launch sites, with **KSC LC-39A** showing the highest overall success performance.
- Payload mass has a noticeable impact on mission outcome: **mid-range payloads** tend to have higher success rates compared to very low or very high payloads.
- Certain orbital types (e.g., LEO) are associated with higher launch success rates.
- Reused boosters show improved success outcomes compared to early non-reused missions, indicating operational maturity over time.
- Later Falcon 9 versions demonstrate higher reliability than earlier versions.

### 5. Interactive Visual Analytics

**Notebooks:**  

- `06.Interactive_Visual_Analytics_with_Folium.ipynb`

Using interactive maps, spatial patterns of launch sites were analyzed:

- Launch sites are located **close to coastlines**, supporting safe downrange trajectories.
- Sites are generally **near highways and railways**, enabling efficient logistics and transportation of launch components.
- Launch facilities maintain a **clear distance from dense urban areas**, minimizing risk to populated regions.
- Proximity to infrastructure appears to be a strategic factor in site selection.

- `07.Interactive_Visual_Analytics_with_Plotly_Dash.ipynb`  

An interactive dashboard was developed to explore launch performance dynamically. Key insights include:

- **KSC LC-39A** has both the largest number of successful launches and the highest success rate.
- Payload ranges between **2,000 kg and 6,000 kg** show the highest launch success rates.
- Very low and very high payload ranges exhibit lower success rates.
- The **Falcon 9 FT and B5 booster versions** achieve the highest launch success rates, reflecting technological improvements over time.

These interactive tools allow users to filter by launch site and payload range, enabling deeper insight into factors influencing mission success.

### 6. Predictive Analysis

**Notebook:** `08.Machine_Learning_Prediction_Lab.ipynb`  

- Classification models to predict first-stage landing success  
- Model evaluation and comparison  

---

## Data Sources

- **SpaceX REST API** — Historical launch records  
- **Wikipedia** — Supplementary launch and mission data (web scraped)  

---

## Methodology

The project follows a structured data science methodology:

1. Data collection using APIs and web scraping  
2. Data wrangling and preprocessing  
3. Exploratory Data Analysis (EDA)  
4. Interactive visual analytics and dashboards  
5. Predictive analysis using classification models  
6. Communication of data-driven insights  

---

## Insights from Folium Plotly Dash

This interactive dashboard enables dynamic exploration of SpaceX launch records by launch site and payload range. By combining dropdown filters, sliders, pie charts, and scatter plots, it provides actionable insights into launch success patterns:

- **Which site has the largest successful launches?**  
  KSC LC-39A has the largest absolute number of successful launches among all sites.

- **Which site has the highest launch success rate?**  
  KSC LC-39A also shows the highest launch success rate, with the largest proportion of successful launches relative to failures.

- **Which payload range(s) has the highest launch success rate?**  
  Payloads in the mid-range (approximately 2,000 kg to 6,000 kg) show the highest concentration of successful launches.

- **Which payload range(s) has the lowest launch success rate?**  
  Very low payloads (below 1,000 kg) and very high payloads (above 8,000 kg) exhibit lower success rates and a higher proportion of failures.

- **Which Falcon 9 Booster version has the highest launch success rate?**
  The Falcon 9 Full Thrust (FT) booster version demonstrates the highest launch success rate, followed closely by B4 and B5, while earlier versions (v1.0 and v1.1) show lower reliability.

These insights highlight how launch site maturity, optimal payload ranges, and booster evolution significantly impact mission success.

---

## Tools & Technologies

- Python
- Pandas, NumPy
- Requests, BeautifulSoup
- Matplotlib, Seaborn
- Folium
- Plotly Dash
- Scikit-learn
- Jupyter Notebook
- GitHub

---

## How to Run Locally

git clone <https://github.com/esanchezlaulhe1312/ibm-datascience-capstone-spacex.git>

cd ibm-datascience-capstone-spacex

py -m venv .venv

## Activate environment (Windows)

.\.venv\Scripts\Activate.ps1

pip install -r requirements.txt

jupyter notebook

---

## Project Status

 **In progress**  
Currently working on **Module 3: Interactive Visual Analytics and Dashboards**

---

## License

This project is licensed under the MIT License.

---

## Author

Elena Sánchez Laulhé
