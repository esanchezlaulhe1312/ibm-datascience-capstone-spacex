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
│ └─ ibm_capstone_spacex_ppt_Rev0.pdf
│
├─ images/
│ ├─ plotly_dash_screenshots/
│ ├─ figures/
│ └─ logos/
│
├─ README.md
├─ requirements.txt
└─ .gitignore
```

---

## Notebooks Overview

### 1. Data Collection — API

**Notebook:** `01.Data_collection_API_Lab.ipynb`  

- Data retrieval using the SpaceX REST API
- Extraction of launch, payload, rocket, landing, and site information
- Parsing nested JSON responses into structured Pandas DataFrames

### 2. Data Collection — Web Scraping

**Notebook:** `02.Data_collection_Web_Scraping_Lab.ipynb`  

- Web scraping of historical launch data from Wikipedia
- HTML parsing with BeautifulSoup  
- Cleaning and structuring tabular data for analysis

### 3. Data Wrangling

**Notebook:** `03.Data_Wrangling.ipynb`  

- Handling missing values and inconsistent formats
- Removing irrelevant and redundant features
- Encoding categorical variables
- Feature scaling for machine learning compatibility
- Definition of a binary target variable (class) representing launch success

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

In this module, several supervised machine learning models were trained and evaluated to predict the success of SpaceX Falcon 9 launches.

#### Models Evaluated

- Logistic Regression (with hyperparameter tuning using GridSearchCV)
- Support Vector Machine (SVM)
- Decision Tree Classifier
- K-Nearest Neighbors (KNN)

#### Key Insights

- The dataset is relatively small (~90 samples), with a limited test set size, making generalization challenging.
- Logistic Regression, SVM, and KNN achieved similar test accuracy (~83.33%).
- Decision Tree performance showed higher sensitivity to data splitting, achieving slightly lower accuracy.
- Comparable performance across models suggests that launch success is partially predictable but influenced by complex, non-linear factors.

---

## Data Sources

- **SpaceX REST API** — Historical launch records  
- **Wikipedia** — Supplementary launch and mission data (web scraped)  
- **IBM Skills Network** — curated Falcon 9 datasets used during the course

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

 **Completed**
Final submission for **Module 5: Present Data-Driven Insights**

---

## License

This project is licensed under the MIT License.

---

## Author

Elena Sánchez Laulhé
[Coursera](https://www.coursera.org/learner/elena-sanchez-laulhe-1312)
[LinkedIn](https://www.linkedin.com/in/elena-sanchez-laulhe/)  
[GitHub](https://github.com/esanchezlaulhe1312)
