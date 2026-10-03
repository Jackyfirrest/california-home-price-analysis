# California Home Price Analysis

This project explores CRMLS home sales and prepares for a model that predicts the final sale price of a California single-family home.

## Start here

Open and run [`notebooks/01_exploration.ipynb`](notebooks/01_exploration.ipynb).

The notebook contains the full Week 0–2 work:

- project goal and scope
- key column definitions
- data-file validation
- required property filters
- missing-value and summary tables
- price and feature distributions
- correlations and scatter plots
- monthly sales and price patterns
- conclusions and next steps

All explanations are written in simple English, and the saved notebook already contains the executed results.

## Simple project structure

```text
.
├── README.md
├── requirements.txt
├── notebooks/
│   └── 01_exploration.ipynb
├── data/
│   ├── README.md
│   └── raw/California/
├── docs/
│   └── data_dictionary.pdf
└── archive/
```

`archive/` is kept only for traceability. It is not used by the notebook.

The original task brief stays local because it contains source-system credentials.

## Data scope

- Period: February 2025 through April 2026
- Required segment: `Residential` and `SingleFamilyResidence`
- Expected monthly files: 15
- Valid monthly files: 14
- July 2025 is an incomplete source CSV and is reported, then skipped
- Raw rows loaded: 298,326
- Filtered rows with a positive price: 149,200

## Run

From the project folder:

```powershell
python -m pip install -r requirements.txt
python -m jupyter notebook notebooks/01_exploration.ipynb
```

To execute and save every cell from the command line:

```powershell
python -m jupyter nbconvert --to notebook --execute notebooks/01_exploration.ipynb --inplace --ExecutePreprocessor.timeout=600
```

## Main findings

- Median close price: **$890,000**
- Living area has the strongest simple relationship with price: **Spearman 0.51**
- Lot size has the most missing values: **1.75%**
- The price distribution is strongly right-skewed and contains extreme values
- Week 3 should handle duplicates, missing values, and unusual values before a time-based train/test split
