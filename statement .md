

**STATEMENT FILE

(Personal Finance Tracker – Python Program)**

## **1. Title of the Program**

Personal Finance Tracker with Reporting, Visualization, and Statistical Analysis


---

##  **2. Objective of the Program**

The objective of this program is to design a simple and efficient personal expense management system that allows users to:

Add and store daily expenses

View all recorded expenses

Generate meaningful financial reports

Visualize spending patterns using charts

Perform statistical analysis on expenditure data


The system uses a CSV file (expenses.csv) to store data permanently.


---

##  **3. Problem Statement**

Managing personal expenses manually is inefficient and error-prone. People often struggle to keep track of their daily spending and analyze where their money goes.
This program provides a menu-driven Python application to help users record expenses, monitor financial activity, and obtain insights through reports and visualizations.


---

##  **4. Proposed System**

The program performs the following operations:

###   a) Add Expense

Accepts Date, Category, Description, and Amount.

Validates numeric entries.

Appends the new data to expenses.csv.


###  b) View Expenses

Displays all stored expenses in tabular form.


###  c) Generate Reports

##  **Two types of reports:**

1. Category-wise Total Expense


2. Monthly Expense Summary



###  d) Visual Analytics

Generates a pie chart to show spending distribution by category.


###  e) Statistical Analysis

Displays:

Total Expenditure

Average Transaction Value

Highest Single Expense

Lowest Single Expense



---

##  **5. Software and Libraries Used**

Python 3

Pandas – Data handling and CSV operations

Matplotlib – Chart visualization

OS module – File handling

Datetime module – Date processing



---

##  **6. Methodology / Working of the Program**

###  1. Loading Data:

Program checks for expenses.csv.

If unavailable, an empty DataFrame is created.



###   2. Menu-Driven Interface:
The main() function displays a menu with multiple choices.


###  3. Adding New Expense:

User inputs are collected.

Data is validated and appended.

Saved to CSV.



###   4. Viewing Expenses:

Complete DataFrame displayed in clean format.



###  5. Reports & Analysis:

Data is grouped (by Category / by Month).

Summaries printed.



###  6. Visualization:

Pie chart displaying percentage-wise expense distribution.



### 7. Statistics:

Calculation using pandas functions (sum, mean, max, min).





---

##  **7. Advantages of the System**

Easy to use

Permanently stores expenses

Helpful analytics and insights

Good visualization

Portable and extendable



---

##  **8. Conclusion**

The Personal Finance Tracker is a compact yet powerful Python application that helps users maintain and analyze their financial records efficiently. With clear visual analytics, detailed reports, and statistical insights, it enhances money-management skills and promotes better financial awareness.


