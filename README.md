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

## Run in Google Colab

Open the notebook in Google Colab from the GitHub repository:

1. Visit `https://colab.research.google.com/`.
2. Select **GitHub** in the notebook picker.
3. Enter `https://github.com/Surja2003/dwbda__assignment`.
4. Open `DWBDA_Assignments.ipynb` and run the cells yourself.

In Colab, clone the repository and change into its folder before running the
assignment cells so the CSV paths resolve:

```python
!git clone https://github.com/Surja2003/dwbda__assignment.git
%cd dwbda__assignment
%pip install -r requirements.txt
```

The notebook is intentionally committed without saved execution results. Run
the cells in Colab to generate the results interactively.

## Run locally (optional)

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

There is no separate test suite. Open the notebook in Colab and run the three
Python cells to perform the checks. The CSV files are already included in the
repository, so no Kaggle account or API key is required.

To verify that all required CSVs are present locally:

