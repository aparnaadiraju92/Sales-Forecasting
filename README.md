# Sales Forecasting

Sales forecasting is the process of estimating future sales. Accurate sales forecasts enable companies to make informed business decisions and predict short-term and long-term performance. Companies can base their forecasts on past sales data, industry-wide comparisons, and economic trends.

## Time Series 

A time series is a sequence of observations taken sequentially in time. Time series analysis involves developing models that best capture or describe an observed time series in order to understand the underlying causes.

# FORECASTING METHODS USED: 

There are several methods to forecast/predict the future sales. Some of the popular concepts that I will be using in this repository are:

1. Popular time series methodoloy - ARIMA/SARIMA

2. Faceboook's Prophet

3. Regression methods -
   a) Multiple Linear Regression
   b) Support Vector Regression
   c) Decision Tree Regression
   d) Random Forest Regression
   e) XGBoost 

## 1. ARIMA

ARIMA is a widely used statistical method for time series forecasting. It stands for *AutoRegressive Integrated Moving Average*. 

AR : AutoRegression - model using dependent relation between observation and some number of lagged observations
I  : Integrated - model using the difference of raw observations (i.e., subtracting an observation from an observation at previous time step) in order to make the time series stationary.
MA : Moving Average - model used dependency between observation and residual error from a moving average model applied to lagged observations.

The parameters of the ARIMA model are defined as follows:

p: The number of lag observations included in the model, also called the lag order.
d: The number of times that the raw observations are differenced, also called the degree of differencing.
q: The size of the moving average window, also called the order of moving average.

### *Components of a Time Series data*
1. Trend : how things are overall changing

2. Seasonality : how things change within a given period (year/month/week/day)

3. Error/Residual/Irregular : activity not explained by the trend or seasonal value

### *Additive and Multiplicative Time Series*
To be able to analyze time series effectively, it is important to understand the interaction between general seasonality in activity and underlying trend. These interactions are classified into Additive or Multiplicative. 

Additive time series - components add together to make time series. If there is an increasing trend, we will observe a roughtly same size peaks/troughs throughout the series i.e., absolute value keeps growing but changes stay relative. The model assumes that the residual are roughly same size throughout the series.

Multiplicative time series - components multiply together to make time series. If there is an increasing trend, the amplitude of seasonal activitiy increases. Common example - web traffic.


## 2. PROPHET
In 2017, Facebook released a forecasting tool Prophet designed for analyzing time series data that display patterns on different time scales such as - yearly, weekly, daily. It also has advanced capabilities for modeling the effect of holidays on time series and implementing custom changepoints.

## 3. REGRESSION ANALYSIS

Regression models (both linear and non-linear) are used for predicting a real value, like salary for example. If your independent variable is time, then you are forecasting future values, otherwise your model is predicting present but unknown values. Regression technique vary from Linear Regression to SVR and Random Forests Regression.

1. Multiple Linear Regression
2. Support Vector Regression
3. Decision Trees
4. Random Forest
5. XGBoost


