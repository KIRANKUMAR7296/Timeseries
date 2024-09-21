# Time Series 🕐
- Every business operates under risk (based on market conditions) and uncertainty (due to some natural calamity)
- Forecasting helps us to assess these risks, and based on that the budgets can be managed.
- Time series involves analyzing data points collected to identify patterns and trends for predictions.

In simple times we can understand with the following equation:
```
y = f(x)
y: Dependent Variable (Future)
x: Independent Variable (Past)
```

### Properties of Time Series data.
- The data points (time intervals) should be at regular intervals.
- Intervals of Time Series: Yearly, Quarterly (4), Monthly(12), Weekly(52), Daily(365), Hourly.
- Order matters in time series analysis, no data should be missing in the given time intervals.

<table>
  <tr><th colspan=3>Time Series</th></tr>
  <tr><th colspan=2>Systematic Component</th><th colspan=1>Irregular Component</th></tr>
  <tr><td>Trend</td><td>Seasonality</td><td>Unpredicted calamity (Error)</td></tr>
  <tr><td>Long term (Ups and downs)</td><td>Regular pattern</td><td>COVID pandemic or any uncertain natural calamity</td></tr>
</table>  

### Data Visualization
- Create plots (line charts, histograms, scatter plots) to identify trends, seasonality, and other patterns.

### Handle Missing Values
- Apply techniques like imputation or deletion to address missing data.

### Stationarity Check 
- A time series is stationary if its statistical properties remain constant over time.
- Statistical properties: mean, median, mode, variance, std, skewness, autocorrelation.

### Transform Data
- If necessary apply transformation (log transformation, differencing) to stabilize variance or remove trends.
- Differencing: If the series is non-stationary, apply differencing to make it stationary.

### Decomposition of Time Series 
- Breaking of Time Series data into trend, seasonality and irregular components.
- We must find these three components in a given Time Series data.
 
### Decomposition Model
- There are two types of decomposition models.
- Additive model (seasonality is constant): Observation = Trend + Seasonality + Error
- Multiplicative model (seasonality is changing): Observation = Trend * Seasonality * Error

```
Forecasting Sales with Trend, Seasonality and Error:

Sales = Trend (Business Growth) + Seasonality (Weather) + Error (Theft / Calamity)
```

### Statsmodels 
- Python library that provides classes and functions for statistical tests on time series data.

## Time Series Forecasting
- A statistical method used to predict future values of a variable based on its historical data.
- It's particularly useful when dealing with data collected over time.
- Data: Stock prices, sales figures, weather patterns, or economic indicators.

### **Key Concepts:**
1. **Time Series:** A sequence of data points collected over time.
2. **Stationarity:** A time series is stationary if its statistical properties (mean, variance, autocorrelation) remain constant over time.
3. **Trend/Dip:** A long-term upward or downward movement in the data.
4. **Seasonality:** A recurring pattern within a specific period (e.g., yearly, monthly, weekly).
5. **Cyclical Pattern:** A pattern that repeats irregularly over time, often longer than seasonal patterns.

### Common Forecasting Methods:
1. **Naive Forecast:** 
- The simplest method, assuming the next value will be the same as the last.

2. **Moving Average:** 
- Calculates the average of the previous n data points to predict the next value.

3. **Exponential Smoothing:** 
- Assigns exponentially decreasing weights to older observations, giving more importance to recent data.
- Used for time series with trends and seasonality.

4. **Autoregressive Integrated Moving Average (ARIMA):**
- ARIMA models are widely used for modelling stationary time series (No seasonal patterns)
- **AR (Autoregressive):** Model that uses historical data to predict future values.
- **I (Integrated):** Applies differencing to make the series stationary.
- **MA (Moving Average):** The current value is the weighted average of past values + errors.

5. **Seasonal ARIMA (SARIMA):** 
- Extends ARIMA to handle seasonal patterns.

6. **Vector Autoregression (VAR):** 
- VARs are useful when multiple time series are interrelated and influence each other.
- For example, in economics, factors like GDP, inflation, and unemployment rates are often interconnected.
- VAR models capture the relationships between multiple variables.
- VAR consider the lagged values of each variable to understand how past values affect current values.

7. **State-Space Models:** 
- Represent the time series as a dynamic system with hidden states.

### Model Fitting + Evaluation
- Use appropriate statistical forecasting methods based on the data's characteristics.
- Assess the model's performance using metrics like MSE, MAE, RMSE, and R-squared.
- Apply k-fold cross-validation to evaluate the model's generalization ability.

### Applications of Time Series Forecasting:
1. **Finance:** Stock price prediction, risk management, portfolio optimization.
2. **Economics:** GDP forecasting, inflation prediction, sales forecasting.
3. **Weather:** Weather forecasting, climate modelling.
4. **Energy:** Demand forecasting, renewable energy integration.
5. **Healthcare:** Disease outbreak prediction, patient demand forecasting.

### Challenges in Time Series Forecasting:
1. **Non-Stationarity:** Dealing with time series that exhibit trends or seasonality.
2. **Outliers:** Identifying and handling outliers that can significantly affect forecasts.
3. **Model Selection:** Choosing the right model from a variety of options.
4. **Evaluation:** Assessing model performance and selecting the best model.
5. **Uncertainty:** Quantifying uncertainty in forecasts.
