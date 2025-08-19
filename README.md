# 📊  Exploratory Data Analysis of Online Retail Dataset

# 🎯 Objective:

The main goal of this project was to analyze online sales data and extract key business insights. For example, which months sold the most, which products were more popular or sold the most, which times sold the most, seasonal trends in sales, etc.

🔍 Dataset Source and Structure

# Source of Dataset
📦 The dataset has been taken from the UCI Machine Learning Repository.

🔗 Dataset Link

https://archive.ics.uci.edu/dataset/352/online+retail

---
# 📊 Structure of Dataset
This dataset contains 525,461 rows and 8 columns. Each column provides different types of information about online retail transactions.

1. 🧾 Invoice
A unique invoice number for each transaction. 

2. 🆔 StockCode
A specific code or ID for each product. 

3. 📝 Description
Product name or description — helps us know what kind of product was sold.

5. 🔢 Quantity
Indicates how many units of a product were sold.

6. 🗓️ InvoiceDate
Date and time of the transaction.

7. 💰 Price
Price of a single unit of the product.

8. 👤 Customer ID
An ID for each customer .

9. 🌍 Country
The country from which the product was purchased.

# 🧹 Data Cleaning & Preprocessing

One of the most important steps in a successful data analysis project is data cleaning and preprocessing. Most data never arrives in a perfectly organized state. Datasets contain errors, missing values, duplicates, and data in incorrect formats.

The cleaning and pre-processing performed in this project is explained step by step below:

# 1️⃣ ❓ Missing Values Handling

Missing (null) values in a dataset can cause

problems during analysis. Missing values need to be managed.

# 🔎 Step 1: Finding Missing Values

Code : df.isnull().sum()

There are 2928 missing values in the Description column and 107927 missing values in the Customer ID column.

# ✍️ Step 2: Fill Missing values

Sometimes there is information about multiple products under the same invoice number, where some records have the Customer ID, some do not.
Therefore, the forward fill method is used to fill the Customer ID missing values.

Code : df["Customer ID"].fillna(df["Customer ID"]. fill(), inplace(True)

# 2️⃣ 🧮 Calculating Total Price

Code : df["Total Income"]=df["Quantity"] * df["Price"]

To find out how much money was sold in each transaction, we multiplied the Quantity (how many products were sold) and Price (price per unit) columns. This calculation created a new column called Total Income, where the total amount of each row of sales will be shown.

# 3️⃣  🗓️ Date Formatting

✔️Step 1

Code :  df["YearMonth"]=df["InvoiceDate"]. dt.to_period()

In the dataset, the InvoiceDate column represents the date and time of each transaction. However, for analysis purposes, only the year and month are collected separately in a new column called YearMonth.

✔️Step 2

Code :  df["Date of Week"]=df["InvoiceDate"]. dt.day_name()

The day of the week on which each transaction occurred is extracted from the Invoice Date column in the dataset and collected into a new column called Week Date.

✔️Step 3

Code :df["Time"]=df["InvoiceDate"].dt.time()

for analysis purposes  separates only the time are collected separately in a new column called called Time.

✔️Step 4

Code :df["Month"]= df["InvoiceDate"]. dt.month

for analysis purposes separates only the month are collects separately in a new column called called Month.

# 📈 Analysis & Visualization
1) What were the total sales and income per month?  (Analysis)
    Total Sales Per Month Line Chart (Visualization)
     Total Income Per Month Line Chart (Visualization)

 2)Which month has the highest income?  (Analysis)
     Highest monthly income Plot (Visualization)

 3) What day of the week costs the most?  (Analysis)
      The most expensive day of the week (Visualization)

 4) Which customer made the most purchases?  (Analysis)

 5) Average price per order  (Analysis)

 6) Which country received the most orders?  (Analysis)

7) Which product sold the most?  (Analysis)

 8) Which product generated the most revenue? (Analysis)

 9) What time of day do you get the most orders? (Analysis)

 10) What is the most returned product? (Analysis)

11) Returned Product List (Analysis)

 12) How many products were returned?  (Analysis)

 13) At what time did the most products get returned?  (Analysis)
        Top 8 Return Times (Visualization)

 14) Seasonal sales trends Seasonal Sales Trends  (Analysis)

 15) What time of year do sell the most?  (Analysis)

 16) Relationship between sales and seasonal changes (Winter vs Summer Sales)  (Analysis)
       Sales Comparison: Winter vs Summer (Visualization)

 17) Which customer is buying the most products at the highest price?  (Analysis)

 18) Average order quantity of customers in different countries 
        Top 10 Countries with Highest Average Order Quantity (Visualization)

 19) What products sell the most at what time of year?   (Analysis)

# Key Features ✨

📌 Monthly Sales & Income Trends

📌 Highest Income Month Analysis

📌 Top Customer & High Spenders

📌 Country-wise Order Distribution

📌 Best-Selling & Revenue-Generating Products

📌 Customer purchase behavior

# 🛠 Tools & Technologies

🐍 Python — Data Processing & Analysis

📑 Pandas — Data Handling

📊 Plotly, Scaborn, Matplotlib — Data Visualization

# Outcome :

📈 Visualized sales & income trends, identified top products, customers, and countries, analyzed returns and seasonal patterns, and revealed customer behavior to guide smarter business decisions.

# Project Objectives:

This analysis help businesses track sales trends, identify top products and customers, understand seasonal and geographical patterns, reduce returns, and make data-driven decisions for growth.
