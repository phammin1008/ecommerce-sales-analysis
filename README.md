# 🛒 E-Commerce Sales Analysis

## 📌 Project Overview

### 🎯 Objective
This project aims to analyze real-world e-commerce transaction data from a UK-based online retailer in order to better understand sales performance, customer purchasing behavior, and revenue distribution across time, countries, and products.

The primary goal is to generate **business-relevant insights** that can support decision-making in areas such as **market prioritization, product strategy, and revenue monitoring**.

---

### 🌍 Context
E-commerce companies generate large volumes of transactional data that often include real-world complexities such as **cancelled orders, returns, missing customer information, and pricing anomalies**.

This dataset, covering transactions between **December 2010 and December 2011**, reflects these challenges and provides an opportunity to apply **practical data analysis techniques on non-ideal, real business data**.

---

### ⏱ Duration
The project was completed over several working sessions, including:
- Data exploration
- Data cleaning
- Metric definition
- Aggregation
- Visualization

---

### 👤 Role
As the **Data Analyst**, I was responsible for:
- Exploring and understanding the structure and quality of the data  
- Defining business rules for handling cancelled and returned transactions  
- Creating key metrics such as revenue  
- Aggregating and visualizing data to extract actionable insights  

---

### 🛠 Tools and Technologies
- **Python** (pandas, numpy) for data manipulation and analysis  
- **Matplotlib & Seaborn** for data visualization  
- **Jupyter Notebook** for exploratory analysis and documentation  

---

## 🔍 Approach and Process

### 📊 Data Understanding and Cleaning
The dataset contains individual transaction lines with information such as:
- Invoice number  
- Product details  
- Quantity  
- Unit price  
- Customer ID  
- Invoice date  
- Country  

A key business rule identified during exploration was that:
- Invoice numbers starting with **“C”** represent cancelled or returned transactions  
- Returned items are recorded as **negative quantities**, with corresponding unit prices  

Instead of removing these rows, they were **intentionally retained** so that returned transactions could naturally **offset sales revenue**.  
This approach ensures that revenue calculations reflect **net sales**, which is more accurate from a business perspective.

Missing values were assessed, particularly for customer identifiers, and retained where they did not impact **revenue-based analysis**.

---

### 🧩 Feature Engineering
To support business analysis:
- Invoice dates were converted to **datetime** format  
- A **Year-Month** variable was created to enable monthly aggregation  
- A **Revenue** metric was calculated at transaction-line level:

