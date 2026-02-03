# Sales Analysis Notebook

## Overview

This project contains a Jupyter Notebook (`sales_analysis.ipynb`) that performs basic data cleaning, transformation, and exploratory analysis on a sales dataset stored in an Excel file. The notebook demonstrates common data analyst workflows using **pandas**, **NumPy**, and **matplotlib**.

The goal is to clean raw sales data, derive a revenue metric, and summarize sales performance by product.

---

## Files in This Repository

* **sales_analysis.ipynb** – Main analysis notebook
* **sales_training_data.xlsx** – Input dataset (expected Excel file)
* **README.md** – Project documentation (this file)

---

## Tools & Libraries Used

* Python 3
* pandas
* NumPy
* matplotlib

---

## Data Description (Expected Columns)

The notebook assumes the Excel file contains at least the following columns:

* **Date** – Date of the transaction
* **Product** – Product name or ID
* **Units** – Number of units sold
* **Price** – Price per unit

Additional columns may exist and will be preserved during processing.

---

## Analysis Steps

### 1. Load Data

* Reads an Excel file into a pandas DataFrame
* Displays basic structure, column names, data types, and shape

### 2. Data Inspection

* Uses `describe()` to generate summary statistics
* Checks for missing values

### 3. Data Cleaning

* Removes rows with null values
* Removes duplicate records
* Verifies that no NaN values remain

### 4. Feature Engineering

* Converts the **Date** column to a datetime format
* Creates a new **Revenue** column using:

  `Revenue = Units × Price`

### 5. Aggregation & Summary

* Groups data by **Product**
* Calculates total revenue per product

---

## Example Output

* Cleaned dataset with a new **Revenue** column
* Aggregated revenue totals by product
* Summary statistics for numerical fields

---

## How to Run the Notebook

1. Install dependencies:

   ```bash
   pip install pandas numpy matplotlib
   ```

2. Place `sales_training_data.xlsx` in the expected path or update the file path in the notebook.

3. Open the notebook:

   ```bash
   jupyter notebook sales_analysis.ipynb
   ```

4. Run all cells from top to bottom.

---

## Notes

* File paths may need adjustment if running locally versus Google Colab.
* The notebook is structured for learning and demonstration purposes.
* Suitable for entry-level data analysis practice and interview prep.

---

## Future Improvements

* Add visualizations (bar charts, trend lines)
* Parameterize file paths
* Add error handling and data validation
* Export cleaned and aggregated outputs to CSV
