![MySQL](https://img.shields.io/badge/Database-MySQL-blue)  
![Project Status](https://img.shields.io/badge/Status-Completed-brightgreen)

# E-Commerce-Customer-Churn-Analysis
---

## 🔍 Project Overview

Customer churn is a critical problem for e-commerce platforms, directly impacting revenue and business sustainability.  
This project analyzes a large transactional dataset containing customer behavior and demographic attributes to uncover:

- What factors influence customer churn  
- Which customer segments are at higher risk  
- How purchase behavior, complaints, payment methods, and engagement metrics relate to churn  

---

## 📂 Dataset Description

The dataset includes key attributes such as:

- Tenure  
- Preferred login device  
- City tier  
- Distance from warehouse  
- Preferred payment mode  
- Satisfaction score  
- Complaint history  
- Number of orders, coupons used, order counts  
- Cashback, order amount hike  
- Churn flag  


---

## 🧹 Data Cleaning Steps

Performed as per instructions:

### **Handling Missing Values**
- Mean imputation for:  
  `WarehouseToHome, HoursSpentOnApp, OrderAmountHikeFromlastYear, DaySinceLastOrder`
- Mode imputation for:  
  `Tenure, CouponUsed, OrderCount`
- Removed outliers where `WarehouseToHome > 100`

### **Standardization**
- Replace:
  - "Phone" → "Mobile Phone"  
  - "Mobile" → "Mobile Phone" in order category  
  - "COD" → "Cash on Delivery"  
  - "CC" → "Credit Card"

### **Column Renaming**
- `PreferedOrderCat` → `PreferredOrderCat`  
- `HourSpendOnApp` → `HoursSpentOnApp`

### **New Columns Created**
- `ComplaintReceived` (Yes/No based on `Complain`)  
- `ChurnStatus` (Churned/Active based on `Churn`)

### **Columns Dropped**
- `Churn`  
- `Complain`

---

## 📊 Data Exploration & Analysis

Key SQL analyses include:

- Count of churned vs. active customers  
- Average tenure & cashback for churned customers  
- Percentage of churned customers who complained  
- Gender distribution among customers who complained  
- Most preferred payment mode among active customers  
- City tier with highest churn in “Laptop & Accessory” category  
- Total order amount hike among single customers using mobile phone orders  
- Average devices registered for UPI users  
- Category-wise max hours spent on the app  
- Average satisfaction score of customers who complained  
- Top 3 categories with highest average cashback  
- Distance-based churn categorization  
- Customer + return details for those who churned and complained  

---

## 📦 Additional Table: Customer Returns

A new table `customer_returns` was created and populated with return records.  
Join queries were written to display return details of customers who:

- **Churned** and  
- **Had complaints**

---

## 📈 Outcome & Insights

This analysis helps identify:

- Which customers are more likely to churn  
- Behavioral patterns that signal dissatisfaction  
- Payment modes & ordering patterns linked to churn  
- High-risk customer groups for targeted retention strategies  

---

## 🚀 How to Use This Repository

1. Clone or download the repository.  
2. Open MySQL Workbench or CLI.  
3. Run the SQL script inside the **sql/** folder.  
4. Follow the cleaning, transformation, and analysis steps described in the PDF.  
5. Execute the queries to generate insights.

---








