### Project Title

**Wind Speed and Direction Prediction Using LSTM , ARIMA, Prophet**

### README

---

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Model Evaluation](#model-evaluation)
- [Results](#results)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project focuses on the analysis and prediction of wind speed and direction using historical weather data. The main objectives of this project are:

1. **Data Preprocessing:** Cleaning and preparing the dataset by handling missing values and transforming data for analysis.
2. **Data Exploration:** Visualizing the wind speed and direction for different weather stations to understand patterns and trends.
3. **Statistical Model Evaluation:** Comparing the performance of different weather prediction models (ICON-D2, ICON-EU, ERA5) by calculating key statistical metrics such as Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and correlation coefficients.
4. **Time Series Forecasting:** Building and training an LSTM (Long Short-Term Memory) model to predict future wind speeds and directions.
5. **Visualization of Results:** Comparing actual vs predicted values through various plots to assess model performance.

## Dataset

The dataset used in this project is a NetCDF file (`wind_2023.nc`) containing wind speed and direction data from multiple weather stations. The key variables in the dataset include:

- **Measured Wind Speed:** Actual wind speed recorded at the stations.
- **Measured Wind Direction:** Actual wind direction recorded at the stations.
- **ICON-D2 Wind Speed:** Predicted wind speed from the ICON-D2 model.
- **ICON-EU Wind Speed:** Predicted wind speed from the ICON-EU model.
- **ERA5 Wind Speed:** Predicted wind speed from the ERA5 model.
- **ICON-D2 Wind Direction:** Predicted wind direction from the ICON-D2 model.
- **ICON-EU Wind Direction:** Predicted wind direction from the ICON-EU model.
- **ERA5 Wind Direction:** Predicted wind direction from the ERA5 model.

## Installation

To run this project, you need to have Python installed along with the required libraries. Follow these steps to set up the environment:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/wind-prediction-lstm.git
   cd wind-prediction-lstm
   ```

2. **Install the required libraries:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Download the dataset:**
   Ensure the `wind_2023.nc` dataset is in the project directory. If not, obtain the dataset and place it in the project folder.

## Usage

To run the analysis and prediction, execute the script:

```bash
python wind_prediction.py
```

This will perform data preprocessing, model evaluation, LSTM-based forecasting, and generate various plots to visualize the results.

## Project Structure

```
wind-prediction-lstm/
│
├── wind_prediction.py         # Main script containing the code
├── wind_2023.nc               # Dataset (not included, must be added manually)
├── requirements.txt           # List of required libraries
├── README.md                  # Project readme file
└── results/                   # Folder containing generated plots and evaluation metrics
```

## Model Evaluation

The project evaluates the performance of three weather prediction models (ICON-D2, ICON-EU, ERA5) by calculating the following metrics:

- **Mean Absolute Error (MAE):** Measures the average magnitude of errors between predicted and actual values.
- **Root Mean Squared Error (RMSE):** Quantifies the square root of the average squared differences between predicted and actual values.
- **Correlation Coefficient:** Indicates the strength and direction of the linear relationship between predicted and actual values.

These metrics are computed for both wind speed and direction across different weather stations.

## Results

The results include:

1. **Plots** showing the actual vs predicted wind speed and direction for each weather station.
2. **Summary tables** displaying the MAE, RMSE, and correlation for each model.
3. **Heatmaps** visualizing the overall performance of the models across all stations.

The LSTM model is also evaluated for its ability to predict future wind speeds and directions.

## Future Work

- **Model Tuning:** Further tuning the LSTM model hyperparameters to improve forecasting accuracy.
- **Feature Engineering:** Incorporating additional meteorological variables to enhance model predictions.
- **Real-Time Forecasting:** Extending the model to make real-time predictions using live data feeds.

## Contributing

Contributions are welcome! If you find a bug or have a feature request, please create an issue or submit a pull request.
