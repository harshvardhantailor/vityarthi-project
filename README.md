

Title: Personal Finance Tracker using Python and CSV Storage
Course: (You can fill your course/subject name)
Submitted by: (Your Name – College/University)


---

⿡ Introduction

Managing daily expenses is important to maintain financial stability. Many students struggle to track where their money goes. This project solves that problem by developing a Personal Finance Tracker using Python.
It stores transaction data (date, category, description, amount) in a CSV file, which makes it lightweight, portable, and easy to update.


---

⿢ Objectives

✔ Record daily expenses conveniently
✔ Display previously recorded transactions
✔ Provide categorical and monthly expense reports
✔ Maintain data in a structured CSV format
✔ Improve financial awareness for users


---

⿣ Features

Feature	Description

Add Expense	User can enter amount, category, description & date
View Expenses	Displays complete expense history
Generate Reports	Shows spending by category or month
CSV Data Storage	Ensures persistent and organized financial data
Error Handling	Validates date and amount format



---

⿤ Software & Libraries Used

Software / Library	Purpose

Python	Backend program logic
pandas	Data management and reporting
os	File handling
datetime	Date validation



---

⿥ Code Description (Summary)

load_expenses(): Reads data from CSV file

save_expenses(df): Saves DataFrame back to CSV

add_expense(): Takes user input and appends new record

view_expenses(): Displays stored expenses

generate_report(): Shows reports (category-wise/monthly)

main(): Runs the entire menu-driven program



---

⿦ Workflow Diagram (Flowchart Style)

        ┌────────────┐
        | Start      |
        └────┬───────┘
             ↓
   ┌─────────────────────┐
   | Display Main Menu   |
   └─────┬───────────────┘
         ↓
  ┌──────────────────────┐
  | User Selects Option? |
  └─────────┬────────────┘
            ↓
 ┌────────────┬────────────┬───────────┬────────────┐
 | Add Exp.   | View Exp.  | Report    | Exit       |
 └──────┬─────┴───────┬────┴───────┬──┘
        ↓             ↓            ↓
   Update CSV   Display Table   Show Summary
        ↓             ↓            ↓
        └─────────Back to Menu────┘


---

⿧ Output Screens (Console)

Menu-based interface

Displays expenses in a neat table

Provides summary reports



---

⿨ Applications

📌 Useful for students, households, freelancers
📌 Can be extended into a GUI or mobile app
📌 Helps manage financial health clearly


---

⿩ Conclusion

This project successfully provides a simple and effective financial tracking system.
It gives users better awareness of spending patterns and supports smart financial decisions.
Future improvements could include charts, user authentication, and database storage.


---

📎 README.md (Project Documentation)

# Personal Finance Tracker (Python + CSV)

A simple command-line based Personal Finance Tracker that helps you record expenses, 
view your spending history and generate reports using CSV storage.

## 📌 Features
- Add daily expenses with date, category, description & amount
- Display all recorded expenses
- Category-wise and Monthly expense reports
- Persistent data stored in a CSV file
- Error handling for correct date and amount format

## 🛠 Requirements
Install the necessary Python libraries before running:
```bash
pip install pandas

▶ How to Run

Just execute the main Python script:

python main.py

📂 File Structure

project-folder/
│
├─ main.py            # Main source code
├─ expenses.csv       # Auto-created database file
└─ README.md          # Documentation

🧮 Functional Overview

add_expense() → Add new transaction

view_expenses() → Display stored data in table format

generate_report() → Summarize expenses by category / month

load_expenses() / save_expenses() → Manage CSV storage


🚀 Future Enhancements

Graphical User Interface (GUI - Tkinter/PyQt)

Login system for multiple users

Data visualization charts

Export reports in PDF/Excel


👨‍💻 Author

HARSHVARDHAN TAILOR 
VIT
