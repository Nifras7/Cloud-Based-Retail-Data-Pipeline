# 🛒 Cloud-Based Retail Data Pipeline

An end-to-end Data Engineering project that demonstrates how raw retail sales data can be transformed into actionable business insights using modern data warehousing and analytics techniques.

---

## 📌 Project Overview

This project builds a complete retail analytics pipeline that:

* Ingests raw retail sales data
* Cleans and transforms data using Python
* Stores processed data in a Data Lake
* Loads dimensional models into Snowflake
* Generates business insights through Power BI dashboards

The architecture follows industry-standard Data Engineering and Business Intelligence practices.

---

## 🚀 Tech Stack

| Category        | Tools            |
| --------------- | ---------------- |
| Programming     | Python           |
| Data Processing | Pandas, NumPy    |
| Data Storage    | Data Lake (CSV)  |
| Data Warehouse  | Snowflake        |
| Data Modeling   | Star Schema      |
| Visualization   | Power BI         |
| Development     | Jupyter Notebook |

---

## 🏗️ Architecture

```text
Raw Retail Dataset
        │
        ▼
   Data Lake (Raw)
        │
        ▼
    Python ETL
        │
        ▼
 Data Lake (Processed)
        │
        ▼
    Snowflake DW
        │
        ▼
   Power BI Dashboard
```

---

## 📂 Project Structure

```text
Cloud-Based-Retail-Data-Pipeline/
│
├── sales_data_lake/
│   ├── raw/
│   └── processed/
│
├── transform/
│   └── etl.ipynb
│
├── snowflake/
│   └── snowflake_queries.sql
│
├── dashboard/
│   └── Retail_Dashboard.pbix
│
├── screenshots/
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## 🔄 ETL Workflow

### 1️⃣ Extract

Raw retail transaction data is loaded from the source dataset.

### 2️⃣ Transform

Data preprocessing includes:

* Removing duplicates
* Handling missing values
* Date formatting
* Data type conversion
* Feature engineering
* Data quality validation

### 3️⃣ Load

Processed data is loaded into Snowflake using a dimensional model.

---

## 🏢 Data Warehouse Design

### Fact Table

**FACT_SALES**

Measures:

* Revenue
* Quantity Sold
* Profit

### Dimension Tables

* DIM_DATE
* DIM_PRODUCT
* DIM_CATEGORY
* DIM_CUSTOMER
* DIM_MONTH
* DIM_YEAR

### Star Schema

```text
              DIM_DATE
                  |
                  |
DIM_PRODUCT --- FACT_SALES --- DIM_CUSTOMER
                  |
                  |
            DIM_CATEGORY
```

---

## 📊 Power BI Dashboard

The dashboard provides:

* Sales Performance Analysis
* Revenue Trends
* Category-wise Sales
* Customer Insights
* Monthly & Yearly Growth
* KPI Tracking

### Key KPIs

* Total Revenue
* Total Orders
* Average Order Value
* Monthly Growth %
* Top Performing Categories

---

## 📈 Business Questions Answered

* Which product category generates the highest revenue?
* What are the monthly sales trends?
* Who are the highest-value customers?
* Which periods show peak sales activity?
* What is the average transaction value?

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/cloud-based-retail-data-pipeline.git
cd cloud-based-retail-data-pipeline
```

### Create Virtual Environment

```bash
python -m venv venv
```

Activate:

Windows

```bash
venv\Scripts\activate
```

Linux/Mac

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Launch Notebook

```bash
jupyter notebook
```

---

## 🔐 Security & Credential Management

### Never Commit Secrets

Do not commit:

* Snowflake Credentials
* API Keys
* Access Tokens
* Passwords
* Connection Strings

### Use Environment Variables

```python
import os

SNOWFLAKE_USER = os.getenv("SNOWFLAKE_USER")
SNOWFLAKE_PASSWORD = os.getenv("SNOWFLAKE_PASSWORD")
SNOWFLAKE_ACCOUNT = os.getenv("SNOWFLAKE_ACCOUNT")
```

### Example .env

```env
SNOWFLAKE_USER=your_username
SNOWFLAKE_PASSWORD=your_password
SNOWFLAKE_ACCOUNT=your_account
```

### Load Environment Variables

```python
from dotenv import load_dotenv

load_dotenv()
```

---

## 🛡️ Data Integrity Controls

Implemented validations:

* Duplicate Detection
* Missing Value Checks
* Data Type Validation
* Referential Integrity Checks
* Consistent Date Formats
* ETL Validation Rules

These controls ensure reliable and trustworthy analytics.

---

## 📸 Dashboard Screenshots

Add your Power BI dashboard screenshots here:

```markdown
![Dashboard](screenshots/dashboard1.png)
```

```markdown
![Dashboard](screenshots/dashboard2.png)
```

---

## 🔮 Future Enhancements

* Apache Airflow Orchestration
* AWS S3 Data Lake
* Snowpipe Automation
* Incremental Loading
* CI/CD Pipeline
* Real-Time Data Streaming
* Advanced Analytics & Forecasting

---

## 👨‍💻 Author

**Mohamed Nifras**

Data Analyst | Aspiring Data Engineer

### Skills

* SQL
* Python
* Pandas
* Power BI
* Snowflake
* Data Warehousing
* ETL Development
* Data Modeling


---

## 📜 License

This project is licensed under the MIT License.

Feel free to fork, improve, and contribute.
