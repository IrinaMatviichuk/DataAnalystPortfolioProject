# Portfolio Project 1 — E-commerce Sales Analytics

## Project Overview

This portfolio project analyzes e-commerce sales data using **SQL, Python, and Tableau**.

The project covers the full analytics workflow:

* extracting data from Google BigQuery using SQL;
* performing exploratory and statistical analysis in Python;
* building an interactive dashboard in Tableau Public.

---

## Project Goals

The main objectives of this project were:

* demonstrate SQL skills for data extraction and dataset preparation;
* perform exploratory data analysis (EDA);
* identify business insights and sales patterns;
* apply statistical methods to validate hypotheses;
* create interactive dashboards in Tableau.

---

## Tech Stack

* **SQL** — Google BigQuery
* **Python** — Pandas, NumPy
* **Visualization** — Matplotlib, Seaborn
* **Statistics** — SciPy, Statsmodels
* **Dashboarding** — Tableau Public
* **Environment** — Google Colab / Jupyter Notebook

---

## Dataset Creation

A custom analytical dataset was created by joining multiple tables from BigQuery:

* session
* session_params
* order
* product
* account_session
* account

The dataset includes:

* order date
* session ID
* geography (continent, country)
* device and browser information
* traffic source and channel
* registered user information
* product details
* price and purchase information

**Join strategy:** LEFT JOIN was used to preserve:

* all website sessions
* sessions without purchases
* sessions from unregistered users

---

## Dataset Overview

Final dataset characteristics:

* **Rows:** 349,545
* **Columns:** 18
* **Unique sessions:** 349,545
* **Time period:** 2020-11-01 — 2021-01-31

Key data quality findings:

* Missing user fields are caused by unregistered users
* Missing product fields correspond to sessions without purchases
* Browser language contains partially missing values

---

## Business Analysis

The following business questions were analyzed:

### Sales by Geography

* Top 3 continents by sales
* Top 5 countries by sales
* Top regions by number of orders

### Product Analysis

* Top 10 product categories by sales
* Category comparison in the top-performing country

### Customer Analysis

* Registered vs unregistered users
* Email verification rate
* Newsletter unsubscribe rate

### Channel Analysis

* Sales by traffic channel
* Sales by device type
* Device model contribution

---

## Key Insights

Main business insights:

* **Americas** generated the highest sales
* **United States** was the strongest market
* **Organic Search** was the top revenue-generating channel
* **Desktop users** generated the largest share of sales
* **Sofas & armchairs** was the highest revenue product category
* Registered users showed significantly different purchase behavior compared to unregistered users

---

## Sales Dynamics Analysis

Time-series analysis included:

* daily sales dynamics
* continent-level sales trends
* traffic channel trends
* device sales trends

Findings:

* sales showed several peaks during December and January
* Americas consistently led daily revenue
* Organic Search remained the strongest traffic source over time

---

## Pivot Table Analysis

Created pivot tables for:

* sessions by traffic channel and device
* sales by product category and country
* sales by traffic channel and device
* orders by product category and device

---

## Statistical Analysis

### Correlation Analysis

Analyzed relationships between:

* daily sessions and sales
* continent sales
* traffic channel sales
* top product category sales

Result:

* Daily sessions and sales showed strong positive correlation (**r = 0.79**)

### Statistical Tests

Applied multiple statistical methods:

* Shapiro-Wilk test
* Mann-Whitney U test
* Kruskal-Wallis test
* Proportion Z-test
* Pearson correlation

Key findings:

* Registered and unregistered users have statistically significant differences in sales
* Traffic channels differ significantly in daily sessions
* Organic traffic share between Americas and Europe showed no significant difference

---

## Tableau Dashboard

Interactive dashboard created in Tableau Public (2 pages max):

### Dashboard Sections

Page 1:

* KPI overview
* Sales by geography
* Sales by traffic channel
* Device breakdown

Page 2:

* Sales dynamics
* Product category analysis
* Customer segmentation

Tableau Public Dashboard:
https://public.tableau.com/app/profile/iryna.matviichuk/viz/E-commerceSalesCustomerInsights_17826701604260/E-commerceSalesCustomerInsights?publish=yes
