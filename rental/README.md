This directory contains the full workflow for analysing Rental data in Singapore and evaluating whether different towns are “worth the money” after adjusting for structural, accessibility, and amenity features. The methodology also incorporates age-cohort preferences (20–29 vs 40–49).

---

## Folder Structure

- `rental/`
  - `PM2 (EDA)/`
    - `PM2.ipynb` — Progress Meeting 2 analysis notebook  
    - `RentingOutofFlats2025.csv` — Input file for PM2 consisting of all rental transactions in Singapore 2021 onwards  
  - `PM3 (ML + Worth It)/`
    - `PM3.ipynb` — Progress Meeting 3 analysis notebook covering Model Training & Worth It analysis  
    - `Input/` — All input files (rental data transactions & amenities locations) required for the notebook to run
    - `Intermediate Files/` — 2 files pre uploaded to save user time ~10 hours where `PM3.ipynb` geocodes transactions and calculates amenities distances   
  - `README.md`

---

## Running the Code

-  `PM2 (EDA)`
    - Run `PM2` Notebook
      
-  `PM3 (ML + Worth It)`
    - Run `PM3` Notebook
      - The entire code takes ~10 hours to complete, hence to make the result production faster, skip code block 4 & 7 (tagged with a comment to skip)
      - Files generated from block 4 & 7 are present in the `Intermediary Files` folder to shorten code run time
      - Subsequently, the succeeding code blocks 5 and 8 respectively, utilise the files from `Intermediary Files` folder to shorten run time

## Summary of Work

- Conducted EDA on Rental transactions to identify structural, spatial, and temporal patterns.  
- Built accessibility and amenity features for fair price comparison across towns.  
- Trained models in `PM3.ipynb` to estimate fair values and extract important drivers.  
- Evaluated town-level value scores in `PM3.ipynb`.  
- Integrated age-cohort preference weights (e.g., MRT proximity, budget sensitivity) in `PM3.ipynb`.  
- Prepared figures and insights for PM2 and PM3 presentations.
