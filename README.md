***README FILE FOR PROJECT***
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

