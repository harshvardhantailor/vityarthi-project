# import pandas as pd

import os
import matplotlib.pyplot as plt
from datetime import datetime
def load_expenses():
if os.path.exists('expenses.csv'):
return pd.read_csv('expenses.csv')
else:
return pd.DataFrame(columns=['Date', 'Category', 'Description', 'Amount'])
def save_expenses(df):
df.to_csv('expenses.csv', index=False)
def add_expense(df):
date_str = input("Date (YYYY-MM-DD): ").strip()
category = input("Category: ").strip()
description = input("Description: ").strip()
while True:
try:
amount = float(input("Amount: ").strip())
break
except ValueError:
print("Please enter a valid number for amount.")
new_expense = pd.DataFrame({
'Date': [date_str],
'Category': [category],
'Description': [description],
'Amount': [amount]
})
updated_df = pd.concat([df, new_expense], ignore_index=True)
save_expenses(updated_df)
print("Expense added successfully!")
def view_expenses():
df = load_expenses()
if df.empty:
print("No expenses recorded yet.")
else:
print(df.to_string(index=False))
def generate_report():
df = load_expenses()
if df.empty:
print("No expenses to report.")
return
df['Date'] = pd.to_datetime(df['Date'])
print("\n1. Total by Category")
print("2. Monthly Summary")
choice = input("Choose report type (1 or 2): ").strip()
if choice == '1':
category_totals = df.groupby('Category')['Amount'].sum()
print("\nTotal Expenses by Category:")
print(category_totals)
elif choice == '2':
df['Month'] = df['Date'].dt.to_period('M')
monthly_totals = df.groupby('Month')['Amount'].sum()
print("\nMonthly Expense Summary:")
print(monthly_totals)
else:
print("Invalid choice.")
def visualize_data():
df = load_expenses()
if df.empty:
print("No data to visualize.")
return
category_totals = df.groupby('Category')['Amount'].sum()
plt.figure(figsize=(8, 6))
plt.pie(category_totals, labels=category_totals.index, autopct='%1.1f%%', startangle=140)
plt.title('Expense Distribution by Category')
plt.axis('equal')
print("\nGenerating visual chart window...")
plt.show()
def statistical_analysis():
df = load_expenses()
if df.empty:
print("No data for analysis.")
return
print("\n--- Statistical Analysis ---")
total_spent = df['Amount'].sum()
average_spent = df['Amount'].mean()
max_expense = df.loc[df['Amount'].idxmax()]
min_expense = df.loc[df['Amount'].idxmin()]
print(f"Total Expenditure: \${total_spent:.2f}")
print(f"Average Transaction: \${average_spent:.2f}")
print(f"Highest Single Expense: \${max_expense['Amount']} ({max_expense['Category']} - {max_expense['Description']})")
print(f"Lowest Single Expense: \${min_expense['Amount']} ({min_expense['Category']})")
print("----------------------------")
def main():
while True:
print("\nPersonal Finance Tracker")
print("1. Add Expense")
print("2. View Expenses")
print("3. Generate Report")
\# New Menu Options
print("4. Visual Analytics (Charts)")
print("5. Statistical Analysis")
print("6. Exit")
choice = input("Choose an option: ").strip()
if choice == '1':
df = load_expenses()
add_expense(df)
elif choice == '2':
view_expenses()
elif choice == '3':
generate_report()
elif choice == '4':
visualize_data()
elif choice == '5':
statistical_analysis()
elif choice == '6':
print("Goodbye!")
break
else:
print("Invalid option. Try again.")
if __name__ == "__main__":
main()

make a readme file for this code and make it humanize as posiible highlight the heading

Here's a humanized README file for your personal finance tracker code with highlighted headings:

# Personal Finance Tracker

Welcome to your Personal Finance Tracker! This simple yet powerful tool helps you keep track of your daily expenses, view detailed reports, visualize your spending habits, and perform statistical analysis — all from the comfort of your command line.

## Features

- **Add Expense:** Easily record your expenses by entering the date, category, description, and amount.
- **View Expenses:** Look through all your recorded expenses in a clear, tabular format.
- **Generate Reports:** Get insightful summaries either by category or monthly totals.
- **Visual Analytics:** See your spending distribution in a colorful pie chart.
- **Statistical Analysis:** Understand your total spending, average transaction amounts, and identify your highest and lowest expenses.


## How to Use

1. Run the program in a Python environment with pandas and matplotlib installed.
2. Choose from the menu:
    - Add new expenses by providing details through prompts.
    - View all expenses at any time.
    - Generate reports to understand where your money goes.
    - Visualize your expenses with charts.
    - Get quick stats about your spending habits.
3. All data is saved automatically in an `expenses.csv` file in the current directory, so your information persists between sessions.

## Requirements

- Python 3
- pandas library
- matplotlib library

You can install the required libraries with this command:

```bash
pip install pandas matplotlib
```


## File Structure

- `expenses.csv`: The main data file where all your expense records are stored.
- Python script: The program handles loading, saving, and updating this file automatically.


## Notes

- When adding an expense, please enter the date in the format `YYYY-MM-DD`.
- The amount must be a valid number.
- Visual charts open in a new window for easy viewing.

Enjoy managing your personal finances with ease!

