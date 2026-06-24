# Books-to-Scrape ETL & Analytics Pipeline

## Overview

This project demonstrates an end-to-end data workflow involving web scraping, data cleaning, exploratory data analysis, database creation, and SQL analytics.

Using the Books to Scrape website, I extracted book information across multiple pages, enriched the data with additional product details, transformed the dataset for analysis, stored it in SQLite, and performed both visual and SQL-based analysis.

The project was designed to demonstrate practical data collection and analytics skills rather than to solve a specific business problem.

---

## Objectives

* Scrape book data from a multi-page website
* Build a reproducible ETL workflow
* Clean and transform scraped data
* Perform exploratory data analysis
* Store data in a relational database
* Answer analytical questions using SQL
* Assess and document data quality issues

---

## Data Pipeline

Web Scraping

↓

Data Cleaning & Feature Engineering

↓

Exploratory Data Analysis

↓

SQLite Database Creation

↓

SQL Analytics

---

## Technologies Used

* Python
* Requests
* BeautifulSoup
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SQLite
* SQL
* Jupyter Notebook

---

## Project Structure

```text
books-to-scrape-etl-analytics/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── books.db
│
├── notebooks/
│   ├── 01_web_scraping.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_exploratory_analysis.ipynb
│   ├── 04_sql_database_creation.ipynb
│   └── 05_sql_analysis.ipynb
│
├── screenshots/
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Data Quality

During the enrichment stage, individual product pages were visited to collect additional information such as category, description, UPC, tax, and stock availability.

### Results

* Total books scraped: 1,000
* Successful product page enrichments: 992
* Enrichment success rate: 99.2%
* Records with missing enrichment fields retained: 8

Incomplete records were preserved to maintain dataset integrity and transparency. Missing values were excluded from category-level aggregations where appropriate.

---

## Exploratory Analysis

Key analyses included:

* Category distribution
* Rating distribution
* Average rating by category
* Price distribution
* Average price by category
* Stock quantity distribution
* Inventory analysis
* Correlation analysis

---

## SQL Analysis

The SQLite database was used to answer analytical questions such as:

* Which categories contain the most books?
* Which categories have the highest average ratings?
* Which books are the most expensive?
* Which categories hold the highest inventory value?
* What is the average price by category?
* Which categories have the highest stock levels?
* What data quality issues exist within the dataset?

---

## Key Findings

* The dataset contains 1,000 books spanning multiple categories.
* Nonfiction and Sequential Art were among the largest categories.
* Several categories achieved consistently high average ratings.
* Inventory value varied considerably across categories.
* Data quality assessment identified a small number of incomplete records resulting from unsuccessful enrichment requests.

---

## Lessons Learned

* Built a complete ETL workflow from extraction to SQL analysis.
* Implemented fault-tolerant scraping using exception handling and request throttling.
* Managed incomplete records while preserving source data integrity.
* Performed data quality assessment and missing value analysis.
* Applied SQL to answer analytical questions using a relational database.

---

## Future Improvements

* Implement automated retry logic for failed requests.
* Add structured logging for scraping operations.
* Build a Power BI dashboard connected to SQLite.
* Schedule automated data collection workflows.
* Introduce unit tests and data validation checks.
