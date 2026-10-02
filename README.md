# ObservationSorter

ObservationSorter is a Python console application for analyzing observation data from CSV files. It helps summarize operational trends by counting observations by operator, identifying common cause codes, and highlighting each operator’s most frequent defect category.

## Features

- Load observation data from a CSV file
- View the imported dataset
- Count total observations by operator
- Find the most common cause codes
- Filter cause-code results by date
- Identify each operator’s most common defect category
- Export results to CSV files

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
source .venv/bin/activate   # macOS/Linux
# or
.venv\Scripts\activate     # Windows
pip install pandas
```

## Usage

```bash
python main.py
```

The application presents a menu with options to:
1. Open an observation file
2. View the dataset
3. Count observations by operator
4. Review common cause codes
5. Review the most common defect by operator
6. Exit

## Expected CSV Format

The script expects CSV data including fields such as:

```csv
date,operator,category,proc_ind
06/01/2024,ALICE,Machine Setup,False
06/01/2024,BOB,Housekeeping,True
06/02/2024,ALICE,Lockout/Tagout,False
```

## Output

Generated reports can be saved to the `output/` directory as CSV files, such as:
- `operator_statistics.csv`
- `cause_code_statistics.csv`
- `most_common_operator_defects.csv`

## License

This project is provided as-is for internal or personal use.
