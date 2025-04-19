# Simple Finance Dashboard

A Streamlit application for visualizing and categorizing personal finance transactions from a CSV file.

## Features

*   Upload transaction data via CSV.
*   Automatically categorizes transactions based on keywords associated with categories.
*   Manually categorize transactions using a data editor.
*   Adds transaction details as keywords to the selected category automatically when changes are applied.
*   Create new spending categories.
*   View total expenses per category in a table and a pie chart.
*   View a summary of income/payments.
*   Persists categories and associated keywords in a `categories.json` file.

## Requirements

*   Python 3.x
*   Streamlit
*   Pandas
*   Plotly Express

## Installation

1.  Clone the repository:
    ```bash
    git clone <your-repository-url>
    cd AutomateFinancesWithPython
    ```
2.  Install the required packages:
    ```bash
    pip install streamlit pandas plotly-express
    ```

## How to Run

1.  Navigate to the project directory in your terminal.
2.  Run the Streamlit app:
    ```bash
    streamlit run main.py
    ```
3.  Open your web browser and go to the local URL provided by Streamlit (usually `http://localhost:8501`).
4.  Upload your transaction CSV file.

## CSV File Format

The application expects a CSV file with at least the following columns:

*   `Date`: Transaction date (e.g., "01 Jan 2023").
*   `Details`: Description of the transaction.
*   `Amount`: Transaction amount (can include commas).
*   `Debit/Credit`: Indicates if the transaction is a 'Debit' or 'Credit'.

Make sure the column names match exactly (case-insensitive, leading/trailing spaces are handled).

## Categorization

*   Transactions are initially categorized based on keywords defined in `categories.json`.
*   You can manually change the category of any debit transaction in the "Expenses (Debits)" tab using the data editor.
*   When you apply changes after editing categories, the 'Details' of the re-categorized transaction will be automatically added as a keyword to the *new* category for future automatic categorization.
*   New categories can be added via the input box in the "Expenses (Debits)" tab.