# Assurance Maladie Reimbursement Analysis

## Data
- **Source:** [Open Damir : base complète sur les dépenses d'assurance maladie - 2009 à 2025](https://www.assurance-maladie.ameli.fr/etudes-et-donnees/open-damir-depenses-sante-interregimes)
- **Codebook:** [Descriptif des variables Open DAMIR](https://www.assurance-maladie.ameli.fr/sites/default/files/2024_descriptif-variables_open-damir-base-complete.xlsx)
- **Coverage:** All reimbursement regimes, France entière
- **Volume:** 106M rows x 57 columns (January, June, December 2025)

## Tools
- DuckDB: SQL queries on raw CSV files without importing full files into memory
- pandas, matplotlib, seaborn

## Analysis
1. Overall reimbursement volume per month
2. Distribution across care settings (CPT_ENV_TYP)
3. Soins de ville expenditure by act type (PRS_NAT): top 50 codes, 12 categories, 89.8% coverage
4. Reimbursement by age group (AGE_BEN_SNDS)

## Key findings
- Soins de ville accounts for 69% of total AM spending (29.3B€ across 3 months)
- Pharmacy is the largest expenditure category within soins de ville (7.92B€)
- Indemnités journalières represent 4.58B€, second largest category after pharmacy
- Reimbursement peaks at age 60-69 (7.88B€) before declining for 80+
- December shows consistently higher expenditure across all care settings
- Code 9 (1.8B€ unclassified) is driven by hospital stay charges from smaller regimes (MSA, SLM)
