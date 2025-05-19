# rockbuster-sql-analysis

SQL-based data analysis project for **Rockbuster Stealth**, a global movie rental company adapting its business model for online streaming. This project focuses on customer segmentation, geographic revenue distribution, rental statistics, and high-value behavior analysis using advanced SQL techniques.

View this project in my portfolio presentation: [Google Slides Portfolio](https://docs.google.com/presentation/d/1qkxnA_wyYDSZGrbO7H8aNu45hsYfwUvO/edit?slide=id.p1#slide=id.p1)

## Project Purpose

This portfolio project demonstrates the use of **PostgreSQL** to answer complex business questions that support Rockbuster’s strategy to compete with platforms like Netflix. The queries make use of **CTEs, joins, aggregations, and subqueries** to explore the customer base, top spenders, high-volume regions, and key product metrics.

---

## Key Questions Answered

1. **What is the average amount spent by the top 5 customers in the top 10 cities?**
2. **How many top customers are located in each country?**
3. **Who are the top 5 customers in the most active cities and countries?**
4. **Which countries and cities have the highest number of customers?**
5. **What are the descriptive statistics for key numerical fields in the film catalog?**

---

## Tools Used

* **PostgreSQL** for querying the data
* **Tableau** *(optional for visualizations – add link if used)*
* **GitHub** for project version control and documentation

---

## Data Source

The analysis is based on the **PostgreSQL DVD Rental Sample Database**, which simulates a real-world video rental business. It includes tables such as `customer`, `address`, `city`, `country`, `payment`, and `film`.

---

## Query Summaries

### 1. **Top Customer Average Payment Analysis**

> *What is the average total payment made by the top 5 customers, filtered by the top 10 cities within the top 10 countries?*

* Uses nested filtering through Common Table Expressions (CTEs)
* Identifies geographic clusters of high-value customers
* Supports regional targeting for loyalty campaigns

### 2. **Top Customer Distribution by Country**

> *How many of the top 5 highest-paying customers live in each country, compared to the total customer base?*

* Aggregates both total and top customer counts by country
* Combines `LEFT JOIN` and `DISTINCT` counting to enable comparison
* Helps identify which countries host the most valuable clients

### 3. **Top 5 Customers in Top Cities and Countries**

> *Who are the top 5 customers from the top 10 cities and top 10 countries?*

* Ranks customers by total payment
* Filters by location using CTEs for cities and countries
* Produces a list of high-revenue individuals for reward programs

### 4. **Top Cities and Countries by Customer Volume**

> *Which countries and cities have the highest customer counts?*

* Identifies top 10 countries and then the top 10 cities within them
* Helps inform regional strategies and market prioritization
* Used as a filtering layer in other queries

### 5. **Descriptive Statistics for the Film Table**

> *What are the min, max, average, and count values for key film-related fields?*

* Covers columns such as `rental_rate`, `replacement_cost`, `length`, and `rental_duration`
* Useful for understanding product pricing, inventory planning, and catalog composition
* Offers baseline statistics to detect outliers or set thresholds

---

## How to Use

1. Clone or fork this repository.
2. Import the [DVD Rental sample database](https://www.postgresqltutorial.com/postgresql-sample-database/) into PostgreSQL.
3. Run the queries in any SQL IDE (e.g., pgAdmin, DBeaver, or DataGrip).
4. Optionally, export results to a BI tool like Tableau for visualization.

---

## Next Steps (Optional Enhancements)

* Create Tableau dashboards for top customer mapping, payment distributions, and film inventory insights.
* Add Python notebooks for deeper statistical analysis or forecasting.
* Automate report generation for recurring insights.

