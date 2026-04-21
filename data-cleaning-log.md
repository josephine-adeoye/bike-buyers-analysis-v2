# **DATA CLEANING LOG**

This file documents the steps taken to prepare the dataset before analysis.

**DATASET OVERVIEW**

The dataset is a customer dataset, not a transaction dataset.
Each row represents a unique customer record and includes demographic, lifestyle and socioeconomic attributes.

**1. STRUCTURAL CLEANING**

Irrelevant Columns:

All columns were reviewed and retained because they support the project’s analysis goals.

Duplicate Records:

CustomerID was assumed to be a unique identifier.

Using a Pivot Table count check:

a) 26 duplicate records were identified.

b) Random samples were manually inspected.

c) Duplicates were confirmed to be exact full-row duplicates.

**Action taken:**
All duplicate rows were removed.

Assumption:
Duplicates were likely caused by data entry or system duplication and removing them does not remove unique customer information.


**2. DATA QUALITY CHECKS**

Manual validation was performed using sorting and filtering.

**Missing Values:**

No missing values were found across the dataset.

**Inconsistent Formatting:**

No inconsistent formats detected in numeric or categorical columns.

**Incorrect Data Inputs:**

No obvious incorrect values were observed.

**Hidden / Extra Characters:**

No hidden characters detected during filtering and sorting checks.


**3. OUTLIERS CHECKS**

Outlier checks were performed on key numeric variables:

a) Age

b) Monthly Income

c) Number of Children

d) Number of Cars Owned

e) Commute Distance

Values were sorted and reviewed from smallest to largest.

**Result:**

All values fall within realistic ranges. No extreme outliers were identified.


Cleaning Outcome
The dataset is considered clean and ready for exploratory data analysis (EDA).
