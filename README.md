# Probabilistic Forecasting of Wind and Solar Energy Production in East England

This project transforms multiple .nc and one .csv dataset into a structured Pandas DataFrame, which is then used to train a machine learning regressor (LightGBM).
The model is evaluated using 5-fold cross-validation and performance metrics.

## Project Overview

- **Goal**: Predict the wind and solar energy production from weather data using machine learning.  
- **Model Used**: LightGBM Regressor  
- **Evaluation**: Mean Pinball Loss and cross-validation techniques  
- **Data Processing**: Handling NetCDF data, managing datetime fields, aggregating over spatial dimensions

## Data Requirements

This repository does not include the datasets due to size. You'll need to obtain them separately:

### 4 NetCDF (`.nc`) files:

- `dwd_icon_eu_hornsea_1_20200920_20231027.nc`  
- `dwd_icon_eu_pes10_20200920_20231027.nc`  
- `ncep_gfs_hornsea_1_20200920_20231027.nc`  
- `ncep_gfs_pes10_20200920_20231027.nc`

### 1 CSV (`.csv`) file:

- `Energy_Data_20200920_20231027.csv`

Download the datasets from the IEEE DataPort:  
[https://ieee-dataport.org/competitions/hybrid-energy-forecasting-and-trading-competition](https://ieee-dataport.org/competitions/hybrid-energy-forecasting-and-trading-competition)

After downloading, place them in the project folder, in the same place as `model_lgbm.ipynb`.

The project structure should then look like this:

forecasting_wind_solar_group1  
├── Energy_Data_20200920_20231027.csv  
├── dwd_icon_eu_hornsea_1_20200920_20231027.nc  
├── dwd_icon_eu_pes10_20200920_20231027.nc  
├── ncep_gfs_hornsea_1_20200920_20231027.nc  
├── ncep_gfs_pes10_20200920_20231027.nc  
├── Site Locations (Google Earth Files)/     
├── README.md  
├── LICENSE  
├── model_lgbm.ipynb  
└── requirements.txt

## Setup Instructions

Install dependencies with:  
pip install -r requirements.txt

## Getting Started

Open and run the main notebook `model_lgbm.ipynb`.  
This notebook handles data loading, preprocessing, model training, and evaluation. 


## Contributors

- Guilherme Lopes
- François de Nailly
- Lena Kühn

## License

This project is licensed under the [MIT License](LICENSE).

## Licenses of Dependencies

This project uses the following open-source Python packages:

- [pandas](https://pandas.pydata.org/) – BSD 3-Clause License
- [xarray](https://xarray.dev/) – Apache License 2.0
- [numpy](https://numpy.org/) – BSD License
- [scikit-learn](https://scikit-learn.org/) – BSD 3-Clause License
- [matplotlib](https://matplotlib.org/) – Python Software Foundation License
- [lightgbm](https://lightgbm.readthedocs.io/) – MIT License
- [seaborn](https://seaborn.pydata.org/) – BSD License

All packages are used in accordance with their respective licenses for non-commercial academic purposes.
