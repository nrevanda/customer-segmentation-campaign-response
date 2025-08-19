# Undressing the Customer Mind: Deep Dive into Spending Behavior and Campaign Response
---

## 1. Business Overview
In today’s competitive retail market, understanding customer behavior is essential for effective marketing strategies. Since not all customers respond the same way to campaigns, segmentation and response analysis are critical.  

This analysis focuses on two priorities:  

1. **High-Value Customers (HVC):** Customers who generate significant revenue and demonstrate strong loyalty. Identifying their profiles enables tailored retention strategies.  

2. **Campaign Responsiveness:** Analyzing how different customer segments respond to campaigns provides insights into engagement levels, helping optimize targeting, improve conversion rates, and allocate resources more effectively.  

By distinguishing between customer segments and their behaviors, businesses can design precise strategies to strengthen loyalty, maximize lifetime value, and enhance overall marketing performance. 

**Key objectives**:
- Identify the characteristics of high-value customers and develop data-driven strategies to retain them.  
- Identify the characteristics of customer responses to marketing campaigns and determine appropriate strategies to enhance effectiveness.

## 2. Data Sources
The dataset used in this project is the [Customer Personality Analysis](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis/data).  
It contains **2,240 customers** with **29 variables** describing demographics, lifestyle, and purchasing behavior.  
The features are grouped into **five categories**:
### 👤 People

| Feature        | Description |
|----------------|-------------|
| `ID`           | Customer's unique identifier |
| `Year_Birth`   | Customer's year of birth |
| `Education`    | Customer's education level |
| `Marital_Status` | Customer's marital status |
| `Income`       | Customer's yearly household income |
| `Kidhome`      | Number of children in the household |
| `Teenhome`     | Number of teenagers in the household |
| `Dt_Customer`  | Date of customer enrollment with the company |
| `Recency`      | Days since the customer's last purchase |
| `Complain`     | 1 if the customer has complained in the last 2 years, 0 otherwise |

---

### 🛍️ Products

| Feature              | Description |
|-----------------------|-------------|
| `MntWines`           | Amount spent on wine in the last 2 years |
| `MntFruits`          | Amount spent on fruits in the last 2 years |
| `MntMeatProducts`    | Amount spent on meat products in the last 2 years |
| `MntFishProducts`    | Amount spent on fish products in the last 2 years |
| `MntSweetProducts`   | Amount spent on sweets in the last 2 years |
| `MntGoldProds`       | Amount spent on gold products in the last 2 years |

---

### 🎯 Promotion

| Feature              | Description |
|-----------------------|-------------|
| `NumDealsPurchases`  | Number of purchases made with a discount |
| `AcceptedCmp1`       | 1 if customer accepted the offer in the 1st campaign, 0 otherwise |
| `AcceptedCmp2`       | 1 if customer accepted the offer in the 2nd campaign, 0 otherwise |
| `AcceptedCmp3`       | 1 if customer accepted the offer in the 3rd campaign, 0 otherwise |
| `AcceptedCmp4`       | 1 if customer accepted the offer in the 4th campaign, 0 otherwise |
| `AcceptedCmp5`       | 1 if customer accepted the offer in the 5th campaign, 0 otherwise |
| `Response`           | 1 if customer accepted the offer in the last campaign, 0 otherwise |

---

### 🏪 Place

| Feature                | Description |
|-------------------------|-------------|
| `NumWebPurchases`      | Number of purchases made through the company’s website |
| `NumCatalogPurchases`  | Number of purchases made using a catalogue |
| `NumStorePurchases`    | Number of purchases made directly in stores |
| `NumWebVisitsMonth`    | Number of visits to the company’s website in the last month |

## 3.Technologies Used
| Category                | Tools / Libraries |
|--------------------------|-------------------|
| **Programming Language** | Python (Pandas, NumPy) |
| **Data Visualization**   | Matplotlib, Seaborn, Plotly |
| **Interactive Dashboard**| Tableau |
| **Development**          | Jupyter Notebook |

## 4. Project Structures
```
The repository is organized as follows:
├── README.md          <- The top-level README for developers using this project.
│
├── data               <- Raw and processed datasets
│
├── notebooks          <- All stages of analysis (data cleaning, EDA, and reporting) were conducted within Jupyter Notebooks
│
├── slide             <- Presentation including background, objective, visuals and business strategies
│
├── dashboard          <- Tableau workbook and related files
│
└── requirements.txt   <- Python dependencies
```

## 5. Methodology / Approach
The project follows these main steps:
1. **Data Cleaning & Preprocessing** – Handling missing values, outliers, and encoding categorical data.  
2. **Exploratory Data Analysis (EDA)** – Understanding demographics, income, and purchasing behavior patterns.  
3. **Feature Engineering** – Creating new features such as total spend, average order, or customer tenure.  
4. **Segmentation Analysis** – Identifying clusters of high-value customers using Length, Recency, Frequency and Monetary (LRFM) analysis.  
5. **Campaign Response Analysis** – Measuring responsiveness across segments to improve targeting.  
6. **Visualization & Dashboarding** – Presenting findings using Tableau for better decision-making.

## 6. Key Insigth
### 6.1 Characteristics of High-Value Customers (HVC)
- **Champion & Loyal Customer (High Value Customer)**
  - Adults (30–45), **high income**, well-educated.
  - Mostly **in relationship**, no children.
  - Spending concentrated on **Wine & Meat**.
  - Heavy **multichannel users** (web, catalog, store).
  - Responsive to high-value campaigns (Cmp1, Cmp5, Response).

- **Big Spender (Growth Potential)**
  - Adults, **high income**, no children.
  - High spending across all categories, store & catalog heavy.
  - Similar to HVC but not yet loyal.

- **Potential Loyalist (Growth Potential)**
  - Adults / Middle-aged, **medium income**, usually with 1 child.
  - Family-oriented spending (Meat, Fruits, Sweets).
  - Low campaign engagement.
 
### 6.2 Customer Responses to Campaigns
- **Overall Acceptance**
  - Generally low (6–7%), **highest in the last Response campaign (15%)**.
  - **Cmp2 failed (1.3%)** → irrelevant design/targeting.

- **By Segment**
  - **Most responsive**: Loyal Customers, Big Spenders, Champions (25–37% acceptance in Cmp5/Response).
  - **Moderate**: Potential Loyalists (10–12%), Occasional Shoppers (13% in Response).
  - **Low**: At Risk, Loyal Lost, Dormant → mostly 0 acceptance.
  - **New Customers**: low, but start engaging in Response (~8%).

- **Distribution**
  - 70%+ customers **never accepted any campaign (0 acceptance)**.
  - Only ~5% accepted ≥3 campaigns.
  - No segment consistently accepted all campaigns → *no one-size-fits-all campaign works*.
 
  ## 7. Actionable Recommendation
  ### 7.1 Retention Strategies
- **Champion & Loyal Customer**
  - VIP programs (tiers, reward points, early access).
  - Personalized campaigns → less frequent, more relevant.
  - Focus on premium & lifestyle positioning, not just discounts.

- **Big Spender**
  - Push conversion into Loyal Customers.
  - Personalized service, luxury bundles, cross-selling.
  - Store events & premium catalog campaigns.

- **Potential Loyalist**
  - Loyalty starter program (bonus points for repeat purchase).
  - Family bundles (Meat + Fruits + Sweets).
  - Nurturing campaigns → education & affordable offers to drive repeat purchases.

  ### 7.2 Campaign Strategies
- **Segmented Campaigns**
  - Champions & Loyal → VIP perks, premium bundles.
  - Big Spenders → personalized offers, push to loyalty tier.
  - Potential Loyalists → nurturing family bundles + starter loyalty program.
  - Occasional & New → welcome/activation campaigns.
  - At Risk, Loyal Lost, Dormant → selective reactivation only.

- **Channel Optimization**
  - HVC → omnichannel (web, catalog, store).
  - Growth Potential → store-heavy, supported by digital.
  - New/Occasional → start with store promotions, then move to web/app.

- **Benchmark Campaign**
  - The last Response campaign was the most successful (15%).
  - Its design (product, channel, targeting) should be replicated in future campaigns.
 
  ## 8. Contact
  - Author: Naufal Fajar Revanda
  - GitHub: [nrevanda](https://github.com/nrevanda)
  - LinkedIn: [Naufal Fajar Revanda](https://www.linkedin.com/in/naufalrevanda/)
  - Email: nrevanda@gmail.com
