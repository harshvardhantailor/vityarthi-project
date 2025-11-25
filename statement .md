

##  **Project Title**  
Personal Finance Tracker (Command-Line Application)  

##  **Objective**  
The objective of this project is to provide a simple command-line based personal finance tracker that allows a user to record daily expenses, view all stored transactions, and generate basic analytic reports to understand spending patterns.  

##  **Problem Statement**  
Many individuals struggle to keep track of their day-to-day expenses, leading to poor visibility into where their money goes and difficulty in budgeting. Manual methods such as notebooks or ad‑hoc spreadsheets are error‑prone, hard to maintain, and not user‑friendly. There is a need for a lightweight, easy‑to‑use tool that enables users to log expenses quickly and review their spending without complex setup.  

##  **Scope of the Project**  
The application runs in a terminal/command‑line environment.  

It supports four main operations:  
- Add a new expense (with date, category, description, and amount).  
- View all recorded expenses.  
- Generate summary reports (by category or by month).  
- Exit the application.  

Data is stored in a CSV file (`expenses.csv`), allowing persistence across program runs and easy external viewing in spreadsheet software.  

The project focuses on individual users and simple expense tracking, not on full accounting or multi‑user features.  

##  **Technologies Used**  
- Programming Language: Python  
- Libraries/Modules:  
  - `pandas` for tabular data handling and analysis.  
  - `os` for checking the existence of the data file.  
  - `datetime` for date handling, with conversion to datetime objects during reporting.  
- Storage Format: CSV file (`expenses.csv`).  

##  **System Overview**  

#  *Data Loading (`load_expenses`)*  
- Checks if `expenses.csv` exists.  
- If it exists, loads the file into a pandas DataFrame.  
- If it does not exist, creates an empty DataFrame with columns: Date, Category, Description, and Amount.  

#  *Data Saving (`save_expenses`)*  
- Takes a DataFrame as input and writes it to `expenses.csv` without the index column, ensuring persistent storage.  

# *Adding a New Expense (`add_expense`)*  
- Prompts the user to enter:  
  - Date (YYYY-MM-DD format).  
  - Category (e.g., Food, Travel, Bills).  
  - Description (short text).  
  - Amount (validated to be numeric).  
- Builds a one‑row DataFrame for the new expense and appends it.  
- Saves updated data back to the CSV.  
- Confirms success with a message.  

#  *Viewing All Expenses (`view_expenses`)*  
- Loads current data.  
- Displays a message if empty; else prints the full DataFrame clearly without indices.  

#  *Generating Reports (`generate_report`)*  
- Converts Date to datetime.  
- Offers two report options:  
  - Total by Category (sum by category).  
  - Monthly Summary (sum by month).  
- Displays report in console.  

#  *Main Menu Loop (`main`)*  
- Text-based menu with four choices: Add Expense, View Expenses, Generate Report, Exit.  
- Loops until exit.  
- Routes user selections to functions, validates input.  

##  **Features**  
- Persistent CSV storage.  
- Input validation for amounts.  
- Structured view of all transactions.  
- Basic analytics by category and month.  
- User-friendly, menu-driven interface.  

##  **Limitations and Possible Improvements**  
- Relies on correct date format input (no strict validation).  
- No editing or deleting existing entries.  
- No advanced filters or graphical visualization.  
- Improvements could include:  
  - Date validation and auto date defaults.  
  - Edit/delete capabilities.  
  - More detailed reporting.  

  - Database storage and GUI/web interface.  
