# SWYNEX Internship — Task 1: Data Cleaning & Preparation

## 1. Project Overview

This project focuses on cleaning and preparing a raw Indian retail sales dataset using Python, Pandas, and NumPy. The objective was to improve data quality, handle missing values, standardize inconsistent data, validate numerical ranges, and prepare the dataset for further analysis.

## 2. Tools and Technologies

- Python
- Pandas
- NumPy
- Jupyter Notebook
- Visual Studio Code

## 3. Dataset Overview

The dataset contains retail order information, including customer details, product information, quantities, prices, discounts, sales, profit, shipping costs, satisfaction ratings, and order statuses.

- Original dataset: 4,310 rows and 21 columns
- Final cleaned dataset: 4,200 rows and 21 columns
- Output file: `data/cleaned_dataset.csv`

## 4. Data Cleaning Performed

1. Removed completely empty rows.
2. Removed duplicate records.
3. Standardized categorical text and gender values.
4. Converted order dates from multiple formats into a consistent datetime format.
5. Validated customer ages and replaced invalid values with missing values.
6. Imputed missing ages using the median.
7. Validated quantities, replacing zero, negative, and suspicious values with missing values before median imputation.
8. Filled missing discounts using the median discount.
9. Validated customer satisfaction ratings against the 1–5 scale while retaining missing ratings.
10. Standardized order-status capitalization.
11. Validated shipping times using a provisional 1–30 day range and retained unknown values as missing.
12. Replaced negative shipping costs with missing values.
13. Converted whole-number columns to appropriate integer data types.
14. Performed final data-quality checks and exported the cleaned dataset.

## 5. Missing-Value Decisions

- Age: invalid and missing values were replaced using the median age.
- Quantity: invalid and missing values were replaced using the median quantity.
- Discount: missing values were replaced using the median discount.
- Customer satisfaction: missing ratings were retained because unknown ratings should not be fabricated.
- Shipping time: missing or out-of-range values were retained as missing.
- Shipping cost: negative values were replaced with missing values.

## 6. Data-Quality Limitation

The recorded `sales_amount` values frequently differed from estimates calculated using quantity, unit price, and discount. The original calculation method could not be confirmed, so recorded sales amounts were preserved rather than overwritten. This discrepancy should be investigated before using the dataset for financial reporting.

The chosen validation ranges are assumptions for this learning project and should be confirmed against authoritative business rules when available.

## 7. Final Output

The cleaned dataset is saved as `data/cleaned_dataset.csv`. The original raw dataset remains unchanged.

## 8. Learning Outcomes

- Data inspection and profiling
- Missing-value handling
- Duplicate removal
- Categorical standardization
- Date parsing
- Numerical validation and outlier investigation
- Data-type conversion
- Exporting cleaned datasets
- Documenting data-quality decisions
S