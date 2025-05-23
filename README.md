# Probabilistic Forecasting of Wind and Solar Energy Production in East England

This project transforms multiple .nc and one .csv dataset into a structured Pandas DataFrame, which is then used to train a machine learning regressor (LightGBM).
The model is evaluated using 5-fold cross-validation and performance metrics.

## Project Overview

Goal: Predict the wind and solar energy production from weather data using machine learning.
Model Used: LightGBM Regressor.
Evaluation: Mean Pinball Loss and cross-validation techniques are used for evaluation.
Data Processing: Involves handling NetCDF data, managing datetime fields, and aggregating over spatial dimensions.

## Data Requirements

This repository does not include the datasets due to size. You'll need to obtain them separately:

4 NetCDF (.nc) files:
dwd_icon_eu_hornsea_1_20200920_20231027.nc,
dwd_icon_eu_pes10_20200920_20231027.nc,
ncep_gfs_hornsea_1_20200920_20231027.nc,
ncep_gfs_pes10_20200920_20231027.nc.

1 CSV (.csv) file:
Energy_Data_20200920_20231027.csv.

Please download them from the IEEE DataPort: https://ieee-dataport.org/competitions/hybrid-energy-forecasting-and-trading-competition

## Setup Instructions

Install dependencies:
pip install -r requirements.txt

## Getting Started

Open and run the notebook:
model_lgbm.ipynb
This notebook handles data loading, preprocessing, model training, and evaluation.

## Project Structure

├── dwd_icon_eu_hornsea_1_20200920_20231027.nc      # Data
├── dwd_icon_eu_pes10_20200920_20231027.nc          # Data
├── ncep_gfs_hornsea_1_20200920_20231027.nc         # Data
├── ncep_gfs_pes10_20200920_20231027.nc             # Data
├── model_lgbm.ipynb                                # Main Jupyter notebook
├── README.md                                       # You're reading this
└── requirements.txt                                # Python dependencies

## Contributors

Guilherme Lopes
François de Nailly
Lena Kühn
