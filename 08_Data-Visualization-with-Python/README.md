# Automobile Sales Data Visualization & Dashboard

A data visualization and interactive dashboard project focused on exploring automobile sales trends during recession and non-recession periods.

This project was completed as part of the **IBM Data Science Professional Certificate – Data Visualization with Python** course. It is divided into two parts: creating visualizations with Matplotlib, Seaborn, and Folium, and building an interactive dashboard with Plotly and Dash.

---

## 📌 Project Overview

The project uses automobile sales data to explore how economic conditions affect vehicle sales, advertising expenditure, and different vehicle categories.

The analysis compares recession and non-recession periods and uses charts, plots, and an interactive dashboard to communicate patterns in the data.

---

## 🎯 Objectives

The project focuses on the following tasks:

1. Visualize average automobile sales over time and identify recession periods.
2. Explore the relationship between advertising expenditure and automobile sales during non-recession periods.
3. Compare sales trends across vehicle types during recession and non-recession periods.
4. Compare GDP trends across recession and non-recession periods.
5. Explore the impact of seasonality on automobile sales.
6. Analyze the relationship between consumer confidence, vehicle prices, and automobile sales during recessions.
7. Compare advertising expenditure during recession and non-recession periods.
8. Visualize advertising expenditure by vehicle type during recessions.
9. Explore how unemployment rates relate to vehicle type and automobile sales.
10. Create a geographical visualization of automobile sales during recession periods.
11. Build an interactive dashboard showing yearly and recession-period automobile statistics.

---

## 📊 Dataset

The project uses the **Automobile Sales** dataset provided through the IBM Skills Network course environment.

The dataset contains automobile sales information and related economic indicators. The notebook uses fields including:

| Feature | Description |
|---|---|
| `Date` | Month-end date of the sales observation |
| `Year` | Year of the observation |
| `Month` | Month of the observation |
| `Recession` | Indicator showing whether the period was a recession (`1`) or non-recession (`0`) |
| `Automobile_Sales` | Number of vehicles sold during the period |
| `GDP` | Gross Domestic Product indicator |
| `unemployment_rate` | Unemployment rate |
| `Consumer_Confidence` | Consumer confidence index |
| `Vehicle_Type` | Vehicle category |
| `Advertising_Expenditure` | Advertising expenditure |
| `Vehicle_Price` | Vehicle price |
| `Seasonality_Weight` | Seasonal weight used in the seasonality visualization |
| `City` | City associated with the automobile sales data |

The dataset is loaded from the IBM Skills Network course environment.

---

## 📈 Part 1: Create Visualizations using Matplotlib, Seaborn & Folium

The first assignment focuses on exploring the automobile sales dataset through static and geographical visualizations.

### Visualizations created

- **Line chart:** Average automobile sales over the years, with recession periods highlighted.
- **Line plots:** Advertising expenditure and automobile sales during non-recession periods.
- **Bar chart:** Comparison of vehicle sales during recession and non-recession periods.
- **Subplots:** GDP trends during recession and non-recession periods.
- **Bubble plot:** Seasonality and its impact on automobile sales.
- **Scatter plots:** Relationships between consumer confidence, vehicle prices, and automobile sales during recessions.
- **Pie charts:** Advertising expenditure during recession and non-recession periods, and expenditure by vehicle type during recessions.
- **Seaborn line plot:** Relationship between unemployment rate, vehicle type, and automobile sales during recessions.
- **Folium choropleth map:** Geographical view of automobile sales during recession periods.

### Main analysis areas

The visualizations are used to explore:

- Changes in automobile sales around recession periods.
- Differences in sales across vehicle categories.
- Advertising expenditure patterns.
- The relationship between economic indicators and automobile sales.
- Seasonal changes in automobile demand.
- Differences in automobile sales across locations.

---

## 📊 Part 2: Create Dashboard with Plotly and Dash

The second assignment builds an interactive **Automobile Sales Statistics Dashboard** using Plotly and Dash.

Users can select a report type from a dropdown menu:

- **Yearly Statistics**
- **Recession Period Statistics**

For yearly statistics, users can also select a year.

### Recession Period Statistics

The dashboard displays:

1. Average automobile sales fluctuation over recession periods.
2. Average number of vehicles sold by vehicle type during recessions.
3. Advertising expenditure share by vehicle type during recessions.
4. Effect of unemployment rate on vehicle type and average automobile sales.

### Yearly Statistics

The dashboard displays:

1. Yearly average automobile sales.
2. Total monthly automobile sales for the selected year.
3. Average vehicles sold by vehicle type in the selected year.
4. Total advertising expenditure by vehicle type in the selected year.

### Interactive features

- Dropdown menu for selecting the report type.
- Year dropdown for yearly statistics.
- Dash callbacks to update the available year selection.
- Dynamic chart updates based on the selected report type and year.
- Interactive Plotly charts.

---

## 🛠️ Technologies & Libraries

- **Python** — programming language
- **Pandas** — data loading, grouping, and analysis
- **NumPy** — numerical operations
- **Matplotlib** — data visualization
- **Seaborn** — statistical data visualization
- **Folium** — geographical visualization and choropleth maps
- **Plotly Express** — interactive charts
- **Dash** — interactive dashboard development
- **Jupyter Notebook** — working environment for Part 1

---

## 📂 Project Files

```text
Automobile-Sales-Data-Visualization/
│
├── README.md
│
├── Final Assignment Part 1 - Create Visualizations using Matplotlib, Seaborn & Folium.ipynb
│
└── Final Assignment Part 2 - Create Dashboard with Plotly and Dash.py
```

---

## ▶️ Running the Dashboard

Part 1 is a Jupyter Notebook. Part 2 is a Python Dash application.

### 1. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn folium plotly dash
```

### 2. Run the dashboard

Open a terminal in the project folder and run:

```bash
python "Final Assignment Part 2 - Create Dashboard with Plotly and Dash.py"
```

### 3. Open the dashboard

After the application starts, open the local address shown in the terminal (usually):

```text
http://127.0.0.1:8050/
```

The dashboard loads the automobile sales CSV from the IBM Skills Network course data URL, so an internet connection is required.

---

## 🧠 Key Skills Demonstrated

This project demonstrates practical experience with:

- Data loading and inspection
- Data grouping and aggregation
- Exploratory data analysis through visualizations
- Time-based trend analysis
- Comparing recession and non-recession periods
- Matplotlib chart creation and customization
- Seaborn statistical plots
- Bubble charts, scatter plots, line charts, bar charts, and pie charts
- Geographical data visualization with Folium
- Interactive visualizations with Plotly
- Building dashboard layouts with Dash
- Creating callbacks using Dash inputs and outputs
- Displaying data dynamically based on user selections
- Communicating data-driven observations

---

## 🎓 Course Context

**IBM Data Science Professional Certificate**

**Course:** Data Visualization with Python

**Assignments:**
- Part 1: Create Visualizations using Matplotlib, Seaborn & Folium
- Part 2: Create Dashboard with Plotly and Dash

---

## 📚 Data Source

The automobile sales dataset is loaded from the IBM Skills Network course environment:

[Automobile Sales Dataset](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/d51iMGfp_t0QpO30Lym-dw/automobile-sales.csv)

The assignments and learning materials are provided as part of the IBM Skills Network course.

---

## 👤 Author

**Mohtashim Usmani**

BS FinTech Student | Data Science & Machine Learning Learner

GitHub: [@MohtashimUsmani](https://github.com/MohtashimUsmani)

---

> This project is part of my ongoing journey through the IBM Data Science Professional Certificate. More projects will be added to this repository as I progress through the certificate.
