# Bike-Buyers-Analysis-v2

## 1. Introduction

This project explores customer data from a bike retail company to understand who is most likely to purchase bikes and where growth opportunities exist.

The goal is to use data to move from guessing customers to clearly identifying the most promising customer segments for targeted marketing and expansion.

This project follows a full analytics workflow:

Data Cleaning → Exploratory Data Analysis → Deeper Analysis → Insights → Recommendations.

## 2. Problem Statement

A bike retail company wants to increase sales and expand market share but lacks clarity on:
- Who its most valuable customers are
- Which regions present the biggest growth opportunities
- Which customer segments should be prioritised for marketing

The company needs data-driven insights to identify high-potential customer segments and guide smarter targeting decisions.

## 3. Project Objective
This analysis explores demographic, socioeconomic and lifestyle factors that influence bike purchase behaviour.

The aim is to support:
- Customer segmentation
- Regional targeting
- Marketing and growth strategy

### Assumptions
Since no background information was provided with the dataset, the following assumptions were made:
- The dataset represents historical customer data from a bike retail company
- The company’s goal is to increase bike sales through better customer targeting
- The dataset contains both bike buyers and non-buyers
- Insights are intended to support marketing and segmentation decisions

## 4. Dataset Overview 
The cleaned dataset contains:
- 1,000 customer records
- 13 variables
Each row represents a customer and whether they purchased a bike.
### Target Variable
The main variable of interest is Bike Purchase (Yes/No).

Out of 1,000 customers:
- 481 purchased a bike
- 519 did not purchase a bike
  
This means the dataset is well balanced, which makes it suitable for analysis and segmentation.
### Variables in the dataset
The dataset includes customer:
- **Demographics:** Age, Gender, Marital Status, Region
- **Socioeconomic Information:** Income, Education, Occupation
- **Lifestyle & Household Factors:** Number of Cars, Number of Children, Home Ownership, Commute Distance
### Data Source
Public practice dataset from Alex The Analyst (YouTube), used for educational and portfolio purposes.

## 5. Data Cleaning & Preparation
- Using customer ID as unique identifier, 26 duplicates were identified and removed
- Income was grouped into income brackets to make analysis easier and more meaningful
- Age was grouped into age bands to help reveal patterns better
- All other data quality checks and data structure were confirmed to be correct and consistent.
- No outliers were identified, all values fall within realistic ranges.

The tools/functions used were: pivot table count to check duplicates, manual validation using sorting and filtering.

## 6. Exploratory Data Analysis (EDA)
The goal of EDA was to understand which customer characteristics influence bike purchase behaviour.

Each variable in the dataset was compared against the target variable Bike Purchase using pivot tables and purchase rates.

For every variable, two things were evaluated:
- Segment size → how large each customer group is
- Purchase rate → how likely customers in each group are to buy bikes

This helped distinguish between:
- High purchase volume (large customer groups)
- High purchase likelihood (true target segments)
### Key Patterns Observed
#### A. Strong Drivers of Bike Purchase
These variables showed clear and actionable differences in purchase likelihood. They strongly indicate lifestyle and usage behaviour.
- Age
- Marital Status
- Number of Cars Owned
- Commute Distance
#### B. Moderate Drivers
These variables showed meaningful patterns but overlap with stronger lifestyle factors.
- Region
- Income
- Education & Occupation
- Number of Children
#### C. Weak Drivers
  These variables showed minimal difference in purchase behaviour. They are unlikely to be useful for targeted marketing. They are unlikely to be useful for targeted marketing.
- Gender
- Home Ownership
  








