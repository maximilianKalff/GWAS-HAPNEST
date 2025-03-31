# HAPNEST GWAS – Ancestry-Specific Genome-Wide Association Study

This repository contains all relevant code, documentation, and results for our project in the course **Biomedical Data Types** at Hasso Plattner Institute. 

The project focuses on performing a genome-wide association study (GWAS) using the synthetic HAPNEST dataset. We analyze genetic associations separately for two ancestry groups – European (EUR) and African (AFR) – and combine the results through meta-analysis. The goal is to explore ancestry-specific patterns in genetic data and assess how population structure impacts GWAS outcomes.

---

## Repository Structure

```bash
HAPNEST_GWAS/
├── data/
│   ├── raw/                # Original input data (PLINK files per chromosome)
│   ├── processed/          # Filtered & QC'd data per ancestry group
│   ├── maps/               # rsID mapping files per chromosome
│   └── results/            # GWAS and meta analysis results and visualizations
│
├── notebooks/
│   ├── 01_preprocessing.ipynb          # Data filtering, phenotype assignment and quality control
│   ├── 02_gwas_analysis.ipynb          # GWAS per ancestry and meta-analysis
│   └── 03_results_visualization.ipynb  # Manhattan plots and summary visuals
│
├── requirements.txt                    # Python dependencies
├── run_gwas_caffeinate.sh              # Optional Bash script to run long jobs
└── README.md
```

## How to Run

1. Clone this repository and set up a python virtual environment.
2. Install dependencies: `pip install -r requirements.txt`
3. Download the HAPNEST dataset manually into data/raw/.
4. Run the preprocessing, QC and GWAS for both ancestries `AFR` and `EUR`.
5. Run the meta analysis.
6. Create plots & visualizations with `03_results_visualization.ipynb`.

## 🛠️ Tools Used

- PLINK v1.9 – for QC, GWAS, and meta-analysis (Slifer, 2018)
- Python 3.11 – data handling and preprocessing
- libraries listed in `requirements.txt`
- Jupyter Notebook – reproducible workflow and step-by-step analysis

## License & Credits

This project was developed as part of the course Biomedical Data Types at HPI.
Dataset credit: HAPNEST project (S-BSST936, EBI).
Code and content are for academic use only.

## Authors

- Maximilian Kalff
- Emil Kobel
