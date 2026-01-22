# LAPD Identity Theft Statistical Analysis (2023)

## 📊 Project Overview
This project performs a statistical analysis of **10,966 identity theft reports** filed in Los Angeles during 2023. The objective was to determine if victimization rates are statistically correlated with specific demographic factors (Age and Sex) or if they follow a random distribution.

Using **Chi-Square Hypothesis Testing**, I rejected the null hypothesis ($p < 0.05$), confirming a statistically significant relationship between demographic groups and report frequency.

## 🛠️ Tools & Methodology
* [cite_start]**Data Engineering:** OpenRefine (ETL pipeline for cleaning, standardization, and null handling)[cite: 853, 908].
* [cite_start]**Statistical Analysis:** Excel (Descriptive Statistics, Kurtosis/Skewness, Chi-Square Test)[cite: 911].
* [cite_start]**Visualization:** Excel (Histograms, Bubble Charts)[cite: 934, 1052].

## 🔍 Key Findings
* [cite_start]**Demographic Skew:** The data distribution is right-skewed (Skewness: 0.89), with victims in their **30s** being the most affected group[cite: 931, 1062].
* [cite_start]**Statistical Significance:** Calculated a Chi-Square value of **219.72** (Critical Value: 22.36), resulting in a p-value of $1.19 \times 10^{-39}$[cite: 999, 1000].
* [cite_start]**Gender Disparity:** Females in the 25-34 age bracket reported incidents at a rate significantly higher than expected values[cite: 1024].

## 📂 Repository Structure
* **`data/`**
  * [cite_start]`lapd_2023_cleaned.csv`: The final processed dataset (10,966 records) exported from OpenRefine[cite: 853].
* **`reports/`**
  * [cite_start]`Executive_Summary.pdf`: The final business report, including the Executive Summary, visualizations, and conclusions[cite: 840].
* **`documentation/`**
  * [cite_start]`Data_Cleaning_Log.pdf`: Detailed documentation of the ETL steps taken in OpenRefine to standardize "Victim Sex" and handle negative/null ages[cite: 898].
* **`analysis/`**
  * [cite_start]`Statistical_Analysis.xlsx`: The Excel workbook containing the raw descriptive statistics, Kurtosis/Skewness calculations, and Chi-Square formulas[cite: 911].

## 🧹 Data Engineering Process
Data integrity was ensured through a rigorous cleaning pipeline documented in `documentation/Data_Cleaning_Log.pdf`. 

**Key Cleaning Steps (OpenRefine):**
1. [cite_start]**Standardization:** Normalized inconsistent "Vict Sex" entries (e.g., mapping 'F', 'f', and 'Fem' to a single standard)[cite: 904].
2. [cite_start]**Null Handling:** Identified and removed records with negative ages (-1) or null placeholders (0) to prevent skewing the statistical mean[cite: 905].
3. [cite_start]**Temporal Filtering:** Parsed timestamp data to isolate the 2023 fiscal year, filtering out non-relevant historical data[cite: 900].

## 💾 Data Source
* [cite_start]**Original Source:** [LAPD Crime Data from 2020 to Present](https://catalog.data.gov/dataset/crime-data-from-2020-to-present)[cite: 865, 867].
* **Processed Data:** The file `data/lapd_2023_cleaned.csv` in this repository is a filtered extract containing only **Identity Theft** reports from **2023**.
