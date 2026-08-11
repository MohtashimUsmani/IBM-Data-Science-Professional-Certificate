# 04 — Python for Data Science, AI & Development

✅ **Status:** Completed

## Overview

This course covered core Python programming for data science — data structures, working with APIs, and manipulating tabular data with `pandas` and `numpy`. The final practice project applies these skills to a realistic data engineering scenario: extracting and cleaning economic data from the web.

## 📓 Notebook

| Notebook | Description |
|---|---|
| [`GDP_Data_extraction_and_processing.ipynb`](notebooks/GDP_Data_extraction_and_processing.ipynb) | **project.** Scenario: as a junior data engineer for an international firm, extract the top 10 largest economies by GDP (IMF figures) from a Wikipedia table via web scraping, clean and convert the data with `pandas`/`numpy`, and export the result to CSV. |

## 🎯 What This Project Demonstrates

- Scraping a live HTML table directly into a DataFrame with `pandas.read_html()`
- Selecting, filtering, and relabeling DataFrame columns and rows
- Type conversion and numeric rounding with `numpy`
- Unit conversion (Million USD → Billion USD) and data cleaning
- Exporting a processed dataset to CSV

## 🛠 Tools

`Python` · `pandas` · `numpy` · `lxml`
