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
  These variables showed minimal difference in purchase behaviour. They are unlikely to be useful for targeted marketing.
- Gender
- Home Ownership

## 7. Deeper Analysis
Here, analysis moved beyond individual variable performance to identify which combinations of customer characteristics produce the highest bike purchase likelihood.

### Approach
- A Master Pivot Table with slicers was built using a binary Purchase Flag helper column to enable dynamic combination testing
- Combinations were tested systematically in pairs, then narrowed to groups of three and four variables using a Combined Rank Score based on segment size and purchase rate
- Final segments were then tested across all three regions

### Final Customer Segments Identified

#### A. Primary Target Profile
Middle to high income customers, aged 30–49, owning 0–1 cars, commuting 0–5 miles
- Overall purchase rate: 71% across 180 customers

#### B. Secondary Target Profile 
Single customers, aged 30–49, owning 0–1 cars, commuting 0–5 miles
- Overall purchase rate: 70% across 113 customers

### Regional Performance Summary

| Segment | Region | Purchase Rate | Segment Size |
|---|---|---|---|
| Primary Target | North America | 63% | 101 |
| Primary Target | Europe | 83% | 50 |
| Secondary Target | North America | 69% | 46 |

## 8. Insights & Recommendations

Deeper Analysis identified two high converting customer profiles and three priority regional markets to guide the company's marketing and expansion strategy.

### A. North America is the Largest Market with Highest Growth Potential
- North America has the largest customer base of 508 but the lowest regional purchase rate of 43%. Yet the Primary Target Profile converts at 63% across 101 customers  and Secondary at 69% with 46 customers, both well above the regional baseline, revealing strong hidden potential beneath a weak average.

  #### Recommendation
- Targeted marketing should be directed specifically at the Primary and Secondary Target Profiles rather than broad campaigns.
- Further investigation is needed to understand why over half of North America's 508 customers leave without purchasing bikes.          Possible areas to examine are stock availability, pricing and in-store experience.

### B. Europe has Strong Conversion and Notable Room to Grow
- The Primary Target Profile delivers 83% purchase rate across 50 customers in Europe, a 34% point lift above the 49% regional          baseline. Although highly convertible it is currently a smaller market.

  #### Recommendation
- Marketing efforts in Europe should be scaled, with focus on the Primary Target Profile
- Factors driving North America's larger customer base should be investigated to assess whether they can be replicated in Europe to     grow its market size.

### C. Primary Target Profile is a Core Segment to Protect and Scale
- Middle to high income customers aged 30-49, with 0-1 cars and 0-5 mile commutes consistently deliver the strongest purchase rates     across all regions.

  #### Recommendation
- Marketing campaigns should position bikes as a practical and cost efficient commuting solution for economically active adults.
- Loyalty programmes can also be introduced to protect and grow repeat purchases within this segment

### D. Secondary Target Profile has Untapped Acquisition Opportunity
- Single adults aged 30-49 with low car ownership within 0-5 mile commutes convert at 69% across 46 customers in North America          reflecting 26% points above the regional baseline.

  #### Recommendation
- Acquisition campaigns emphasising independence and lifestyle benefits of cycling in North America should be launched and targeted     at this profile.
- A combined campaign strategy covering both primary and secondary profiles simultaneously in North America can also be considered      for cost efficiency.

### E.  Pacific Current Performance should be Sustained
- Pacific has the highest regional baseline at 59% but the smallest customer base of 192 with segment sizes too small for reliable      targeted expansion.

 #### Recommendation
- Current performance should be maintained while channeling focus on organically growing the Pacific customer base, before committing   to targeted expansion investment.

