# COMP3522-Singapore: Comprehensive Housing Market Analysis

This repository contains a comprehensive analysis of the Singapore housing market, covering three key sectors: **HDB Resale**, **Private Residential**, and **Rental** markets. The project leverages data analytics, geospatial processing, and machine learning to understand price drivers and identify "value" opportunities for different demographic groups.

## Project Overview

The goal of this project is to provide a holistic view of Singapore's housing landscape. By analyzing transaction data from 2020 to 2025, we aim to:
*   **Predict Prices**: Train machine learning models (XGBoost, LightGBM, etc.) to estimate fair market values.
*   **Identify Value**: Develop "Value Scores" to highlight undervalued properties or districts.
*   **Analyze Demographics**: Tailor insights for specific age cohorts (e.g., 20-29 vs. 40-49) based on their unique preferences for amenities and budget.

## Repository Structure

The codebase is organized into three main directories, each focusing on a specific market segment:

### 1. HDB Resale (`hdb/`)
*   **Focus**: Public housing resale market.
*   **Key Features**:
    *   Analysis of structural, spatial, and temporal patterns.
    *   "Worth the Money" evaluation for different towns.
    *   Age-cohort preference weighting.
*   **Key Notebooks**: `pm3/analysis.ipynb`, `pm3/worth_it_by_town.ipynb`.

### 2. Private Residential (`private/`)
*   **Focus**: Private condominiums and apartments.
*   **Key Features**:
    *   End-to-end pipeline: Data Collection -> Cleaning -> ML.
    *   Geospatial analysis using OneMap API and Data.gov.sg GeoJSONs.
    *   Value scoring for districts based on predicted vs. actual prices.
*   **Key Notebooks**: `private_eda.ipynb`, `data_cleaning.ipynb`, `ml.ipynb`.

### 3. Rental Market (`rental/`)
*   **Focus**: Residential rental transactions.
*   **Key Features**:
    *   Evaluation of rental "worth" across towns.
    *   Integration of accessibility and amenity features.
    *   Production-ready ML pipeline with optimized intermediate files.
*   **Key Notebooks**: `PM2 (EDA)/PM2.ipynb`, `PM3 (ML+Worth It)/PM3.ipynb`.

## Getting Started

Each folder contains its own `README.md` with specific instructions on how to run the notebooks and the required data files. Please refer to the respective directories for detailed documentation.

## Technologies Used

*   **Languages**: Python
*   **Libraries**: Pandas, NumPy, GeoPandas, Plotly, Scikit-learn, XGBoost, CatBoost, LightGBM, SHAP.
*   **Data Sources**: URA Transaction Portal, OneMap API, Data.gov.sg.
