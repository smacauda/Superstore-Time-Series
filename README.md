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

### Furniture

| Model | MSE | RMSE | MAPE |
| :---  | :---: | :---:  | ---: |
| ARIMA | 39996.01  | 199.99  |28.65 |
| Double Exponential Smoothing | 420545.2 | 648.49 | 100.74 |
| Triple Exponential Smoothing | 40603.56  | 201.5  | 27.45  |
| Prophet | 124539.53  | 291.11  | 0.34  |
| Vanilla LSTM | 18812.36  | 136.3  | 17.81  |
| Stacked LSTM | 21951.72  | 148.16  | 18.36 |
| Bidirectional LSTM | 77062.45  | 277.6  | 29.72 |
| CNN| 55400.07  | 235.37  | 24.86  |

### Technology

Analysis in progress.

[//]: <> (| Model | MSE | RMSE | MAPE |)
[//]: <> (| :---  | :---: | :---:  | ---: |)
[//]: <> (| ARIMA | 142623.98  | 377.66  | 30.27 |)
[//]: <> (| DES | 252679.99  | 502.67  | 76.53 |)
[//]: <> (| TES | 48790.19  | 220.89  | 27.1 |)
[//]: <> (| Prophet | 631328.33  | 663.29  | 0.63  |)
[//]: <> (| Vanilla LSTM | 145070.55  | 380.88  | 131.52 |)
[//]: <> (| Stacked LSTM | 16,515.49  | 128.51  | 17.34  |)
[//]: <> (| Bidirectional LSTM | 53,981.32  | 232.34  | 31.4  |)
[//]: <> (| CNN| 39,938.47  | 199.85  | 22.26  |)

### Office

Analysis in progress.

[//]: <> (| Model | MSE | RMSE | MAPE |)
[//]: <> (| :---  | :---: | :---:  | ---: |)
[//]: <> (| ARIMA | 70427.02  | 265.38  | 25.26  |)
[//]: <> (| DES | 238122.24  | 487.98  | 74.9 |)
[//]: <> (| TES | 91942.47  | 303.22  | 43.93  |)
[//]: <> (| Prophet | 183175.03  | 385.51  | 0.49  |)
[//]: <> (| Vanilla LSTM | 18,829.66  | 137.22  | 18.39  |)
[//]: <> (| Stacked LSTM | 16,515.49  | 128.51  | 17.34  |)
[//]: <> (| Bidirectional LSTM | 53,981.32  | 232.34  | 31.4  |)
[//]: <> (| CNN| 39,938.47  | 199.85  | 22.26  | )

