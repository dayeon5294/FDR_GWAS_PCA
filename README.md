# FDR-GWAS-PCA

This repository contains selected data and code used in the paper:

**"FDR controlling procedures with dimension reduction and their application to GWAS with linkage disequilibrium score"**

## Overview

The study proposes two covariate-assisted procedures for false discovery rate (FDR) control in genome-wide association studies (GWAS), particularly in the presence of high-dimensional linkage disequilibrium (LD) score covariates. Dimension reduction is achieved via principal component analysis (PCA), and comparisons are made between classical FDR methods and covariate-based approaches (e.g., IHW, Boca-Leek).

## Contents

```
FDR-GWAS-PCA/
├── data/
│   ├── data_chro.zip                    # Compressed summary statistics for BMI (from GIANT)
│   └── [external] LD scores & MAF       # See links below for original sources
├── code/
│   ├── R/
│   │   ├── SNP_analysis.Rmd                      # Preprocessing of GWAS data
│   │   ├── Simulation with IHW method.Rmd        # Simulation data generation using IHW
│   │   └── Simulation with BL method.Rmd         # Simulation data generation using Boca-Leek
│   └── Python/
│       ├── Result of SNP analysis.ipynb                   # Real data GWAS analysis with PCA
│       ├── Result of simulation with IHW method.ipynb     # Visualization and summary of IHW simulation
│       └── Result of simulation with BL method.ipynb      # Visualization and summary of BL simulation
└── README.md
```

## How to Reproduce

To replicate the main findings:

1. Install R (≥ 4.1.0) and Python (≥ 3.8) with the necessary packages.
2. Extract the BMI summary statistics file from `/data/BMI_chr3_summary.zip`.
3. Download the following external datasets:
   - **LD scores** (baseline model):  
    [LD Score Regression Annotations – BaselineLD](https://alkesgroup.broadinstitute.org/LDSCORE/)  
    → Download: `1000G_Phase3_baselineLD_ldscores.tgz`  
    - Use `.annot` files to determine SNP membership in functional groups (binary annotation: 0/1).  
    - Use `.l2.ldscore` files for the LD scores of each SNP.  
    - The column **base** includes all SNPs (all 1s).
  
  - **Minor Allele Frequency (MAF)**:  
    [1000 Genomes Phase 3 Data](https://alkesgroup.broadinstitute.org/LDSCORE/)  
    → Download: `1000G_Phase3_frq.tgz`  
    - Contains files for chromosomes 1–22 with MAF per SNP.

> Note: Due to file size constraints, only the BMI summary statistics used in our real-data analysis are included directly in this repository. LD score and MAF data used in the study can be obtained from the original sources linked above.

## Citation

If you use this code or dataset, please cite:

> Jung D, Kim Y, Park J. FDR controlling procedures with dimension reduction and their application to GWAS with linkage disequilibrium score. *PLOS ONE*. [Forthcoming].

## License

This project is licensed under the MIT License (see `LICENSE` file for details).
