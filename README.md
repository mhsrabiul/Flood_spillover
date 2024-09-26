# Flood Spillover Prediction Using Spatial Lag Model (SLM) and Spatial Error Model (SEM)

This repository contains code and data used for analyzing flood spillovers in Bangladesh, using the Spatial Lag Model (SLM) and Spatial Error Model (SEM). The analysis is performed on a dataset that includes various meteorological features and station information across different time periods. The goal is to understand both direct flood predictions and indirect spillover effects between stations.

## Dataset

The dataset used in this project includes the following features:

- **Station_Names:** Identifier for different weather stations
- **Year:** Year of the recorded data
- **Month:** Month of the recorded data
- **Rainfall (mm):** Amount of rainfall recorded
- **Relative_Humidity (%):** Percentage of relative humidity
- **Wind_Speed (m/s):** Wind speed recorded
- **Cloud_Coverage (okta):** Cloud coverage measured in oktas
- **Bright_Sunshine (hours):** Duration of bright sunshine hours
- **Station_Number:** Numeric identifier for each station
- **X_COR:** X-coordinate (for spatial analysis)
- **Y_COR:** Y-coordinate (for spatial analysis)
- **LATITUDE:** Latitude of the station
- **LONGITUDE:** Longitude of the station
- **ALT (m):** Altitude of the station
- **Period:** Time period of the data recording
- **Flood? (binary):** Indicator for flood occurrence
- **Temp_Range (°C):** Range of temperature recorded

### Data Source

The dataset for this analysis was obtained from another GitHub repository. Please ensure proper citation of the dataset as follows:

Gauhar, N., Das, S., & Moury, K. S. (2021). Prediction of flood in Bangladesh using k-nearest neighbors algorithm. In *2021 2nd International Conference on Robotics, Electrical and Signal Processing Techniques (ICREST)* (pp. 357–361). IEEE.


## Project Files

- **Flood_spillover.ipynb**: The main Jupyter notebook for flood prediction and spillover analysis using SLM and SEM models. It includes data preprocessing, spatial analysis, and model evaluation.
- **Data**: The folder containing the dataset used for analysis.
- **ShapeFiles**: Contains shapefiles used for mapping and spatial analysis.
- **README.md**: This file.

## Methodology

This project applies spatial econometrics to predict flood occurrences and analyze spillovers. The models implemented include:

- **Spatial Lag Model (SLM)**: Captures the spatial dependency of flood occurrences, where the flood risk in one station is influenced by its neighboring stations.
- **Spatial Error Model (SEM)**: Focuses on the spatial dependence in the error terms, addressing unobserved factors shared across neighboring stations.

Both models are compared for performance, and spillover-prone stations are highlighted using a heatmap of Bangladesh.

## Results

The spatial models reveal significant spillover effects, with certain stations showing higher indirect flood risks based on their neighbors' conditions. The temporal component is also examined to understand how flood risks evolve over time across different regions.

## How to Run the Code

1. Clone the repository:
```bash
   git clone https://github.com/mhsrabiul/Flood_spillover.git

2. Install the required libraries:
```bash
   pip install -r requirements.txt

## Citations
If you use this dataset in your research, please cite the dataset as mentioned above.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
