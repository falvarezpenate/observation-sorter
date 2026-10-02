# ObservationSorter

ObservationSorter is a Python console application for analyzing observation data stored in CSV files. It lets you load a dataset, inspect it, summarize operational trends, and export useful reports such as total observations by operator and the most common defect categories.

## Features

- Open an observation CSV file from the command line
- Preview the imported dataset
- Count total observations by operator
- Find the most common cause codes
- Filter cause-code results by date
- Identify each operator's most common defect category
- Save report output as CSV files

## Project Structure

```text
observation-sorter/
├── main.py
├── README.md
├── output/
├── src/
│   ├── menu.py
│   └── observationSorter.py
└── .gitignore
```

## Requirements

- Python 3.9+
- pandas

## Installation

```bash
git clone https://github.com/falvarezpenate/observation-sorter.git
cd observation-sorter
python -m venv .venv
source .venv/bin/activate      # On macOS/Linux
# or
.venv\Scripts\activate         # On Windows
pip install pandas
```

## Running the Application

```bash
python main.py
```

This launches a menu-driven console app with the following options:

1. Open Observation File
2. View Data
3. Count Total Observations by Operator
4. Find Most Common Cause Code
5. Find Most Common Cause Code by Operator
6. Exit

## Expected CSV Format

The application expects a CSV file containing at least the columns used in the analysis, such as:

```csv
date,operator,category,proc_ind
06/01/2024,ALICE,Machine Setup,False
06/01/2024,BOB,Housekeeping,True
06/02/2024,ALICE,Lockout/Tagout,False
06/02/2024,CHARLIE,Unsafe Act,False
```

Notes:
- `date` is used for filtering by date in the format `mm/dd/yyyy`
- `operator` is used for grouping by employee/operator
- `category` holds the cause-code or defect category
- `proc_ind` indicates whether the observation is a procedural item (`True`/`False`)

## Example Workflow

1. Run `python main.py`
2. Choose option `1` to open your CSV file
3. View the dataset or generate reports
4. Save the generated results as CSV files when prompted

## Output Files

When you choose to save a report, the app writes CSV files to the `output/` directory using names such as:

- `operator_statistics.csv`
- `cause_code_statistics.csv`
- `most_common_operator_defects.csv`

## Notes

This project is designed as a simple data-analysis utility for observation records and is intended to be easy to extend. If you want to add features such as drag-and-drop CSV support, more advanced filtering, or a GUI, this codebase is a good starting point.
