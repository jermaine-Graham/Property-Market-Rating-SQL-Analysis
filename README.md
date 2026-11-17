 SQL Queries & Database Projects

A collection of SQL scripts and database schemas created for analyzing housing market data and running structured queries.

# Project Overview
This repository contains local SQL scripts written and tested in VS Code. It covers schema definitions, data filtering, aggregations, and summary statistics.

# Data Source 
Source: kaggle  www.kaggle.com

Data name: UK housing market

# Key Files
`01_schema.sql` - Database structure and initial table creation.

`Maine SQL Schema uk_housing_market 01 02.sql` - Queries analyzing housing market data, property ratings, and location metrics.

## Tools & Technologies
LanguageSQL
Editor: Visual Studio Code (SQLTools extension)
Version Control: Git &b github 


# UK Housing Market — SQL Schema & Exploratory Analysis

A collection of PostgreSQL scripts for creating, importing, and analyzing housing market data. This project demonstrates core SQL data analysis techniques, including schema definition, bulk CSV ingestion, aggregations, Common Table Expressions (CTEs), conditional categorization, and subqueries.


## 📊 Dataset & Schema

* **Source:** Kaggle (`uk_housing_market.csv`)
* **Table Name:** `uk_housing_market`

| Column | Data Type | Description |

`id` | `INT` | Unique identifier for each property |
 `name` | `VARCHAR(225)` | Name or title of the property |
 `rating` | `NUMERIC(3, 1)` | Property rating score (scale up to 10.0) |
 `address` | `VARCHAR(255)` | Street address of the property |
 `city` | `VARCHAR(100)` | City where the property is located |
 `lat_long` | `VARCHAR(100)` | Latitude and longitude coordinates |

---

## 🔍 Queries & Analysis Included

The SQL script ([Maine SQL Schema uk_housing_market 01 02.sql](https://github.com/jermaine-Graham/VSC-queries-1/blob/main/Maine%20SQL%20Schema%20uk_housing_market%2001%2002.sql)) walks through the following analytical tasks:

1. **Database Setup & Data Ingestion**
   * Defines the `uk_housing_market` table schema and loads records from a local CSV file using PostgreSQL's `COPY` command.
2. **Summary Statistics & Aggregations**
   * Calculates total property counts alongside overall average, maximum, and minimum property ratings using `COUNT()`, `AVG()`, `MAX()`, and `MIN()`.
   * Groups data by city (`GROUP BY`) to compare total listings and average ratings across locations, ranked from highest to lowest property volume.
3. **Filtering & Pattern Matching**
   * Identifies distinct cities with ratings above `5.0`.
   * Filters listings within specific target cities (`San Francisco` and `San Jose`).
   * Uses wildcard pattern matching (`LIKE '%bar%'`) to search for specific keywords in property names.
4. **Common Table Expressions (CTEs)**
   * Uses a `WITH` clause (`avg_property_rating_san_jose`) to dynamically compute the average rating in San Jose and isolate properties outperforming the local average.
5. **Conditional Categorization & Nested Subqueries**
   * Classifies properties into performance tiers (`Excellent`, `Good`, `Okay`, `Poor`) using `CASE WHEN` statements.
   * Aggregates tier counts and averages per city using multi-level nested subqueries.

---

## 🛠️ Tools & Technologies

* **Database:** PostgreSQL
* **Editor:** Visual Studio Code (SQLTools extension)
* **Version Control:** Git & GitHub

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone [https://github.com/jermaine-Graham/VSC-queries-1.git](https://github.com/jermaine-Graham/VSC-queries-1.git)
