# 🛒 Fetch Data Analysis Assignment

## Project Overview
This repository contains an end-to-end data analysis project for Fetch Rewards. The project involves data cleaning, exploratory analysis, and generating business insights from transactions, user behavior, and product sales.

The dataset consists of three key files: **Users, Transactions, and Products**, which have been cleaned and processed for insights.

---

## 📂 Dataset Details
The project includes the following datasets:

- **Users.csv** (Compressed as `.zip` for storage efficiency)
- **Transactions.csv** (Compressed as `.zip`)
- **Products.csv** (Compressed as `.zip`)

### **Columns in Each Dataset**
#### 🧑 Users Data:
| Column | Description |
|--------|------------|
| ID | Unique User ID |
| BIRTH_DATE | User's Birthdate |
| STATE | User's State |
| LANGUAGE | Preferred Language |
| GENDER | Gender Information |

#### 💰 Transactions Data:
| Column | Description |
|--------|------------|
| RECEIPT_ID | Unique Receipt Identifier |
| PURCHASE_DATE | Date of Transaction |
| SCAN_DATE | Date of Receipt Scan |
| STORE_NAME | Store where purchase was made |
| USER_ID | Linked User ID |
| BARCODE | Product Barcode |
| FINAL_QUANTITY | Quantity Purchased |
| FINAL_SALE | Sale Value of the Transaction |

#### 🏷️ Products Data:
| Column | Description |
|--------|------------|
| CATEGORY_1 | Product's Main Category |
| CATEGORY_2 | Subcategory Level 1 |
| CATEGORY_3 | Subcategory Level 2 |
| CATEGORY_4 | Subcategory Level 3 |
| MANUFACTURER | Manufacturer Name |
| BRAND | Brand Name |
| BARCODE | Unique Product Barcode |

---

## 🔍 Data Cleaning Process
### **1️⃣ Handling Missing Values**
- Replaced missing **birthdates** using the median birth year.
- Filled missing **store names** with `"Unknown Store"`.
- Replaced `"Unknown"` values in the **BRAND** column with the most common brand in the same **CATEGORY_1**.
- Dropped transactions with missing **USER_ID** or **BARCODE** since they are essential.

### **2️⃣ Data Type Standardization**
- Converted `PURCHASE_DATE` and `BIRTH_DATE` to **datetime format**.
- Ensured numerical columns like `FINAL_SALE` and `FINAL_QUANTITY` were correctly formatted.

---

## Key Insights from Analysis
### **1️⃣ Top 5 Brands by Receipts Scanned Among Users 21 and Over**
- Identified the most popular brands preferred by users over **21 years old**.

### **2️⃣ Power Users**
- Discovered that the **top 10% of users** account for nearly **50% of all transactions**, highlighting strong brand loyalty.

### **3️⃣ Top 5 Most Purchased Product Categories**
- Found the highest-selling product categories based on total quantity sold.

### **4️⃣ Revenue Trends**
- Visualized **daily revenue trends** to understand sales fluctuations over time.

### **5️⃣ Store Performance**
- Ranked the **top-performing stores** based on total revenue.

📊 **All findings were visualized using Python (Matplotlib & Seaborn).**

---

##  How to Run the Project
1. **Clone the repository**
   ```sh
   git clone https://github.com/your-username/fetch_assesment.git
   cd fetch_assesment
   ```
2. **Extract the Data Files**
   ```sh
   unzip data
   ```
3. **Run Jupyter Notebook**
   ```sh
   jupyter notebook Fetch_Assignment.ipynb
   ```

---

##  Next Steps
- Enhance data visualization with **Tableau or Power BI**.
- Implement **machine learning models** for user segmentation.
- Improve **data pipeline automation**.

---
