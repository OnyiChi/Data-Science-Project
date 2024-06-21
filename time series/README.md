# Time Series Analysis on Airline Passengers Dataset

## Introduction
This report details the analysis performed on the Airline Passengers dataset, which contains monthly totals of international airline passengers from 1949 to 1960. The primary goal is to analyze the stationarity of the time series data and apply various transformations and models to achieve stationarity and accurate forecasting.

## Data Overview
- Dataset: Airline Passengers which consists of 144 entries.
- Period: anuary 1949 to December 1960
- Variables:
  - year
  - month
  - passengers

## Data Visualization
A line plot was generated to visualize the number of passengers over time.

## Checking Stationarity

### Rolling Statistics

- #### Rolling Mean and Standard Deviation:
  - A 12-month rolling window was used to calculate the rolling mean and standard deviation.
  - Plots showed that while the rolling standard deviation appeared stationary, the rolling mean exhibited a trend, indicating non-stationarity.
    
### Augmented Dickey-Fuller Test

- #### Test Result:
  - Test Statistic: 0.815
  - p-value: 0.991
  - Critical Values:
    - 1%: -3.482
    - 5%: -2.884
    - 10%: -2.579
    
- Conclusion: Since the test statistic is higher than the critical values, the null hypothesis of non-stationarity cannot be rejected.

## Transformations to Achieve Stationarity

### Method 1: Time Shift

- #### First Differencing:
  - The time series was differenced by subtracting the previous month's value.
  - The resulting series showed reduced trends, making the series closer to stationary.
  - Stationarity was tested again using the ADF test, showing improved stationarity but not fully achieving it.

### Method 2: Log Transformation
- #### Log Transformation:
  -   The log of the passenger numbers was taken to stabilize the variance.
  -   Stationarity testing showed the series was still not stationary.
    
### Method 3: Square Root Transformation

- #### Square Root Transformation:
  - The square root of the passenger numbers was taken.
  - ADF test results indicated non-stationarity.

### Method 4: Cube Root Transformation

- #### Cube Root Transformation:
  - The cube root of the passenger numbers was taken.
  - ADF test results still indicated non-stationarity.

### Combined Log and Square Root Transformation

- #### Combined Transformation:
  - Log transformation followed by square root transformation and differencing.
  - ADF test showed improved results but the series was still not stationary.

### Differencing

- #### Seasonal Differencing:
  - The dataset was differenced by 12 months to account for seasonality.
  - Improved stationarity was observed.
    
## Modeling

### ARIMA Model

- The dataset was split into training (70%) and testing (30%) sets.

- An ARIMA(1,1,3) model was fitted on the training data.

- Predictions were made and plotted alongside the actual values.

- RMSE: 111.11

### Seasonal ARIMA (SARIMA) Model

- A SARIMA(1,1,3)(2,1,2,12) model was fitted to account for seasonality.

- Predictions were made and plotted.

- RMSE: 27.50

## Forecasting

- Future dates from January 1961 to December 1962 were generated.
- Predictions for these future dates were made using the SARIMA model.

## Conclusion

- The time series data was initially non-stationary, exhibiting a clear trend.
- Various transformations and differencing methods were applied to achieve stationarity.
- ARIMA and SARIMA models were implemented, with SARIMA showing better performance due to its ability to handle seasonality.
- Future forecasts were made, providing insights into potential passenger numbers for the subsequent two years.
  
The analysis demonstrates the importance of achieving stationarity in time series data for accurate modeling and forecasting.
