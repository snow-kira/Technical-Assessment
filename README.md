# Technical-Assessment

Forecasting Industrial Production of Electric and Gas Utilities
This project builds a model to forecast the industrial production of electric and gas utilities using historical monthly data from January 1939 to September 2022. 

Data Source: Industrial Production: Electric and Gas Utilities Link: https://fred.stlouisfed.org/series/IPG2211A2N

Below is a summary of the steps undertaken:

# 1. Uploading and Preparing Data:
Imported the dataset.

Checked for missing values.

Indexed the data using the date column to create a time series.

# 2. Data Exploration
Performed a decomposition of the time series to analyze trend, seasonality, and residuals.

Conducted visual exploration of the data to identify patterns.

# 3. Stationarity Testing
Applied ADF (Augmented Dickey-Fuller) and KPSS (Kwiatkowski-Phillips-Schmidt-Shin) tests to check for stationarity.

# 4. Autocorrelation Analysis
Plotted ACF and PACF to identify lags for modeling.

# 5. Splitting Data
Split the dataset into training and test sets.

# 6. Model Selection
Selected a SARIMA model for initial forecasting based on data characteristics.

Tuned model orders (p, d, q, P, D, Q, S) iteratively using AIC.

# 7. Forecasting and Visualization
Plotted predictions on the training and test sets.

Visualized the forecasted values along with actual data and confidence intervals.

# 8. Model Evaluation
Assessed model performance using metrics:

Mean Absolute Error (MAE)

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

Diagnosed residuals for:

Normality (Jarque-Bera test, skewness, and kurtosis).

Stationarity (ADF and KPSS).

Autocorrelation (Durbin-Watson and ACF plot).

Heteroskedasticity (visual inspection and statistical tests).
# 9. Box-Cox Transformation
Applied Box-Cox transformation to address heteroskedasticity and non-normality in residuals.

Repeated modeling and evaluation post-transformation.

# Summary
While the SARIMA(1,0,2)x(2,1,1)12 model performed reasonably well, residual diagnostics revealed issues such as heteroskedasticity and non-normality.

Applying Box-Cax transformation improved the model but did not completely eliminate these issues.
