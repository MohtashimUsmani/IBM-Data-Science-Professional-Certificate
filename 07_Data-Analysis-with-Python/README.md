# 🏠 House Sales in King County, USA

A data analysis and machine learning project focused on predicting residential house prices using the **King County, USA** housing dataset.

This project was completed as part of the **IBM Data Science Professional Certificate – Data Analysis with Python** course. The notebook covers the complete workflow from importing and cleaning the data to exploratory data analysis, regression modeling, and model evaluation.

---

## 📌 Project Overview

The goal of this project is to determine the market price of a house based on features such as:

- Square footage
- Number of bedrooms and bathrooms
- Number of floors
- Waterfront view
- House condition and grade
- Location information
- Living area and basement size
- Year built and renovation information

The project uses statistical analysis and several regression techniques to understand which features are useful for predicting house prices.

---

## 🎯 Objectives

The notebook focuses on the following tasks:

1. Import and inspect the housing dataset.
2. Understand data types and descriptive statistics.
3. Clean missing values.
4. Perform exploratory data analysis.
5. Investigate relationships between housing features and price.
6. Build linear regression models.
7. Build a regression pipeline using feature scaling and polynomial features.
8. Evaluate models using the **R² (coefficient of determination)** metric.
9. Apply Ridge Regression for regularization.
10. Evaluate a second-order polynomial Ridge Regression model.

---

## 📊 Dataset

The dataset contains house sale information for **King County, which includes Seattle**, covering homes sold between **May 2014 and May 2015**.

The dataset includes variables such as:

| Feature | Description |
|---|---|
| `price` | House sale price — prediction target |
| `bedrooms` | Number of bedrooms |
| `bathrooms` | Number of bathrooms |
| `sqft_living` | Square footage of the home |
| `sqft_lot` | Square footage of the lot |
| `floors` | Number of floors |
| `waterfront` | Whether the house has a waterfront view |
| `view` | Number of times the property has been viewed |
| `condition` | Overall condition of the house |
| `grade` | Overall grade of the housing unit |
| `sqft_above` | Square footage excluding the basement |
| `sqft_basement` | Square footage of the basement |
| `yr_built` | Year the house was built |
| `yr_renovated` | Year the house was renovated |
| `zipcode` | ZIP code |
| `lat` | Latitude |
| `long` | Longitude |
| `sqft_living15` | Living room area in 2015 |
| `sqft_lot15` | Lot area in 2015 |

The dataset used in the notebook was provided through the IBM Skills Network course environment and is based on the King County housing dataset.

---

## 🧹 Data Wrangling

The dataset initially contained missing values in:

- `bedrooms` — 13 missing values
- `bathrooms` — 10 missing values

The missing values were replaced with the respective column means.

The columns below were also removed because they were identifiers rather than useful predictive features:

```text
id
Unnamed: 0
```

---

## 🔎 Exploratory Data Analysis

Several techniques were used to explore the dataset:

### Floor Distribution

The number of houses was calculated for each unique floor value using `value_counts()`.

### Waterfront Price Comparison

A Seaborn boxplot was used to compare house prices for properties with and without waterfront views.

### `sqft_above` vs. Price

A regression plot was used to investigate the relationship between the above-ground square footage and house price.

### Correlation Analysis

The numerical features were correlated with `price` to identify features with stronger relationships to house prices.

The strongest positive correlations observed in the notebook included:

| Feature | Correlation with Price |
|---|---:|
| `sqft_living` | 0.702 |
| `grade` | 0.667 |
| `sqft_above` | 0.606 |
| `sqft_living15` | 0.585 |
| `bathrooms` | 0.526 |

---

## 🤖 Model Development

Several regression approaches were tested.

### 1. Linear Regression — `long`

A simple linear regression using longitude produced:

```text
R² = 0.00047
```

This indicates that longitude alone provided very little explanatory power for the target in this model.

### 2. Linear Regression — `sqft_living`

Using `sqft_living` as the predictor produced:

```text
R² = 0.49285
```

### 3. Multiple Linear Regression

The following features were used:

```python
[
    "floors",
    "waterfront",
    "lat",
    "bedrooms",
    "sqft_basement",
    "view",
    "bathrooms",
    "sqft_living15",
    "sqft_above",
    "grade",
    "sqft_living"
]
```

The model achieved:

```text
R² = 0.65769
```

### 4. Polynomial Regression Pipeline

A pipeline combining:

- `StandardScaler`
- `PolynomialFeatures`
- `LinearRegression`

was created.

The resulting model achieved:

```text
R² = 0.75121
```

---

## 🧪 Model Evaluation and Refinement

The dataset was divided into training and testing sets:

```text
Training samples: 18,371
Testing samples: 3,242
Test size: 15%
Random state: 1
```

### Ridge Regression

A Ridge Regression model with:

```text
alpha = 0.1
```

achieved:

```text
Test R² = 0.64788
```

### Second-Order Polynomial Ridge Regression

A second-order polynomial transformation was applied to the training and testing data, followed by Ridge Regression with:

```text
degree = 2
alpha = 0.1
```

The model achieved:

```text
Test R² = 0.70027
```

---

## 📈 Results Summary

| Model | R² |
|---|---:|
| Linear Regression — `long` | 0.00047 |
| Linear Regression — `sqft_living` | 0.49285 |
| Multiple Linear Regression | 0.65769 |
| Polynomial Regression Pipeline | 0.75121 |
| Ridge Regression | 0.64788 |
| Polynomial + Ridge Regression | 0.70027 |

Among the models evaluated in the notebook, the **Polynomial Regression Pipeline** produced the highest R² value of approximately **0.7512** on the data used for that evaluation.

The Polynomial + Ridge model achieved a test R² of approximately **0.7003**.

---

## 🛠️ Technologies & Libraries

- **Python**
- **Pandas** — data manipulation and analysis
- **NumPy** — numerical operations
- **Matplotlib** — data visualization
- **Seaborn** — statistical visualization
- **Scikit-learn** — regression, preprocessing, pipelines, and model evaluation
- **Jupyter Notebook** — interactive analysis

---

## 📂 Project Files

```text
House-Sales-in-King-County/
│
├── README.md
└── House_Sales_in_King_Count_USA.ipynb
```

---

## 🧠 Key Skills Demonstrated

This project demonstrates practical experience with:

- Data loading and inspection
- Data cleaning
- Missing-value handling
- Descriptive statistics
- Exploratory Data Analysis (EDA)
- Correlation analysis
- Data visualization
- Simple linear regression
- Multiple linear regression
- Polynomial features
- Machine learning pipelines
- Feature scaling
- Ridge Regression
- Train/test splitting
- R² model evaluation

---

## 🎓 Course Context

**IBM Data Science Professional Certificate**

**Course:** Data Analysis with Python

**Project:** House Sales in King County, USA

The project was completed as a final project/assignment within the IBM Data Science learning path.

---

## 📚 Dataset Reference

The notebook identifies the original dataset as the King County House Sales Prediction dataset available through Kaggle:

https://www.kaggle.com/harlfoxem/housesalesprediction

The version used in this course was slightly modified for the IBM Skills Network course.

---

## 👤 Author

**Mohtashim Usmani**

BS FinTech Student | Data Science & Machine Learning Learner

PortFolio: [@MohtashimUsmani](https://www.mohtashimusmani.me)

LinkedIn: [Mohtashim Usmani](https://www.linkedin.com/in/mohtashim-usmani/)

---

> This project is part of my ongoing journey through the IBM Data Science Professional Certificate. More projects will be added to this repository as I progress through the certificate.
