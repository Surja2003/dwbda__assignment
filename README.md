# DWBDA Assignments

This repository contains three data-processing assignments in
`DWBDA_Assignments.ipynb`:

1. Market Basket Analysis with Apriori on the Bread Basket dataset.
2. MapReduce-style grade counting on the Students Performance dataset.
3. PySpark aggregation of products sold by category on the Sample Superstore dataset.

## Data

The CSV files are stored in `data/` so the notebook can run without a network
connection. They correspond to these Kaggle datasets:

- [Bread Basket](https://www.kaggle.com/datasets/mittalvasu/breadbasket)
- [Students Performance in Exams](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)
- [Sample Superstore](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

The downloaded copies used by the notebook are:

- `data/BreadBasket_DMS.csv`
- `data/StudentsPerformance.csv`
- `data/SampleSuperstore.csv`

## Setup

Use Python 3.10 or newer. From the repository root, create and activate a
virtual environment, then install the dependencies:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

If PowerShell blocks activation, run the notebook with the environment's
interpreter directly or use Command Prompt:

```bat
.venv\Scripts\activate.bat
```

## Run

Start Jupyter from the repository root:

```powershell
jupyter notebook
```

Open `DWBDA_Assignments.ipynb` and run the three Python cells from top to
bottom. The Spark assignment requires a working Java installation because
PySpark starts a local Spark process.

## Test

There is no separate test suite yet. The notebook itself is the executable
check. A successful run should show approximately 21,292 bakery rows after
excluding `NONE`, 1,000 student rows, and 9,994 superstore rows. It should also
print association rules, a grade-count table, and Spark totals grouped by
category.

To verify that all required CSVs are present before opening Jupyter:

```powershell
Get-ChildItem .\data\*.csv | Select-Object Name,Length
```

## Push to GitHub

The target repository is `https://github.com/Surja2003/dwbda__assignment.git`.
After configuring Git and authenticating to GitHub, run:

```powershell
git init
git add .
git commit -m "Add DWBDA assignments and datasets"
git branch -M main
git remote add origin https://github.com/Surja2003/dwbda__assignment.git
git push -u origin main
```

If `origin` already exists, update it instead:

```powershell
git remote set-url origin https://github.com/Surja2003/dwbda__assignment.git
git push -u origin main
```