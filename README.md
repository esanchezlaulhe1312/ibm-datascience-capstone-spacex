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
├─ images/
│ ├─ plotly_dash_screenshots/
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

In this module, several supervised machine learning models were trained and evaluated to predict the success of SpaceX Falcon 9 launches.

#### Models Evaluated

- Logistic Regression (with hyperparameter tuning using GridSearchCV)
- Support Vector Machine (SVM)
- Decision Tree Classifier
- K-Nearest Neighbors (KNN)

All models were trained using standardized features and evaluated with a train/test split (80/20).

#### Key Insights

- The dataset was relatively small (90 samples), with only **18 samples in the test set**, which makes model generalization more challenging.
- **Logistic Regression** provided stable performance and served as a strong baseline model after tuning.
- For **Support Vector Machines**, the **sigmoid kernel** achieved the best performance on the validation dataset.
- The **Decision Tree classifier**, after hyperparameter tuning, achieved a test accuracy of approximately **83.33%**, making it one of the best-performing models.
- **KNN** performance was sensitive to feature scaling and the choice of neighbors, but did not outperform the tuned Decision Tree.
- Overall, models that included regularization and controlled complexity (Logistic Regression and Decision Tree) performed better given the limited dataset size.


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

## Insights from Machine Learning Prediction

### Best Performing Model

Based on the test accuracy comparison, **Logistic Regression**, **Support Vector Machine (SVM)**, and **K-Nearest Neighbors (KNN)** achieved the highest accuracy, each with approximately **83.33%**.  

The **Decision Tree** model performed slightly worse, with an accuracy of about **77.78%**.  

Overall, multiple models showed comparable performance, but simpler models such as Logistic Regression and KNN achieved the best results on this dataset.

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
Currently working on **Module 5: Present Data-Driven Insights**

---

## License

This project is licensed under the MIT License.

---

## Author

Elena Sánchez Laulhé
