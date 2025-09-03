# Support Email Analysis

This notebook analyzes support emails to identify urgent tickets and generate a summary report.

## Files

- `mypro.csv`: Input CSV file containing support email data with columns: `sender`, `subject`, `body`, and `sent_date`.
- `outputs/urgent_tickets.csv`: Output CSV file containing only the urgent tickets identified.
- `outputs/processed_emails_report.csv`: Output CSV file containing the complete dataset with an added `is_urgent` column.

## Setup

1. Make sure you have the `mypro.csv` file in the same directory as the notebook or update the `INPUT_CSV` variable with the correct path.
2. Run all the cells in the notebook.

## Functionality

The notebook performs the following steps:

- **Load Data**: Reads email data into a pandas DataFrame.
- **Preprocess Data**: Converts `subject` and `body` columns to lowercase.
- **Detect Urgent Tickets**: Flags emails containing keywords like `urgent`, `critical`, or `immediate`.
- **Generate Summary**: Lists top 5 subjects, issues, senders, and total urgent tickets.
- **Save Outputs**: Exports urgent tickets and full dataset to the `outputs` folder.

## Output

- Top Subjects
- Top Issues (body content)
- Top Senders
- Number of Urgent Tickets

Generates:
- `urgent_tickets.csv` (urgent emails)
- `processed_emails_report.csv` (full dataset with urgency flag)

## Code Structure

- `load_data(csv_file)`: Loads CSV
- `preprocess_data(df)`: Makes text lowercase
- `detect_urgent(df, keywords)`: Flags urgent emails
- `generate_summary(df)`: Creates summary
- `save_outputs(df, urgent_tickets, output_dir)`: Saves results
- `main()`: Runs all steps

Analysis starts automatically when running the notebook.
