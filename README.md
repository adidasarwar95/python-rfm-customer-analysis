
# Python Mini Project – Customer RFM Analysis

**Course:** IBM Data Analyst Program – Career247 (Batch 13)  
**Tools Used:** Python, Pandas, NumPy, Matplotlib, Jupyter Notebook

---

## Project Overview
Performed RFM (Recency, Frequency, Monetary) analysis on a 
real-world customer dataset to segment customers based on their 
purchasing behavior. RFM is widely used in banking and retail 
analytics for customer retention strategy.

---

## Datasets Used

| File | Description | Size |
|------|-------------|------|
| Customer_Master_Data.csv | Customer demographics | 1,000 rows, 9 columns |
| Customer_Transactions.csv | Transaction history | 23,050 rows, 3 columns |

---

## Steps Performed

1. **Data Loading & Exploration** – Loaded both datasets using Pandas, 
   checked shape, dtypes, and null values (no missing values found)
2. **Data Merging** – Merged both datasets on CustomerID using 
   left join → 23,050 rows, 11 columns
3. **RFM Metric Calculation**
   - Recency: Days since last transaction
   - Frequency: Total number of transactions per customer
   - Monetary: Total spend per customer
4. **RFM Scoring** – Scored each metric on a 1–5 scale using 
   `pd.qcut()` and combined into a final RFM Score
5. **Customer Segmentation** – Classified customers into 6 segments 
   based on RFM scores

---

## Key Findings

| Segment | Customers |
|---------|-----------|
| Others | 477 |
| Potential Loyalists | 181 |
| At Risk | 134 |
| Loyal Customers | 122 |
| Lost | 51 |
| Champions | 35 |

- Total Transactions Analyzed: **23,050**
- Total Revenue: **₹2,30,53,199**
- Average Transaction Value: **₹1,000**
- Customer Base: **1,000 unique customers** across 10 cities

---

## Libraries Used
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```
