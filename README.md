# Time Series Forecasting with Prophet

This project uses the Prophet library to perform time series forecasting.

## Dependencies

The project requires the following Python libraries:

- **pystan**: A Python interface to Stan, a package for Bayesian inference. Stan is used for statistical modeling, data analysis, and prediction in various fields.

- **prophet**: Prophet is a forecasting procedure implemented in R and Python. It is fast and provides completely automated forecasts that can be tuned by hand by data scientists and analysts.

- **pandas**: A software library written for the Python programming language for data manipulation and analysis. It offers data structures and operations for manipulating numerical tables and time series.

You can install these dependencies using pip:

```python
!pip install pystan prophet pandas
```

# Data Processing
The data is read from a CSV file named ‘dataset.csv’. The ‘Time Date’ column is processed to extract ‘Year’, ‘Month’, and ‘Day’, and a new datetime column ‘ds’ is created.

The unnecessary columns are dropped, and the remaining columns are renamed to ‘y’ and ‘ds’ to fit the input format required by Prophet.

# Model Training
A Prophet model is created with an interval width of 0.95 and daily seasonality enabled. The model is then fitted on the processed data.

# Forecasting
A future dataframe is created for a period of 100 days, and predictions are made using the fitted model. The forecasted data includes components like trend, yearly seasonality, and weekly seasonality.

# Visualization
The forecasted data is visualized using Prophet’s built-in plotting functions. These plots provide a clear view of the original data, the forecasted data, as well as the components of the forecast.

