# Autocorrelation, Partial Autocorrelation Plots and Seasonality, Trend and Noise Plots in Time Series Data

## Description :
In this jupyter notebook, we will learn about autocorrelation and partial autocorrelation plots.

And, also learn how to detect seasonality, trend and noise in time series data.

---
## Contents :
1. Importing the required libraries
2. Loading and Importing the dataset
    - Knowing the dataset
    - Importing the dataset
    - Loading the dataset
3. Data Manipulations
4. Autocorrelation and Partial Autocorrelation
    - Importing the Statmodels library
    - Autocorrelation on time series
    - Partial Autocorrelation on time series
5. Properties of time series - Decomposition
    - Time series Decomposition
    - Plot of time series decomposition
    - Extracting components from time series decomposition
    - **Seasonality component** in time series
    - **Trend component** in time series
    - **Noise component** in time series
6. Conclusion

---
## Data Info :
This time series dataset contains the CO2 measurements at the Mauna Loa Observatory, Hawaii between the years of 1958 and 2001. [(data)](https://github.com/Ravjot03/Visualizing-Time-Series-Data-in-Python/blob/main/Chapter-3/ch2_co2_levels.csv)

---
## Theoretical Concepts :

### Q-1. Autocorrelation
- Autocorrelation is a measure of the correlation between the time series and a delayed copy of itself.

- For example, an autocorrelation of order 3 returns the correlation between a time series at points t_1, t_2, t_3, and its own values lagged by 3 time points, i.e. t_4, t_5, t_6.

- Autocorrelation is used to find repeating patterns or periodic signals in time series data.

- The principle of autocorrelation can be applied to any signal, and not just time series. Therefore, it is common to encounter the same principle in other fields, where it is also sometimes referred to as autocovariance.

### Q-2. Partial Autocorrelation
- The partial autocorrelation measures the correlation coefficient between a time-series and lagged versions of itself. However, it extends this idea by also removing the effect of previous time points.

- For example, a partial autocorrelation function of order 3 returns the correlation between the time series at points t_1 , t_2 , t_3 ,and lagged values of itself by 3 time points t_4, t_5, t_6, but only after removing all effects attributable to lags 1 and 2.

### Q-3. Time Series Decomposition
- In general, most time series can be decomposed in three major components. The first is **seasonality**, which describes the periodic signal in the time series. The second component is **trend**, which describes whether the time series is decreasing, constant or increasing over time. Finally, the third component is **noise (resid/ residuals)**, which describes the unexplained variance and volatility of the time series.

### Q-4. Seasonality Component
- Describes the periodic signal in the time series.
- This extracts and plots the values for the seasonal component. A seasonal pattern exists when a time series is influenced by seasonal factors. Seasonality should always be a fixed and known period.

### Q-5. Trend Component
- Describes whether the time series is decreasing, constant or increasing over time.
- This extracts the trend values of the time series decomposition. The trend component reflects the overall progression of the time series and can be extracted using the `decomposition.trend` command.

### Q-6. Noise Component
- Describes the unexplained variance and volatility of the time series.
- Noise/ Residual components describes random, irregular influences that could not be attributed to either trend or seasonality.

---
