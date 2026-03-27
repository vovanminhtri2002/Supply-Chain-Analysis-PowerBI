# 📊 Supply Chain Performance Analysis – Power BI Dashboard

<p align="center">
  <img src="https://img.shields.io/badge/PowerBI-Analytics-orange?logo=powerbi">
  <img src="https://img.shields.io/badge/Status-Completed-success">
  <img src="https://img.shields.io/badge/Data-SupplyChain-blue">
  <img src="https://img.shields.io/badge/Visualization-DAX%20%26%20PowerQuery-green">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/f56197b2-72cc-469a-9b43-d3c85786abff"
       alt="Supply Chain"
       width="1200">
</p>

---

## 📖 Table of Contents

- [✨ Introduction](#-introduction)
- [📌 Project Objectives](#-project-objectives)
- [📂 Data Source](#-data-source)
- [🧠 Project Workflow](#-project-workflow)
- [📊 Dashboard Overview](#-dashboard-overview)
- [1️⃣ Overview](#1️⃣-overview)
- [2️⃣ Shipping & Delivery Analysis](#2️⃣-shipping--delivery-analysis)
- [3️⃣ Profit & Sales Analysis](#3️⃣-profit--sales-analysis)
- [4️⃣ Product / Category Analysis](#4️⃣-product--category-analysis)
- [💡 Key Insights](#-key-insights)
- [🧠 Key DAX Measures](#-key-dax-measures)
- [📁 Project Structure](#-project-structure)
- [🔮 Future Improvements](#-future-improvements)
- [👨‍💻 Author](#-author)

---

## ✨ Introduction

This project **Supply Chain Performance Analysis** is built using **Microsoft Power BI**, focusing on analyzing logistics performance, sales, and operational efficiency.

The dashboard helps businesses answer key questions:

**1. How efficient is the delivery system?**

**2. What causes late deliveries?**

**3. Which shipping modes perform the worst?**

**4. Which regions and products generate the most profit?**

**5. How can the supply chain be optimized?**

👉 Designed with: *Insight-driven – Business-focused – Actionable KPIs*

---

## 📌 Project Objectives

- Analyze **delivery performance** and logistics efficiency  
- Identify factors affecting **late delivery**  
- Evaluate **profit and sales performance**  
- Analyze **product/category performance**  
- Build a **4-page Power BI dashboard**  
- Use **DAX measures** to calculate key KPIs  

---

## 📂 Data Source

- Dataset: **[DataCo Global Supply Chain Dataset](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis)**

- Source: Kaggle

- Data includes:

  - Orders information  
  - Shipping & delivery details  
  - Product categories  
  - Sales and profit  

- Key fields:

  - Order Date  
  - Shipping Mode  
  - Order Region  
  - Category Name  
  - Sales  
  - Order Profit Per Order  
  - Late Delivery Flag  

---

## 🧠 Project Workflow

🔧 **1. Data Preprocessing (Python - Colab)**

- Handle missing values  
- Remove irrelevant columns  
- Convert date columns to datetime  
- Feature engineering:

  - Shipping Delay Days  
  - Late Delivery Flag  

📊 **2. Exploratory Data Analysis (EDA)**

- Univariate analysis  
- Bivariate analysis  
- Multivariate analysis  

📈 **3. Power BI Development**

- Data modeling  
- DAX measures creation  
- Interactive dashboard design  

---

## 📊 Dashboard Overview

The dashboard is divided into 4 pages:

1️⃣ **Overview** – Overall business performance  
2️⃣ **Shipping & Delivery Analysis** – Logistics performance  
3️⃣ **Profit & Sales Analysis** – Revenue insights  
4️⃣ **Product / Category Analysis** – Product performance  

---

## 1️⃣ Overview

Main KPIs:

- Total Orders  
- Total Sales  
- Total Profit  
- On-time Delivery Rate  
- Late Delivery Rate  

👉 Provides a **high-level summary of business performance**

<p align="center">
  <img src="https://github.com/user-attachments/assets/cf7f5f49-31bb-4f5c-9ec3-4fe8ed0d7bf0" />
       alt="Supply Chain"
       width="1200">
</p>

---

## 2️⃣ Shipping & Delivery Analysis

Focus on logistics:

- Orders by Shipping Mode  
- Late Delivery by Shipping Mode  
- Shipping Delay Distribution  

👉 Helps identify **delivery inefficiencies**

---

## 3️⃣ Profit & Sales Analysis

Analyze business performance:

- Sales by Market  
- Profit by Region  
- Sales vs Profit comparison  

👉 Identifies **high-performing markets**

---

## 4️⃣ Product / Category Analysis

Analyze product performance:

- Sales by Category  
- Profit by Category  
- Category comparison  

👉 Helps optimize **product strategy**

---

## 💡 Key Insights

🔥 **1. Late Delivery Rate is significantly high (~50%+)**

➡️ Suggestion: Improve logistics system and delivery process  

🔥 **2. Standard Class has the highest number of late deliveries**

➡️ Suggestion: Optimize shipping routes or upgrade shipping options  

🔥 **3. Some regions generate higher profit than others**

➡️ Suggestion: Focus business strategy on high-performing regions  

🔥 **4. Product categories show different profitability levels**

➡️ Suggestion: Prioritize high-profit categories  

---

## 🧠 Key DAX Measures

```DAX
Total Orders = COUNTROWS(Data)
```

```DAX
Total Sales = SUM(Data[sales])
```

```DAX
Total Profit = SUM(Data[order_profit_per_order])
```

```DAX
Late Orders =
CALCULATE(
    COUNTROWS(Data),
    Data[is_late_flag] = 1
)
```

```DAX
On-time Orders =
CALCULATE(
    COUNTROWS(Data),
    Data[is_late_flag] = 0
)
```

```DAX
Late Delivery Rate (%) =
DIVIDE([Late Orders], [Total Orders])
```

```DAX
On-time Delivery Rate (%) =
DIVIDE([On-time Orders], [Total Orders])
```

---

## 📁 Project Structure

```bash
├── powerbi/
│   └── SupplyChain_Dashboard.pbix
├── data/
│   └── DataCoSupplyChainDataset.csv
├── notebook/
│   └── EDA_SupplyChain.ipynb
├── images/
│   └── dashboard.png
└── documents/
    └── report.docx
```

---

## 🔮 Future Improvements

Build **machine learning** model to predict late delivery
Integrate real-time logistics data
Deploy dashboard to **Power BI Service**
Create **automated alerts for late deliveries**

---

## 👨‍💻 Author

Name: **Võ Văn Minh Trí**

Tools: **Power BI, Python, Pandas, Seaborn**

---
