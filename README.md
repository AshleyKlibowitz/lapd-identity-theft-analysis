# LAPD Identity Theft Statistical Analysis (2023)

## 📊 Project Overview
This project performs a statistical analysis of **10,966 identity theft reports** filed in Los Angeles during 2023. The objective was to determine if victimization rates are statistically correlated with specific demographic factors (Age and Sex) or if they follow a random distribution.

Using **Chi-Square Hypothesis Testing**, I rejected the null hypothesis ($p < 0.05$), confirming a statistically significant relationship between demographic groups and report frequency.

## 🛠️ Tools & Methodology
* **Data Engineering:** OpenRefine (ETL pipeline for cleaning, standardization, and null handling).
* **Statistical Analysis:** Excel (Descriptive Statistics, Kurtosis/Skewness, Chi-Square Test).
* **Visualization:** Excel (Histograms, Bubble Charts).

## 🔍 Key Findings
* **Demographic Skew:** The data distribution is right-skewed (Skewness: 0.89), with victims in their **30s** being the most affected group.
* **Statistical Significance:** Calculated a Chi-Square value of **219.72** (Critical Value: 22.36), resulting in a p-value of $1.19 \times 10^{-39}$.
* **Gender Disparity:** Females in the 25-34 age bracket reported incidents at a rate significantly higher than expected values.

## 📂 Repository Structure
* **`data/`**
  * `lapd_2023_cleaned.csv`: The final processed dataset (10,966 records) exported from OpenRefine.
* **`reports/`**
  * `Executive_Summary.pdf`: The final business report, including the Executive Summary, visualizations, and conclusions.
* **`documentation/`**
  * `Data_Cleaning_Log.pdf`: Detailed documentation of the ETL steps taken in OpenRefine to standardize "Victim Sex" and handle negative/null ages.
* **`analysis/`**
  * `Statistical_Analysis.xlsx`: The Excel workbook containing the raw descriptive statistics, Kurtosis/Skewness calculations, and Chi-Square formulas.

## 🧹 Data Engineering Process
Data integrity was ensured through a rigorous cleaning pipeline documented in `documentation/Data_Cleaning_Log.pdf`. 

**Key Cleaning Steps (OpenRefine):**
1. **Standardization:** Normalized inconsistent "Vict Sex" entries (e.g., mapping 'F', 'f', and 'Fem' to a single standard).
2. **Null Handling:** Identified and removed records with negative ages (-1) or null placeholders (0) to prevent skewing the statistical mean.
3. **Temporal Filtering:** Parsed timestamp data to isolate the 2023 fiscal year, filtering out non-relevant historical data.

## 💾 Data Source
* **Original Source:** [LAPD Crime Data from 2020 to Present](https://catalog.data.gov/dataset/crime-data-from-2020-to-present).
* **Processed Data:** The file `data/lapd_2023_cleaned.csv` in this repository is a filtered extract containing only **Identity Theft** reports from **2023**.
