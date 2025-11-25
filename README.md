***

# Personal Finance Tracker

This is a simple command-line Personal Finance Tracker application written in Python. It allows you to add, view, analyze, and visualize your personal expenses stored in a CSV file.

## Features

- Add expense entries with date, category, description, and amount.
- View all recorded expenses in a tabular format.
- Generate reports by category or monthly summaries.
- Visualize expense distribution by category with pie charts.
- Perform statistical analysis including total, average, highest, and lowest expenses.

## Installation

Make sure you have Python installed (version 3.x recommended). Also install the required Python packages:

```bash
pip install pandas matplotlib
```

## Usage

Run the program using:

```bash
python your_script_name.py
```

You will see a menu with the following options:

1. Add Expense: Enter the date, category, description, and amount for a new expense.
2. View Expenses: Display all recorded expenses.
3. Generate Report: Choose between total expenses by category or monthly summary.
4. Visual Analytics (Charts): View a pie chart showing expense distribution by category.
5. Statistical Analysis: Display total spending, average transaction, highest and lowest expenses.
6. Exit: Close the application.

Follow the on-screen prompts to interact with your data.

## Data Storage

All expenses are saved in a CSV file named `expenses.csv` in the same directory as the program. The file contains the columns:

- Date (YYYY-MM-DD)
- Category
- Description
- Amount

## Dependencies

- pandas: For data handling and analysis.
- matplotlib: For visualization (pie charts).

## Notes

- Input validation ensures amounts entered are numeric.
- Date input must be in YYYY-MM-DD format.
- Visualizations require a display environment to show the plot window.
- Adding and viewing data refreshes the CSV file to keep data persistent.

## License

This project is provided for personal use and learning purposes.
