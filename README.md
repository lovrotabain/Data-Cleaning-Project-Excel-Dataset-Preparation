# Data-Cleaning-Project-Excel-Dataset-Preparation

## Overview
This project focuses on **cleaning and preparing a raw Excel dataset** to make it suitable for further analysis and use in tools such as **SQL databases** and **Python (pandas)**.

The main objective was not only to clean the data, but to demonstrate **data quality decision-making** — identifying what data should be kept, corrected, standardised, or transformed to ensure consistency, accuracy, and usability.

---

## Objectives
- Improve overall data quality and consistency
- Prepare the dataset for downstream use in SQL and Python
- Apply Excel data-cleaning functions in a structured and intentional way
- Demonstrate reasoning behind cleaning decisions

---

## Key Data Cleaning Decisions

### Column Review & Retention
- Reviewed all columns to assess relevance and data completeness
- Retained columns that added analytical or contextual value
- Ensured column names were clear and suitable for database usage

---

### Text Cleaning & Standardisation
To ensure consistent text values across the dataset, the following Excel functions and filters were applied:

- Corrected inconsistent categorical values using filtering (e.g. `Republicans` → `Republican`)

  <img width="321" height="415" alt="Screenshot 2026-01-20 134937" src="https://github.com/user-attachments/assets/baf259b0-787c-4b62-b374-3447b8914c18" />


- **`TRIM()`**
  - Removed leading, trailing, and unnecessary spaces
  - Prevented issues with duplicate values caused by hidden whitespace
    
 
  <img width="421" height="212" alt="trim function" src="https://github.com/user-attachments/assets/33131317-bd1b-4b19-9da0-08b8e0578d36" />


- **`PROPER()`**
  - Standardised text formatting (e.g. names and titles)
  - Improved readability and consistency across records
 

    <img width="423" height="143" alt="image" src="https://github.com/user-attachments/assets/59e2414a-c3b3-4831-bc62-fb1c09514feb" />

### Duplicate Handling
- Identified and removed duplicate records using Excel filtering
- Ensured each row represented a unique and valid data entry

### Currency & Numeric Conversion
- Removed currency symbols by converting from currency → number
- Converted values into numeric data types for compatibility with SQL and Python

  <img width="423" height="311" alt="Screenshot 2026-01-20 140514" src="https://github.com/user-attachments/assets/8719085f-e7f5-472b-a33b-d28abdba0d83" />


### Date conversion 
- Successfully standardised date formats by converting long date values to a consistent short date format, ensuring compatibility with SQL databases.

  <img width="422" height="122" alt="convert to short date" src="https://github.com/user-attachments/assets/63a31ca3-20cc-48f4-a297-08db6f43a830" />



This ensures:
- Values can be aggregated using `SUM`, `AVG`, etc.
- The dataset can be reliably imported into **SQL databases**
- The data is compatible with **Python-based analysis (pandas, NumPy)**


These steps help prevent grouping and filtering errors when importing data into SQL or Python.

---


## Why This Matters for SQL & Python
Cleaning the data at the Excel stage:
- Prevents type errors when loading into SQL tables
- Ensures numeric columns behave correctly in queries
- Reduces preprocessing time when working in Python
- Improves reliability of analysis and reporting

This approach reflects real-world data workflows, where clean input data is essential for accurate outputs.

---

## Tools Used
- **Microsoft Excel**
  - Text functions: `TRIM`, `PROPER`
  - Data type conversion
  - Manual data validation and review
  - Filtering

---

## Key Learnings
- Data cleaning requires **judgement**, not just functions
- Small formatting issues can cause large downstream problems
- Preparing data correctly early improves efficiency in later analysis
- Excel remains a powerful tool for initial data preparation

---

## Next Steps
- Import the cleaned dataset into SQL for querying
- Use Python (pandas) for further analysis or visualisation
- Apply similar cleaning techniques to larger or less structured datasets
