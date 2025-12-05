# COMP3522-Singapore: Private Residential Property Analysis

This project analyzes private residential property transactions in Singapore from 2020 to 2025. It involves a complete data pipeline from data collection and cleaning to geospatial analysis and machine learning for price prediction and value scoring.

## Project Overview

The goal of this project is to understand the factors influencing private property prices in Singapore and to develop a model that can predict property prices and identify "value" buys for different demographic groups.

## Data Sources

*   **URA Transaction Portal**: Historical transaction data for private residential properties (2020-2025).
*   **OneMap API**: Used for geocoding transaction addresses to obtain latitude and longitude coordinates.
*   **Data.gov.sg**: GeoJSON files for Singapore's planning areas, districts, and amenities (MRT stations, parks, hawker centres, schools, etc.).

## Project Structure & Workflow

The project is organized into three main Jupyter notebooks that should be executed in the following order:

### 1. Data Collection & EDA (`private/private_eda.ipynb`)
*   **Data Ingestion**: Loads raw transaction data (originally sourced from Azure/URA and saved as CSVs for reproducibility).
*   **Geocoding**: Uses the OneMap API to convert property addresses into geospatial coordinates.
*   **Initial EDA**: Performs preliminary exploratory data analysis to understand the distribution of transactions.

### 2. Data Cleaning & Feature Engineering (`private/data_cleaning.ipynb`)
*   **Data Cleaning**: Handles missing values, corrects data types, and filters outliers.
*   **Spatial Analysis**: Calculates proximity to key amenities using GeoJSON data. Features generated include distance to the nearest MRT station, CBD, schools, and parks.
*   **Output**: Produces a cleaned dataset with rich geospatial features ready for machine learning.

### 3. Machine Learning & Value Analysis (`private/ml.ipynb`)
*   **Model Training**: Trains multiple regression models to predict property prices (log-transformed).
    *   **Models Used**: Linear Regression (Baseline), Random Forest, XGBoost, CatBoost, and LightGBM.
    *   **Performance**: The XGBoost and LightGBM models achieved high accuracy with R² scores > 0.96.
*   **Evaluation**: Compares models using MAE, RMSE, and R². Includes hypothesis testing (Welch's t-test) to analyze price differences between groups (e.g., near vs. far from amenities).
*   **Interpretability**: Uses SHAP (SHapley Additive exPlanations) values to explain model predictions and feature importance.
*   **Value Scoring**: Develops a "Value Score" metric to identify undervalued districts based on predicted vs. actual prices, tailored for specific demographic groups (e.g., Age 20-29, Age 40-49).
*   **Visualization**: Generates interactive Choropleth maps to visualize district-level value scores.

## Requirements

To run this project, you will need the following Python libraries:

*   `pandas`
*   `numpy`
*   `geopandas`
*   `plotly`
*   `scikit-learn`
*   `xgboost`
*   `catboost`
*   `lightgbm`
*   `shap`
*   `scipy`
*   `matplotlib`
*   `seaborn`

## Usage

1.  Ensure all data files are present in the `private/data/` directory.
2.  Run `private/private_eda.ipynb` to process raw data and geocode addresses.
3.  Run `private/data_cleaning.ipynb` to clean the data and generate spatial features.
4.  Run `private/ml.ipynb` to train models, evaluate performance, and generate value insights.
