# Retail-Orders-Data-Analysis-Sales-Performance-Growth
Retail Orders Data Analysis (2022-2023): An E2E project using Python (Pandas/Matplotlib) and MySQL to analyze sales. It covers ETL, advanced SQL querying (Top 10 Products, Regional Leaders), and visualization of trends like Month-over-Month Growth and the 79% sales growth in the Supplies sub-category. Demonstrates full data pipeline proficiency.




# 🛍️ Retail Orders Data Analysis: Sales Performance & Growth (2022-2023)

## 🌟 Project Overview
This project is a comprehensive **end-to-end data analysis** of a retail orders dataset, covering performance and growth metrics from 2022 and 2023. It showcases a complete analytics pipeline, starting from data cleaning and transformation to advanced querying and professional visualization.

The analysis is driven by key business questions, demonstrating proficiency in integrating **Python** for ETL and visualization with **MySQL** for scalable data management and complex analytical processing.

## 💻 Technologies Used
| Tool/Library | Purpose |
| :--- | :--- |
| **Python** | Primary scripting language. |
| **Pandas** | Data cleaning, transformation, and feature engineering (calculating profit/sale price). |
| **MySQL** | Database for data storage and execution of complex SQL queries. |
| **SQLAlchemy/PyMySQL** | Connector for bridging Python (Pandas) and the MySQL database. |
| **Matplotlib** | Generating all visualizations (line charts, bar charts) for reporting. |
| **SQL** | Advanced querying using **CTEs**, **Window Functions** (`ROW_NUMBER()`), and **Conditional Aggregation** (`CASE` statements). |

---

## 🔑 Key Business Insights & Findings

The project answers the following strategic questions, with results derived directly from the MySQL database and visualized in Python:

### 1. Top 10 Revenue Products
Identified the highest revenue contributors, which are critical for inventory focus.
* **Top Product:** **TEC-CO-10004722**, generating over **\$60K** in sales.

### 2. Top 5 Selling Products in Each Region
A regional breakdown for localized sales strategy.
* The same product, **TEC-CO-10004722**, is the top seller in the **West** region ($\approx \$30K$ sales for that product alone in the region).

### 3. Month-over-Month (MoM) Sales Comparison (2022 vs 2023)
Tracking annual sales growth and seasonal stability.
* **Peak Sales:** **February 2023** showed an exceptional performance, significantly exceeding February 2022.
* **Anomaly:** **November 2023** sales dropped sharply compared to November 2022, highlighting an area for investigation.

### 4. Highest Sales Month per Category
Determined the optimal timing for category-specific promotions.
* **Technology** peaked in **Oct-2023** ($\approx \$53K$ sales).
* **Office Supplies** peaked in **Feb-2023** ($\approx \$44.1K$ sales).

### 5. Highest Sales Growth Sub-Category (2023 vs 2022)
Measured year-over-year performance to identify hyper-growth segments.
* The **Supplies** sub-category achieved the highest sales growth at **$79.16\%$** (from $\$$16,140.7 to $\$$28,917.4).

---

## 🚀 Analytical Pipeline
The project follows a rigorous, multi-step process:

1.  **Data Cleaning & ETL (Python/Pandas):**
    * Read CSV, handling specific null values (`Not Available`, `unknown`).
    * Standardized column names (lowercase, underscores).
    * Derived new fields: `discount`, `sale_price`, and `profit`.
    * Converted `order_date` to the correct datetime format.

2.  **Database Loading (SQLAlchemy):**
    * The cleaned DataFrame was pushed to a MySQL database table named `df_orders`.

3.  **Data Analysis (MySQL/SQL):**
    * Five distinct analytical SQL queries were executed against the `df_orders` table to extract the required insights.

4.  **Visualization & Reporting (Matplotlib):**
    * Query results were pulled back into Python to generate high-impact visuals (as seen in the project output).

---

## 🛠️ Setup and Execution

To run this project locally, you will need the following:

### Prerequisites
* Python 3.x
* A running **MySQL Server** instance.
* The project CSV file (`orders.csv`).

### Installation
Install the necessary Python dependencies:
```bash
pip install pandas matplotlib sqlalchemy pymysql


###
**Configuration**
You must update the database connection string in the Python script (your_script_name.py) to match your local credentials:


# UPDATE THIS LINE in your code
engine = create_engine("mysql+pymysql://root:[YOUR_PASSWORD]@[YOUR_HOST]:3306/retail_orders")
