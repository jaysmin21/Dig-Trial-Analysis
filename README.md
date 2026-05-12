# Dig-Trial-Analysis

Multivariable Cox proportional hazards analysis of Digoxin's effect on first hospitalization due to worsening heart failure (WHF) in the DIG trial, with subgroup interaction tests and a forest plot.

## Background

Extension of an MPH integrated learning experience (BU SPH, 2025) that performed a stratified subgroup analysis of the DIG trial using risk differences and a Breslow-Day test. This project re-analyzes the same question using a time-to-event framework (Cox PH) and compares findings to the original.

## Repo structure

```
Dig-Trial-Analysis/
├── README.md
├── decisions.md          # Running log of analytical decisions and rationale
├── writeup.md            # Methods, results, limitations
├── .gitignore
├── scripts/
│   ├── 01_data_prep.R
│   ├── 02_reproduce_ile.R
│   ├── 03_cox_models.R
│   ├── 04_diagnostics.R
│   └── 05_forest_plot.R
├── data/                 # Raw DIG data (gitignored; see Data section)
└── output/               # Forest plot, summary tables, logs
```

## Data

DIG trial data is publicly available through NHLBI BioLINCC (requires a brief data use agreement). Place the raw file at `data/dig.csv` before running scripts. Not committed to this repo.

## How to run

```r
# From repo root, in R:
source("scripts/01_data_prep.R")
source("scripts/02_reproduce_ile.R")
source("scripts/03_cox_models.R")
source("scripts/04_diagnostics.R")
source("scripts/05_forest_plot.R")
```

## Status

In progress. v1 target: 2 weeks.
