

## Power BI Finance Dashboard
## Overview
The Power BI Finance Dashboard provides a comprehensive view of financial data, allowing users to analyze income, savings, and expenses on a yearly basis. It is designed to help users understand their financial health by visualizing key metrics and their proportions.

## Problem Statement
In financial management, understanding the distribution of income, expenses, and savings over time is crucial. This dashboard aims to solve the following problems:

**1. Total Income Calculation:** Easily view and analyze the total income received per year.

**2. Expense Tracking:** Track and visualize expenses as a percentage of total income.

**3.Savings Analysis:** Determine savings and their percentage relative to income.

**4.Dynamic Title and Insights:** Provide dynamic titles and other relevant metrics to enhance user understanding and navigation.

## Dataset
The dashboard utilizes a dataset with the following columns:

**Type:** The type of financial entry (Income, Expense, Savings, etc.).

**Component:** The specific component or category within each type (e.g., Salary, Utilities, Investments).

**Date:** The date of the financial entry.

**Value:** The monetary value associated with the entry.



## Example Data

![App Screenshot](https://github.com/souhacks/Finance_Dashboard/blob/main/Capture002.PNG?raw=t)

## Features
**Total Income:** Displays the total income for each year.

**Total Expenses:** Shows total expenses and their percentage relative to income.

**Total Savings:** Provides total savings and their percentage relative to income.

**Dynamic Titles:** Utilizes DAX to create dynamic titles based on user selections and timeframes.

**Percentage Calculations:** Calculates and displays percentages for expenses, savings, and other components relative to total income.

## Dashboard

![App Screenshot](https://github.com/souhacks/Finance_Dashboard/blob/main/Capture001.PNG?raw=t)

## Usage
**Open the Power BI File:** Open the .pbix file in Power BI Desktop.

**Interact with Visuals:** Use slicers and filters to view data for different years or categories.

**Review Metrics:** Analyze the total income, expenses, savings, and their respective percentages through the provided visuals.

## DAX Formulas
Here are some of the key DAX formulas used in the dashboard:

**Total value**

Total_Value = SUM('Finance_Data'[Value])

**Expense % :** 

Expense % = DIVIDE([Expenses],[Income])

**Salary % :** 

Saving % = DIVIDE([Savings],[Income])

**Line Chart Measures**

Line_chart_Measures = var Selected_val = SELECTEDVALUE(Line_Selection_Table[No.])
RETURN SWITCH(Selected_val, 1, [Expense %], 2, [Income Change MoM %], 3, [Saving %], 4, [Target])

**Savings**

Savings = CALCULATE([Total_Value],'Finance_Data'[Type]="Savings")

and so on

## Contributing
Feel free to fork the repository, make changes, and submit pull requests. Contributions to improve the dashboard and its features are always welcome!