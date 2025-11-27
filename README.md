# MOFA Analysis of Pancreatic Cancer Cells from CCLE Database

This repository contains a Multi-Omic Factor Analysis (MOFA) of pancreatic cancer cell lines from the Cancer Cell Line Encyclopedia (CCLE) database, integrating transcriptomic and proteomic data.

## Overview

Multi-Omic Factor Analysis (MOFA) is a statistical framework for integrating multi-omics data sets in an unsupervised fashion. This analysis applies MOFA to pancreatic cancer cell lines to identify major sources of variation across RNA expression and protein abundance data.

## Repository Structure

```
.
├── code/
│   ├── Multiomic_analysis.ipynb      # Main MOFA analysis notebook
│   └── Downstream_MOFA.ipynb         # Downstream analysis of MOFA results
├── Data_set_for_training/
│   ├── pancreas_CCLE_protein_profile.csv  # Protein abundance data
│   └── pancreas_CCLE_RNA_profile.csv      # RNA expression data
├── source_data/
│   ├── Expression_Public_25Q2_subsetted.csv
│   ├── Metada_DepMap Public 25Q2.csv
│   └── Harmonized_MS_CCLE_Gygi_subsetted.csv
└── Model_and_results/
    ├── CLLE_no_groups.hdf5                # Trained MOFA model
    ├── RNA_5_main_variance_drivers.png
    ├── RNA_10_main_variance_drivers.png
    ├── Protein_5_main_variance_drivers.png
    └── Protein_10_main_variance_drivers.png
```

## Features

The main analysis script (`Multiomic_analysis.ipynb`) allows you to:
- Run MOFA on the entire pancreatic cancer cell line dataset
- Perform analysis on clusters formed by the expression level of a specific gene
- Integrate transcriptomic and proteomic data to identify key variance drivers

## Data Sources

- **CCLE (Cancer Cell Line Encyclopedia)**: Provides comprehensive characterization of cancer cell lines
- **DepMap Public 25Q2**: Metadata and expression data
- **Harmonized MS CCLE (Gygi Lab)**: Mass spectrometry-based proteomic data

## Requirements

To run the analysis, you'll need:
- Python 3.x
- Jupyter Notebook
- MOFA+ (Multi-Omics Factor Analysis)
- Standard data science libraries (pandas, numpy, matplotlib, etc.)

## Usage

1. Open `code/Multiomic_analysis.ipynb` in Jupyter Notebook
2. Follow the notebook instructions to run the analysis
3. Explore downstream results using `code/Downstream_MOFA.ipynb`

## About MOFA

MOFA is a free tool developed for multi-omic integration. For more information:
- [MOFA+ GitHub Repository](https://github.com/bioFAM/MOFA2)
- [MOFA+ Publication](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-020-02015-1)

## License

This analysis is provided as-is for research and educational purposes.

## Citation

If you use this analysis, please cite the original MOFA publication and the CCLE database:
- Argelaguet, R., et al. (2020). MOFA+: a statistical framework for comprehensive integration of multi-modal single-cell data. Genome Biology, 21(1), 111.
- Ghandi, M., et al. (2019). Next-generation characterization of the Cancer Cell Line Encyclopedia. Nature, 569(7757), 503-508.
