# Retail Time Series Forecasting

## Dataset

The dataset used in this project describes superstore sales from 2014 to 2017 and it contains nearly 10,000 entries and 21 features. It contains sales data
for three categories: furniture, technology, and home office. 

## Data Preparation

The dataset was split into 3 sales categories: furniture, technology, and home office. Outliers (88/9994 data points) were then removed from the dataset
to improve results. 

## Models

### ARIMA
 The autoregressive integrated moving average (ARIMA) model is a generalization of an autoregressive moving average (ARMA) model. Both of these models are fitted to time series data either to better understand the data or to predict future points in the series (forecasting). The AR part of ARIMA indicates that the evolving variable of interest is regressed on its own lagged (i.e., prior) values. The MA part indicates that the regression error is actually a linear combination of error terms whose values occurred contemporaneously and at various times in the past. The I (for "integrated") indicates that the data values have been replaced with the difference between their values and the previous values (and this differencing process may have been performed more than once). The purpose of each of these features is to make the model fit the data as well as possible.

### LSTM


### CNN


### Prophet 


### Exponential Smoothing


## Results

