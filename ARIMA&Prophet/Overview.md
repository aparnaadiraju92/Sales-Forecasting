# TIME SERIES FORECASTING

A time series is a sequence of observations taken sequentially in time. Time series analysis involves developing models that best capture or describe an observed time series in order to understand the underlying causes.

# BACKGROUND

### *Components of a Time Series data*
1. Trend : how things are overall changing

2. Seasonality : how things change within a given period (year/month/week/day)

3. Error/Residual/Irregular : activity not explained by the trend or seasonal value

### *Additive and Multiplicative Time Series*
To be able to analyze time series effectively, it is important to understand the interaction between general seasonality in activity and underlying trend. These interactions are classified into Additive or Multiplicative. 

Additive time series - components add together to make time series. If there is an increasing trend, we will observe a roughtly same size peaks/troughs throughout the series i.e., absolute value keeps growing but changes stay relative. The model assumes that the residual are roughly same size throughout the series.

Multiplicative time series - components multiply together to make time series. If there is an increasing trend, the amplitude of seasonal activitiy increases. Common example - web traffic.

### *Choosing a Model*

1. ARIMA models - appropriate for stationary data only. Remove trend before applying model.

2. [Exponential smoorting](https://machinelearningmastery.com/exponential-smoothing-for-time-series-forecasting-in-python/) - appropriate for non-stationary data (i.e., data with trend and seasonal data). 

  a. Simple Exponential smoothing : used when there are few data points, data is irregular, no seasonality or trend. Forecast is made of just one component - level which is the weighted average of previous level and current observation.

  b. Holt's Linear smoothing : used when there is trend in data and no seasonality. Forecast is made of level component and trend component.

# FORECASTING METHODS USED: 

## 1. ARIMA

ARIMA is a widely used statistical method for time series forecasting. It stands for *AutoRegressive Integrated Moving Average*. 

AR : AutoRegression - model using dependent relation between observation and some number of lagged observations.

I  : Integrated - model using the difference of raw observations (i.e., subtracting an observation from an observation at previous time step) in order to make the time series stationary. 

MA : Moving Average - model used dependency between observation and residual error from a moving average model applied to lagged observations.

The parameters of the ARIMA model are defined as follows:

p: The number of lag observations included in the model, also called the lag order.  A weighted sum of lagged values of the series. (AR part)

d: The number of times that the raw observations are differenced, also called the degree of differencing. A difference of time series (I part)

q: The size of the moving average window, also called the order of moving average. A weighted sum of lagged forecasted errors of the series (MA part)

There are several multiple ways to choose p,d,q values for the ARIMA model. In this project, I have used the Akaike Information Critera (AIC) is the used measure. It basically quantifies : the goodness of fit, and the simplicity of the model. When comparing two models, the one with the lower AIC is generally “better”.

## 2. PROPHET
In 2017, Facebook released a forecasting tool Prophet designed for analyzing time series data that display patterns on different time scales such as - yearly, weekly, daily. It also has advanced capabilities for modeling the effect of holidays on time series and implementing custom changepoints.
