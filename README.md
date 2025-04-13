# FDR-GWAS-PCA

This repository contains selected data and code used in the paper:

**"FDR controlling procedures with dimension reduction and their application to GWAS with linkage disequilibrium score"**

## Overview

The study proposes two covariate-assisted procedures for false discovery rate (FDR) control in genome-wide association studies (GWAS), particularly in the presence of high-dimensional linkage disequilibrium (LD) score covariates. Dimension reduction is achieved via principal component analysis (PCA), and comparisons are made between classical FDR methods and covariate-based approaches (e.g., IHW, Boca-Leek).

## Contents

```
FDR-GWAS-PCA/
├── data/
│   ├── BMI_chr3_summary.txt              # Example summary statistics (GIANT BMI, chromosome 3)
│   └── simulated_covariates.csv         # Simulated covariate matrix for Scenario 1
├── code/
│   ├── simulation_scenario1.R           # R script for null proportion estimation scenario
│   ├── simulation_scenario2.R           # R script for size-investing scenario
│   └── realdata_analysis_PCA.ipynb      # Jupyter notebook for PCA-based analysis on real data
├── results/
│   └── figs/                            # Selected plots (e.g., TPR/FDR comparisons)
└── README.md
```

## How to Reproduce

To replicate the main findings:

1. Install R (≥ 4.1.0) and Python (≥ 3.8) with the necessary packages.
2. Run the simulation scripts in `/code/`.
3. Use the notebook `realdata_analysis_PCA.ipynb` for real GWAS data analysis.

## Citation

If you use this code or dataset, please cite:

> Jung D, Kim Y, Park J. FDR controlling procedures with dimension reduction and their application to GWAS with linkage disequilibrium score. *PLOS ONE*. [Forthcoming].

## License

This project is licensed under the MIT License (see `LICENSE` file for details).
