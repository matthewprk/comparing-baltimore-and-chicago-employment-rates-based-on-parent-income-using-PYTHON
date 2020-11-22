# comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON
This repository contains data analysis comparing Baltimore City's and Chicago's employment rates based on parent income. Analysis was conducted using Python. 

## Background
For this project, I chose to analyze Baltimore City, MD and Chicago, IL (hometown). 
The explored metric is employment rates (%) based on parent income (high, medium, and low). This is interesting to me, because I wanted to know if parent income can have an effect on employment rates and whether preconceptions about economic disparities hold true. 

## Business Question
How does parent income contribute to employment rates in Baltimore and Chicago and what are the key differences between the two cities?

## Data Analysis

### Data Sources

#### Baltimore City Employment Data - Employment Rates by Parent Income
- [Baltimore City Employment Data All Parent Incomes](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/BaltimoreEmployment_All_PI.csv) 
- [Baltimore City Employment Data High Parent Incomes](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/BaltimoreEmployment_High_PI.csv) 
- [Baltimore City Employment Data Medium Parent Incomes](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/BaltimoreEmployment_Med_PI.csv) 
- [Baltimore City Employment Data Low Parent Incomes](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/BaltimoreEmployment_Low_PI.csv) 

#### Chicago Employment Data - Employment Rates by Parent Income
- [Chicago Employment Data All Parent Incomes](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/ChicagoEmployment_All_PI.csv) 
- [Chicago Employment Data High Parent Incomes](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/ChicagoEmployment_High_PI.csv) 
- [Chicago Employment Data Medium Parent Incomes](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/ChicagoEmployment_Med_PI.csv) 
- [Chicago Employment Data Low Parent Incomes](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/ChicagoEmployment_Low_PI.csv)

#### Opportunity Atlas - Source for CSV Tract Data in Baltimore and Chicago
- [Opportunity Atlas](https://www.opportunityatlas.org/) 

### Data Question
- How do employment rates compare in Baltimore and Chicago?
- How do employment rates compare in Baltimore and Chicago when segmented by Parent Income?
- How does each segment contribute to the average employment rate in either city?

### Data Answer
- Metric explored: Employment Rate = # Employed / # Labor Force

#### Plotly Express
![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.52.14%20PM.png) 

#### Pivot Tables
![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.53.39%20PM.png)

![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.54.44%20PM.png)

- The average employment rate in Baltimore is 71.48%. 
- The average employment rate in Chicago is 74.41%. 
- In Baltimore, employment for people with high-income parents is 78.00%, middle-income parents is 74.51%, and low-income parents is 69.06%.
- In Chicago, employment for people with high-income parents is 76.98%, middle-income parents is 76.40%, and low-income parents is 71.74%.
This shows the difference in employment rates for Baltimore and Chicago, segmented by parent income. Here, we see that Baltimore's employment rate for people with low-income parents is ~2% lower than Chicago's and could be driving a lower overall employment rate. 

#### Multiple Linear Regression
![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.56.15%20PM.png)

![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.57.21%20PM.png)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OydoEiz-Q99r4Tz1ehHyobecL2W-I3VW?usp=sharing)

## Business Answer

## Comparing Python and Excel

## Summary and Next Steps 
Parent income affects employment rates. Generally, average employment rate increases as parent income increases for both cities, though we cannot assert causation. Baltimore's employment rate for people with low-income parents is lower than Chicago's, which could be driving lower overall employment. 

The next steps are to look at why parent income influences employment rates. I'd like to explore data about the job market and education levels to see if those are impacted by parent income. Likewise, external factors like industries or types of jobs are important to consider for each city. 

This is important to me, because addressing employment rates, especially amongst those with low-income parents, is critical to social mobility and thriving cities.

