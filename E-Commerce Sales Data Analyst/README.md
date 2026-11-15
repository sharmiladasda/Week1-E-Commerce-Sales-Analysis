# E-Commerce Sales Analysis and Visualization

**Internship:** WeIntern Pvt. Ltd. -- Data Science Internship\
**Week:** Week 1\
**Project type:** Data cleaning, exploratory data analysis (EDA), sales
analysis, and visualization
**GitHub Profile:** https://github.com/sharmiladasda

## 1. Project Objective

The objective of this Week 1 project is to clean an e-commerce dataset,
analyze sales and customer-related patterns, calculate key business
performance indicators, and communicate the findings through
visualizations and a Power BI dashboard.

The work covers: - Inspecting and cleaning the raw e-commerce data. -
Checking missing values, duplicate records, and data validity. -
Calculating sales KPIs. - Exploring product categories, monthly sales,
payment modes, cities, and delivery statuses. - Presenting the results
using charts and a dashboard.

## 2. Dataset Description

The project uses an e-commerce transactions dataset containing **50,000
original records**.

The dataset includes fields used for transaction and sales analysis,
such as: - Order ID - Customer ID - Order Date - Product Name -
Category - Quantity - Total Amount - Payment Mode - City - Delivery
Status

The cleaned output contains **48,730 records**. The cleaning workflow
also produced a separate set of **1,270 invalid records** for review. No
exact duplicate rows or repeated Order IDs were identified in the
cleaning output.

> **Data interpretation note:** The reported revenue is calculated by
> summing `Total Amount` across the cleaned records, including all
> delivery statuses. It is therefore treated as **Gross Order Value**,
> not net realized revenue.

## 3. Tools and Libraries Used

### Tools

-   Python
-   Jupyter Notebook / Python script
-   Microsoft Excel
-   Microsoft Power BI

### Python libraries

-   `pandas` -- data loading, cleaning, transformation, and analysis
-   `numpy` -- numerical operations
-   `matplotlib` -- chart creation
-   `seaborn` -- statistical visualization 

Power BI was used to build an interactive dashboard with KPI cards,
charts, and slicers.

## 4. Key Steps Performed

### Task 1 -- Data Cleaning

1.  Loaded and inspected the original dataset.
2.  Reviewed column names, data types, missing values, and basic
    statistics.
3.  Checked for exact duplicate rows and repeated Order IDs.
4.  Applied validation checks to identify invalid records.
5.  Separated invalid records for review.
6.  Exported the cleaned data and supporting audit sheets to an Excel
    workbook.

### Task 2 -- Sales Analysis

Calculated the following key performance indicators: - Gross Order Value
/ Total Revenue - Total Orders - Average Order Value (AOV) - Total Units
Sold - Total Customers - Top revenue-generating category - Top
revenue-generating product

Also explored: - Revenue by product category - Monthly revenue trend -
Payment mode distribution - Revenue by city - Orders by delivery
status - Customer order frequency and repeat-customer contribution

### Task 3 -- Data Visualization

Created visualizations to communicate the analysis: - Bar chart --
revenue by product category - Line chart -- monthly revenue trend - Pie
chart -- payment mode distribution - Dashboard mockup / Power BI
dashboard -- KPI cards and supporting charts

Known category and label variations (for example, `Electronics` /
`Electronic`, `Cancelled` / `Canceled`, and `COD` / `Cash On Delivery`)
were identified. Where applicable, variants were standardized for
analysis or charting; the original workbook values were not necessarily
overwritten.

## 5. Major Findings

The following findings are based on the current cleaned dataset and
analysis:

  Metric                                        Result
  --------------------------------- ------------------
  Original records                              50,000
  Cleaned records                               48,730
  Invalid records set aside                      1,270
  Exact duplicate rows identified                    0
  Repeated Order IDs identified                      0
  Gross Order Value                   ₹16,51,47,406.05
  Total Orders                                  48,730
  Average Order Value                        ₹3,389.03
  Total Units Sold                             146,349
  Distinct Customers                            11,780
  Top revenue category                     Electronics
  Top revenue product                      Smart Watch
  Top product by units sold                 Phone Case

Additional observations: - Electronics generated the highest category
revenue in the analysis. - Smart Watch was the highest-revenue product,
while Phone Case had the highest number of units sold. - Monthly gross
order value varied over the analyzed period. - Repeat customers
accounted for a large share of gross order value in the current
analysis. Customer-level outliers should be reviewed before drawing
strong conclusions from order-frequency comparisons. - Revenue totals
include cancelled and returned records; they should not be interpreted
as completed-sale or net revenue without further filtering and business
rules.

## 6. Folder Structure

The following is a suggested repository structure. Update file names to
match the files actually included in your GitHub repository.

``` text
E-Commerce-Sales-Analysis/
│
├── README.md
│
├── data/
│   ├── raw/
│   │   └── ecommerce_dataset.xlsx
│   └── processed/
│       └── Ecommerce_Cleaning_Output.xlsx
│
├── notebooks/
│   ├── Task1_Data_Cleaning.ipynb
│   └── Task2_Sales_Analysis.ipynb
│
├── scripts/
│   └── sales_analysis.py
│
├── visualizations/
│   ├── 01_revenue_by_category.png
│   ├── 02_monthly_revenue_trend.png
│   ├── 03_payment_mode_share.png
│   └── 04_dashboard_mockup.png
│
├── powerbi/
│   └── Ecommerce_Sales_Dashboard.pbix
│
└── reports/
    └── Week1_Sales_Analysis_Report.pdf
```

## 7. Execution Instructions

### A. Set up the environment

Install Python 3 and the required libraries:

``` bash
pip install pandas numpy matplotlib seaborn openpyxl jupyter
```

### B. Run the data-cleaning and analysis notebook

1.  Clone or download this repository.
2.  Place the original dataset in `data/raw/`.
3.  Open a terminal in the project directory.
4.  Start Jupyter Notebook:

``` bash
jupyter notebook
```

5.  Open the notebooks in the `notebooks/` folder.
6.  Run the cells from top to bottom.
7.  Confirm that the processed Excel workbook and visualizations are
    saved to the intended output folders.

If using a Python script instead of a notebook, run it from the project
root:

``` bash
python scripts/sales_analysis.py
```

Make sure the input and output paths in the notebook or script match
your local folder structure.

### C. Open the Power BI dashboard

1.  Open `powerbi/Ecommerce_Sales_Dashboard.pbix` in Microsoft Power BI
    Desktop.
2.  If prompted, update the source path to the processed Excel workbook.
3.  Select **Refresh** to reload the data.
4.  Use the date, category, city, and payment-mode slicers to interact
    with the dashboard.

## 8. Author Details

-   **Name:** Sharmila Das
-   **Internship Organization:** WeIntern Pvt. Ltd.
-   **Internship Role:** Data Science Intern
-   **Week:** Week 1
-   **GitHub Project:** Week1-E-Commerce-Sales-Analysis
-   **Email:** sharmiladas.da@gmail.com

## 9. Notes and Limitations

-   The dataset's original field values are retained in the source
    workbook; standardization may be applied in analysis or
    visualization steps.
-   Gross Order Value includes all delivery statuses in the current
    calculation. A separate net-sales measure should be defined if
    cancelled and returned orders must be excluded.
-   The folder structure and execution commands are templates. Adjust
    them to the actual filenames and scripts committed to the
    repository.
-   The findings should be rechecked if the dataset, cleaning rules, or
    analysis filters change.
