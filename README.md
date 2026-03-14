# Customer Segmentation using RFM Analysis

## Project Overview

This project performs customer segmentation using the **RFM (Recency, Frequency, Monetary) methodology** applied to transactional data. The objective is to identify behavioral patterns among customers and support strategic decision-making related to retention, marketing prioritization, and customer value management.

Through exploratory data analysis, data preparation, and RFM segmentation, the project identifies groups of customers with distinct purchasing behaviors and quantifies their relative impact on business revenue.

The final result provides a structured segmentation framework that can be used to guide CRM strategies, retention campaigns, and customer lifecycle management.

---

## Dataset Description

The dataset contains transactional and customer information including:

- Customer identifier
- Purchase value
- Purchase frequency
- Last purchase date
- Product category
- Customer demographic information

From these variables, the **RFM metrics** were derived:

- **Recency (R):** Number of days since the customer's last purchase
- **Frequency (F):** Number of purchases made by the customer
- **Monetary (M):** Total value spent by the customer

---

## Methodology

The project follows a structured analytical pipeline composed of the following stages.

### 1. Data Cleaning and Preparation

Initial data preparation included:

- Identification and removal of missing values in key variables
- Detection and treatment of outliers using the **Interquartile Range (IQR) method**
- Validation of data consistency and structure
- Standardization of numeric variables

This step ensured the dataset used for analysis contained reliable and consistent information.

---

### 2. Feature Engineering

Additional variables were created to support customer behavior analysis, including:

- Estimated monthly spending
- Average ticket value
- RFM indicators (Recency, Frequency, Monetary)

These features allow the analysis to capture both **customer activity level and economic contribution**.

---

### 3. RFM Scoring

Customers were scored using **quintile-based ranking (1–5)** for each dimension:

- **R Score:** Based on recency (lower recency → higher score)
- **F Score:** Based on purchase frequency
- **M Score:** Based on total spending

The final **RFM score** was obtained by combining these three scores.

To simplify the segmentation visualization, a consolidated metric was created:

**MF Score = (Frequency Score + Monetary Score) / 2**

This allows the construction of a **Recency × Value matrix** used to define customer segments.

---

### 4. Customer Segmentation

Customers were classified into behavioral segments based on their RFM profiles:

- Champions
- Loyal Customers
- Potential Loyalists
- Customers at Risk
- Need Attention
- About to Sleep
- Hibernating
- Lost
- Promising
- Recent Customers
- Cannot Lose Them

These segments reflect different stages of the customer lifecycle and engagement level.

---

### 5. Segment Analysis

For each segment, the following metrics were analyzed:

- Number of customers
- Percentage of the customer base
- Average recency
- Average frequency
- Average monetary value
- Total revenue generated
- Average ticket size

This analysis allowed the identification of segments that combine **large customer volume with significant revenue impact**.

Visualizations were created to support the analysis, including:

- RFM matrix visualization
- Segment distribution charts
- Revenue contribution by segment

---

## Key Findings

The analysis revealed three main behavioral groups within the customer base:

### High Impact Segments

The segments **Loyal Customers**, **Customers at Risk**, and **Potential Loyalists** concentrate the majority of customers and revenue.  
These groups represent the core of the business and require careful retention and engagement strategies.

### Intermediate Segments

Segments such as **Lost**, **About to Sleep**, **Hibernating**, and **Need Attention** show moderate customer volume and lower revenue impact.  
These customers have had previous engagement but demonstrate declining activity, indicating potential for reactivation campaigns.

### Strategic Niche Segments

Segments such as **Champions**, **Cannot Lose Them**, **Recent Customers**, and **Promising** represent smaller portions of the customer base but hold strategic importance due to their high value or future potential.

---

## Business Implications

The segmentation allows organizations to prioritize actions based on both **customer scale and financial impact**:

- Retention strategies should focus on customers classified as **At Risk**
- Relationship-building strategies should target **Potential Loyalists**
- High-value customers such as **Champions** should receive personalized engagement

This framework enables more efficient allocation of marketing resources and supports data-driven CRM strategies.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Project Structure
