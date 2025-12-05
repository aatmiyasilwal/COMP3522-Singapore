Here is the entire README in a single code block, exactly as GitHub will accept it:

This directory contains the full workflow for analysing HDB resale prices and evaluating whether different towns are “worth the money” after adjusting for structural, accessibility, and amenity features. The methodology also incorporates age-cohort preferences (20–29 vs 40–49).

---

## Folder Structure

- `hdb/`
  - `pm2/`
    - `PM2.ipynb` — Progress Meeting 2 analysis notebook  
    - `plots/` — Figures used in PM2  
  - `pm3/`
    - `age_cohort_value_scores.ipynb` — Age-based preference weighting and scoring  
    - `analysis.ipynb` — Main PM3 analysis pipeline
    - `training.ipynb` — Model training and feature setup  
    - `worth_it_by_town.ipynb` — Town-level worth-the-money evaluatio
    - `Data/`n  
  - `README.md`

---

## Summary of Work

- Conducted EDA on HDB resale transactions to identify structural, spatial, and temporal patterns.  
- Built accessibility and amenity features for fair price comparison across towns.  
- Trained models in `training.ipynb` to estimate fair values and extract important drivers.  
- Evaluated town-level value scores in `worth_it_by_town.ipynb`.  
- Integrated age-cohort preference weights (e.g., MRT proximity, budget sensitivity) in `age_cohort_value_scores.ipynb`.  
- Prepared figures and insights for PM2 and PM3 presentations.

If you’d like, I can also add badges, a project title, or a cleaner ASCII tree.

