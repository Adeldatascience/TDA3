# TDA3 — Topological Data Analysis of U.S. Colleges

This project applies **Topological Data Analysis (TDA)** to U.S. College Scorecard data
to study the evolving geometric structure of higher-education institutions over time.

## Data Source
The data come from the **U.S. Department of Education College Scorecard** MERGED files.

Due to size constraints, **raw MERGED files are not included** in this repository.
They can be downloaded from:
https://collegescorecard.ed.gov/data/

Missing values in the selected variables are encoded using **machine epsilon**
rather than dropping observations.

## Variables Used
All point clouds are constructed in **ℝ³** using only:
- `COSTT4_A` — Cost of attendance
- `MD_EARN_WNE_P10` — Median earnings (10 years after entry)
- `DEBT_MDN` — Median student debt

## Methodology
- Each academic year is treated as a point cloud of colleges in ℝ³
- Alpha complexes are constructed using **Gudhi**
- Persistent homology (H₀, H₁) is computed year-by-year
- Temporal changes in topological structure are visualized

## Repository Structure
TDA3/
├── data/
│ └── processed/ # derived data products
├── notebooks/ # analysis notebooks
├── figures/ # plots and visualizations
├── .gitignore
└── README.md

## Notes
This repository contains **code and results only**.
Raw data must be downloaded separately to reproduce the analysis.


