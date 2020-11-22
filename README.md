# comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON
This repository contains data analysis comparing Baltimore City's and Chicago's employment rates based on parent income. Analysis was conducted using Python. 

## Background
For this project, I chose to analyze employment rates in Baltimore City, MD and Chicago, IL (hometown), segmented by parent income. 
The explored metric is employment rate (%) based on parent income (high, medium, and low). This is interesting because some studies cite a [positive relationship between parent income and a child's employment/wealth outcomes](https://www.irp.wisc.edu/publications/focus/pdfs/foc272e.pdf). 
Comparing Baltimore and Chicago's employment maps, we can see that the two cities are visually similar, with large clusters of low employment areas and small clusters of high employment near the city centers. 

![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%206.14.01%20PM.png) 

![alt text]( https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%206.13.21%20PM.png)

With our discussions regarding social mobility, it's important to understand if parent income is a driver of employment in these cities, how they differ, and what can be done to increase employment. 

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
This graph shows the difference in employment rate between Baltimore and Chicago factoring in all parent income groups. 
- The average employment in Baltimore is 72.0%
- The average employment in Chicago is 74.5%
Chicago's employment is 2.5% higher than Baltimore, which is significant given the population differences. 
![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.52.14%20PM.png) 

#### Pivot Tables
![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.53.39%20PM.png)

![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.54.44%20PM.png)

- In Baltimore, employment for people with high-income parents is 78.9%, middle-income parents is 75.0%, and low-income parents is 69.7%.
- In Chicago, employment for people with high-income parents is 80.2%, middle-income parents is 76.8%, and low-income parents is 72.1%.

Chicago exhibits higher employment rates for each income group. The most notable differences are 1) The 2.4% higher employment for the low-income parent group 2) The smaller employment delta between those with high-income parents and low-income parents. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OydoEiz-Q99r4Tz1ehHyobecL2W-I3VW?usp=sharing)

#### Multiple Linear Regression
* Note that I did not determine the statistical significance of the coefficients. 

The goal was to determine whether or not one's parent-income group (high, medium, or low) would be a predictor of average employment for all parent-income groups. 
- Assuming all variables are significant: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OydoEiz-Q99r4Tz1ehHyobecL2W-I3VW?usp=sharing)
  - Chicago's intercept is more than double that of Baltimore's
  - Middle-income parents have relatively the same impact on employment in both cities
  - Being in the high or low-income parent group has double the impact on employment in Chicago than in Baltimore
  
Baltimore Linear Regression
![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.56.15%20PM.png)

Chicago Linear Regression
![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.57.21%20PM.png)

## Comparing Python and Excel
There were three main differences between my experiences with Excel and Python:
- Data Prep: When data cleaning and aggregating, Colab required the importing of certain modules. In contrast, Excel has most of the functionality already built in. I personally found it easier to clean and aggregate data in Excel. This is because the dataset is always viewable in Excel, which makes it easier for me to appy filters, standardize columns, and merge worksheets. However, I see myself using Python for larger datasets for which Excel slows down. 
- Data Analysis: Python in Colab required downloading modules like pandas and numpy. Similar to Excel, which required downloading Data Analysis Tool Paks like Solver. Personally, I found it easier to create pivot tables, charts, and linear regressions in Excel. Likewise, I found the customizability of Excel's visuals to be more intuitive, especially with Pivot Charts. While I see myself using Excel for future analyses, Python can be valuable for larger datasets.
- Organization: When organizing my data analysis, I was pleased by how structured Colab is. The ability to create headers, leave comments, and create text cells makes it easier to follow the my analysis. Likewise, it was useful knowing where an error was in my code. In collaborative environments, I can see myself preferring to use Python because it is easier for others to follow the work or pinpoint errors. 

## Summary and Next Steps 
Parent income affects employment rates in both Baltimore and Chicago. Generally, average employment rate increases as parent income increases for both cities, though we cannot assert causation. Chicago's employment rate is higher than Baltimore's for each parent-income group. Baltimore's employment rate for people with low-income parents is >2% lower than Chicago's, which could be driving lower overall employment. This means that Chicago residents with high-income parents and low-income parents are more likely to be employed than their comaprable groups in Baltimore. Thus, it'd be interesting to explore why it's easier for both of these groups to be employed in Chicago. 

The next steps are to look at why parent income influences employment rates. 
- Person-specific factors: education, demographics, incarceration 
- City-specific factors: prevalent industries, available jobs, economic growth, policies

This is important to me, because addressing employment rates, especially amongst those with low-income parents, is critical to social mobility and thriving cities. Balitmore is a city where there is a strong [disconnect between one's skills and job opportunities](https://www.baltimoresun.com/opinion/op-ed/bs-ed-op-0115-baltimore-unemployment-20200115-urcqmi467vcqnlw4usgtonzwja-story.html). If we can determine what the root cause for the employment difference is, Baltimore can solve its lower employment issue. 

