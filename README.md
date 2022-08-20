# Retail Time Series Forecasting

## Dataset

The dataset used in this project describes superstore sales from 2014 to 2017 and it contains nearly 10,000 entries and 21 features. It contains sales data
for three categories: furniture, technology, and home office. 

## Data Preparation

The dataset was split into 3 sales categories: furniture, technology, and home office. Outliers (88/9994 data points) were then removed from the dataset
to improve results. 

## Data Exploration



## Models

### ARIMA

The autoregressive integrated moving average (ARIMA) model is a generalization of an autoregressive moving average (ARMA) model. Both of these models are fitted to time series data either to better understand the data or to predict future points in the series (forecasting). The AR part of ARIMA indicates that the evolving variable of interest is regressed on its own lagged (i.e., prior) values. The MA part indicates that the regression error is actually a linear combination of error terms whose values occurred contemporaneously and at various times in the past. The I (for "integrated") indicates that the data values have been replaced with the difference between their values and the previous values (and this differencing process may have been performed more than once). The purpose of each of these features is to make the model fit the data as well as possible.

### LSTM

Long short-term memory (LSTM) is an artificial neural network used in the fields of artificial intelligence and deep learning. The name of LSTM refers to the analogy that a standard RNN has both "long-term memory" and "short-term memory". The connection weights and biases in the network change once per episode of training, analogous to how physiological changes in synaptic strengths store long-term memories; the activation patterns in the network change once per time-step, analogous to how the moment-to-moment change in electric firing patterns in the brain store short-term memories. The LSTM architecture aims to provide a short-term memory for RNN that can last thousands of timesteps, thus "long short-term memory".

### CNN
A convolutional neural network (CNN, or ConvNet) is a class of artificial neural network (ANN), most commonly applied to analyze visual imagery. CNNs are also known as Shift Invariant or Space Invariant Artificial Neural Networks (SIANN), based on the shared-weight architecture of the convolution kernels or filters that slide along input features and provide translation-equivariant responses known as feature maps. CNNs are regularized versions of multilayer perceptrons. Multilayer perceptrons usually mean fully connected networks, that is, each neuron in one layer is connected to all neurons in the next layer. The "full connectivity" of these networks make them prone to overfitting data. Typical ways of regularization, or preventing overfitting, include: penalizing parameters during training (such as weight decay) or trimming connectivity (skipped connections, dropout, etc.) CNNs take a different approach towards regularization: they take advantage of the hierarchical pattern in data and assemble patterns of increasing complexity using smaller and simpler patterns embossed in their filters. Therefore, on a scale of connectivity and complexity, CNNs are on the lower extreme.


### Prophet 

Prophet is a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series that have strong seasonal effects and several seasons of historical data. Prophet is robust to missing data and shifts in the trend, and typically handles outliers well.Prophet is open source software released by Facebook.

### Exponential Smoothing

Exponential smoothing is a rule of thumb technique for smoothing time series data using the exponential window function. Whereas in the simple moving average the past observations are weighted equally, exponential functions are used to assign exponentially decreasing weights over time. It is an easily learned and easily applied procedure for making some determination based on prior assumptions by the user, such as seasonality.

## Results

| Model | MSE | RMSE | MAPE |
| :---  | :---: | :---:  | ---: |
| ARMA   | 87,237.01   | 295.36    |33.88|
| ARIMA | 79,804.31  | 282.5  |35.07  |
| SARIMA 1 | 42,305.37  | 205.68  | 28.89  |
| SARIMA 2 | 55,497.86 | 235.58  | 33.5 |
| DES | 40,4596.36  | 636.08  | 98.79  |
| TES | 49,846.48  | 223.26  | 30.81  |
| Prophet1 | 37,992.52  | 194.92  | 26.67  |
| Prophet2 | 27,986.56 | 167.29  | 22.62 |
| Vanilla LSTM | 18,829.66  | 137.22  | 18.39  |
| Stacked LSTM | 16,515.49  | 128.51  | 17.34  |
| Bidirectional LSTM | 53,981.32  | 232.34  | 31.4  |
| LSTM 1| 68,671.5  | 262.05  | 29.4  |
| CNN| 39,938.47  | 199.85  | 22.26  |
