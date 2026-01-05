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
│ ├─ 07.Interactive_Visual_Analytics_with_Plotly_Dash.ipynb
│ └─ 08.Machine_Learning_Prediction_Lab.ipynb
│
├─ reports/
│ ├─ figures/
│ └─ slides/
│
├─ docs/
│ └─ project_log.docx
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

Exploration of relationships between launch success and variables such as payload mass, orbit type, launch site, and booster reuse.

### 5. Interactive Visual Analytics

**Notebooks:**  

- `06.Interactive_Visual_Analytics_with_Folium.ipynb`
- `07.Interactive_Visual_Analytics_with_Plotly_Dash.ipynb`  

Geospatial analysis of launch sites and interactive dashboards for deeper insight exploration.

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

## Preliminary Insights (Early Findings)

Based on exploratory data analysis performed using SQL queries and visual analytics, the following insights have been identified:

- Launch success rates vary significantly across launch sites, indicating that site-specific operational conditions may influence first-stage landing outcomes.
- Payload mass shows a clear relationship with launch success, where extremely low and extremely high payloads tend to have lower success rates compared to mid-range payloads.
- Certain orbit types are associated with higher launch success, suggesting that mission profile and orbital requirements impact landing feasibility.
- Newer Falcon 9 booster versions exhibit higher success rates compared to earlier versions, highlighting the impact of technological iteration and operational learning.
- The proportion of successful landings has increased over time, reflecting SpaceX’s progressive improvement in reusability and recovery techniques.

These EDA findings inform feature selection and hypothesis formulation for the predictive modeling stage.

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
Currently working on **Module 1: Introduction & Data Collection**

---

## License

This project is licensed under the MIT License.

---

## Author

Elena Sánchez Laulhé
