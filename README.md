# Project Overview

In this project i've used Sqlite3  to save the data into the database then did **Exploratory Data Analysis (EDA)** and business-focused querying on a dataset of 10,000+ international clients from Infosys Ltd.

It is split into two real-world case studies:
- Case Study 1: Country-level revenue trends
- Case Study 2: Industry-level performance and workload management

---

## Tools & Skills Used

- SQlite3- SQL-based Exploratory Data Analysis (EDA)
- Python
- Pandas
- Matplotlib
- Seaborn
- CSV Data Loading

---

## EDA Techniques Performed

- Value distribution analysis of `RevenueUSD`
- Profiling `Country`, `Industry`, and `ContactName` fields
- Identifying data outliers (very high-revenue clients)
- Aggregating by categories to spot patterns
- Filtering to isolate high-impact segments (e.g., avg. revenue > $4M)

Example:  
```
# 1. Total and average revenue by industry.
total_and_avg_rev_by_industry=('''select industry, sum(revenueUSD) as total_revenue,
                               avg(revenueUSD) as avg_revenue
                               from infosys_clients_table
                               group by industry
                               order by total_revenue desc''')

pd.read_sql(total_and_avg_rev_by_industry,conn)
```
