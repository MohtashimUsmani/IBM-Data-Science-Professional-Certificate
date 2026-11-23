# Winning Space Race with Data Science — SpaceX Falcon 9 Landing Prediction

**Author:** Mohtashim Usmani  
**Program:** IBM Data Science Professional Certificate — Applied Data Science Capstone  
**Date:** November 24, 2026  
**Final Score:** 100%  

---

## Project Overview
SpaceX offers Falcon 9 rocket launches at a much lower cost than traditional providers because it recovers and reuses the first stage booster. In this capstone project, I collected historical Falcon 9 launch data, explored patterns using SQL and visualizations, built interactive maps and a dashboard, and trained machine learning models to predict whether the first stage will land successfully (`Class = 1` for successful landing, `Class = 0` for unsuccessful landing).

---

## Repository Contents
- **Final Report (PDF):** `Data Science Capstone Project Report.pdf`
- **Notebooks & Scripts:**
  - `Hands-on Lab Complete the Data Collection API Lab` — Collecting Falcon 9 launch records from the SpaceX REST API
  - `Hands-on Lab Complete the Data Collection with Web Scraping lab` — Scraping historical Falcon 9 launch tables from Wikipedia
  - `Hands-on Lab Data Wrangling` — Cleaning data, handling missing values, and creating the binary `Class` target label
  - `EDA with Visualization Lab` — Exploring launch trends, payload mass, orbit types, and launch sites with Matplotlib and Seaborn
  - `Hands-on Lab Complete the EDA with SQL` — Running SQL queries on launch records in SQLite
  - `Hands-on Lab Interactive Visual Analytics with Folium lab` — Mapping launch sites and calculating distances to coastlines/infrastructure
  - `Hands-on Lab Build an Interactive Dashboard with Plotly Dash` (`spacex-dash-app.py`) — Interactive dashboard with launch site filter and payload range slider
  - `Hands-on Lab Complete the Machine Learning Prediction lab` (`SpaceX_Machine Learning Prediction_Part_5.ipynb`) — Classification modeling and hyperparameter tuning with `GridSearchCV`

---

## Key Findings & Results

### 1. Exploratory & Visual Insights
- **Top Launch Site:** **KSC LC-39A** accounted for the largest share of successful launches across all sites at **41.7%** (with a **76.9%** individual success rate).
- **Booster Version Performance:** Booster version **FT** was the most frequently used and showed strong landing success across a wide range of payload masses.
- **Yearly Trend:** First-stage landing success improved significantly from 2013 onward, reaching over **80%** by 2020.

### 2. Machine Learning Classification Performance
Models were trained using an `80%` train / `20%` test split with feature standardization (`StandardScaler`) and 10-fold cross-validation (`GridSearchCV`, `cv=10`):

| Model | Test Accuracy |
| :--- | :---: |
| **Logistic Regression** | **83.33%** |
| **Support Vector Machine (SVM)** | **83.33%** |
| **K-Nearest Neighbors (KNN)** | **83.33%** |
| **Decision Tree** | **72.22%** |

- **Takeaway:** Logistic Regression, SVM, and KNN tied for the highest test accuracy at **83.33%**, while Decision Tree scored **72.22%** on the 18-sample test set due to overfitting on training splits.

---

## Module 1 Lab Issues Encountered & Resolutions

### 1. SpaceX API Lab — HTTP 522 Connection Timeout
- **Issue:** Running API helper functions such as `getBoosterVersion(data)` returned an **HTTP 522 (Connection Timed Out)** error and raised `JSONDecodeError: Expecting value: line 1 column 1 (char 0)`.
- **Cause:** General internet connectivity inside JupyterLab returned `HTTP 200`, while both JupyterLab and direct browser requests to the external SpaceX API returned `HTTP 522`, indicating an external server/API timeout rather than an issue in the Python code.
- **Resolution:** Retried API calls when the service was available and used the saved dataset to continue downstream wrangling, EDA, and modeling labs without interruption.

### 2. Web Scraping Lab — `AttributeError` on `Customer` Table Cells
- **Issue:** Scraping the Wikipedia launch table stopped partway through with `AttributeError: 'NoneType' object has no attribute 'string'` on `customer = row[6].a.string`.
- **Cause:** Several cells in the `Customer` column did not contain an `<a>` hyperlink tag, causing `row[6].a` to return `None` and leaving incomplete row counts (`105` rows for `Customer`, `Launch outcome`, and `Booster landing` vs. `106` for other columns).
- **Resolution:** Added a safe helper function (`cell_text`) to extract `cell.a.string.strip()` when a link exists and fall back to `cell.get_text().strip()` when no `<a>` tag is present, allowing all **121** records across **11** columns to parse cleanly.

---

## Technologies Used
- **Languages & Libraries:** Python, Pandas, NumPy, Requests, BeautifulSoup, Matplotlib, Seaborn, Scikit-learn, Folium, Plotly Dash
- **Database & Querying:** SQLite / SQL (`%sql`)