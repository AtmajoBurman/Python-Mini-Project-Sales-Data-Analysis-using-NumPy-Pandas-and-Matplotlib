# Sales Data Analysis with NumPy, Pandas & Matplotlib

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Overview

This project performs a **complete sales data analysis** using Python’s core data science libraries:

- **NumPy** – for numerical operations (mean, median, standard deviation, normalization, etc.)
- **Pandas** – for data loading, cleaning, and aggregation
- **Matplotlib** – for creating insightful visualizations (bar charts, pie charts, line charts, subplots)

The dataset simulates real‑world sales records with intentional **missing values** and **duplicates**, requiring a thorough cleaning process before analysis.

---

## 📊 Dataset

The dataset (`sales_data2.csv`) contains at least 30 rows with the following columns:

| Column    | Description                        |
|-----------|------------------------------------|
| `Date`    | Transaction date (YYYY-MM-DD)      |
| `Product` | Name of the product sold           |
| `Sales`   | Revenue from the transaction       |
| `Region`  | Geographic region of the sale      |

**Characteristics**:
- Missing values in `Sales`, `Product`, and `Region`
- Duplicate rows present

> **Note**: The dataset is included in the `Dataset_CSV_file/` folder. If you wish to use your own data, ensure the same column names.

---
# 📊 Sales Data Analysis  
### NumPy, Pandas & Matplotlib Mini Project  

---

## 📁 Dataset Sample  
**First 5 rows of the generated sales data:**

| Date       | Product    | Sales      | Region   |
|------------|------------|------------|----------|
| 2023-04-13 | Headphones | 54.808505  | Central  |
| 2023-12-15 | Headphones | 202.767649 | North    |
| 2023-09-28 | Keyboard   | 571.297100 | East     |
| 2023-04-17 | Keyboard   | 707.300438 | East     |
| 2023-03-13 | Laptop     | 669.363197 | North    |

---

## 🔧 Steps & Findings  

### 🧮 Part 1: NumPy Operations  
- Converted `Sales` column to a NumPy array.  
- Calculated **mean**, **median**, and **standard deviation** using NumPy.  
- Normalized sales data to a range between 0 and 1.  
- Found top 3 highest sales values and their original DataFrame indices.  

**Top 3 highest sales values:**  
`[990.5511576, 977.05947549, 974.36002701]`  

**Corresponding original DataFrame indices:**  
`[53, 97, 18]`  

- **Mean comparison:** The mean calculated using NumPy matched the Pandas mean (after cleaning), confirming consistency across libraries.

---

### 📂 Part 2: Data Loading & Inspection (Pandas)  
- Loaded the sales dataset into a Pandas DataFrame.  
- Displayed first 5 and last 5 rows.  
- Used `info()` to check data types and non‑null counts, and `describe()` for statistical summary.

---

### 🧹 Part 3: Data Cleaning  
- Converted `Date` column to datetime objects.  
- Handled missing values:  
  - `Sales` → filled with mean of the column.  
  - `Product` / `Region` → filled with `"Unknown"`.  
- Removed duplicate rows.

---

### 📊 Part 4: Data Analysis  
- Calculated **total sales** across the dataset.  
- Aggregated **sales by product** and **sales by region**.  
- Identified:  
  - **Best‑selling product:** `Headphones` (Total Sales: **$11,304.91**)  
  - **Lowest‑performing region:** `Central` (Total Sales: **$3,599.10**)  
- Computed **average sales per product**.

---

### 🎨 Part 5: Visualization (Matplotlib Focus)  

#### Subplots: Sales by Product & Sales by Region  
![Sales by Product and Region](Data%20Plots/Image1.png)
*Bar chart (left) shows total sales per product; pie chart (right) shows regional distribution.*

#### Line Chart: Daily Sales Trend Over Time  
![Daily Sales Trend](Data%20Plots/Image2.png)  
*Daily sales over the entire period with grid and customized styling.*

---

### 📅 Part 6: Time‑Based Analysis  
- Extracted **Month** and **Day** from the `Date` column and added them as new columns.  
- Calculated **monthly total sales** and identified the peak month.  

**Month with the highest sales:** `Month 9` (Total Sales: **$7,834.11**)

#### Monthly Sales Trend  
![Monthly Sales Trend](Data%20Plots/Image3.png)  
*Line plot showing sales per month, highlighting the month with highest revenue.*

---

## 🚀 How to Run  
1. Clone the repository.  
2. Install dependencies: `pip install numpy pandas matplotlib`  
3. Open `Sales_Data_Analysis.ipynb` in Jupyter Notebook and run all cells.  

---

## 📌 Notes  
- All generated graphs are saved in the `images/` folder.  
- The dataset is designed with intentional missing values and duplicates for practice.

---

## 🔮 Future Improvements  
- Add interactive dashboards with Plotly.  
- Include statistical tests (e.g., ANOVA by region).  
- Automate report generation.  

---
**Happy analyzing!** 🚀
---

## 🛠️ Installation & Setup

### 1. Clone the repository

### 2. Create a virtual environment (recommended)
```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```
### 3. Install dependencies
```bash
pip install -r requirements.txt
```
requirements.txt:
```text
numpy
pandas
matplotlib
```
📁 Project Structure
```text
sales-data-analysis/
├── Dataset_CSV_file/
│   └── sales_data.csv          # Dataset
├── Python Notebook/
│   └── Sales_Data_Analysis.ipynb    # Main Jupyter notebook
├── Data Plots/                     # Generated plots 
│   ├── Image1.png
│   ├── Image2.png
│   └── Image3.png
├── README.md                   # This file
└── requirements.txt
```
🚀 Usage
Launch Jupyter Notebook:

```bash
Python Notebook/Sales_Data_Analysis.ipynb
```
---

## 🚀 Running the Analysis

**Run all cells sequentially to:**

1. 🧹 **Load and inspect** the data  
2. 🔧 **Clean** missing values and duplicates  
3. 📐 **Perform NumPy** calculations  
4. 📊 **Aggregate** sales by product, region, and time  
5. 📈 **Generate** visualizations  

All graphs are saved in the `Data Plots/` folder for easy inclusion in reports.  
*(If the folder name causes linking issues, use `Data%20Plots/` or angle brackets in Markdown.)*

---

## 🙌 Acknowledgements

- Dataset generated to simulate real‑world sales records with intentional missing values and duplicates.  
- Inspired by typical business analytics workflows.

---

## 📄 License

This project is licensed under the **MIT License** – feel free to use, modify, and distribute as you like.

---

## 📬 Contact

Have questions or suggestions? Feel free to [open an issue](https://github.com/AtmajoBurman/Python-Mini-Project-Sales-Data-Analysis-using-NumPy-Pandas-and-Matplotlib/issues) or reach out!

---

**Happy analyzing!** 🎯
