# Chapter 8 -- Forecasting

*Operations Management -- R. Dan Reid & Nada R. Sanders*

------------------------------------------------------------------------

## Learning Objectives

-   Identify principles of forecasting
-   Explain the steps in the forecasting process
-   Identify types of forecasting methods and their characteristics
-   Describe time series models
-   Describe causal modeling using linear regression
-   Perform time series and causal calculations in Excel
-   Compute forecast accuracy

------------------------------------------------------------------------

## What Is Forecasting?

-   Forecasting = predicting future events to support decisions
-   Goal: produce good forecasts on average over time and keep errors low
-   Forecasting is an ongoing, iterative process

------------------------------------------------------------------------

## Core Principles of Forecasting

-   Forecasts are rarely perfect
-   Forecasts are more accurate for **groups** than for individuals
-   Forecasts are more accurate for **short-term** horizons than for long-term

------------------------------------------------------------------------

## The Forecasting Process

1.  Decide what to forecast (detail level, units, time horizon)
2.  Evaluate and analyze data (needed vs. available)
3.  Select and test a model (cost, ease of use, accuracy)
4.  Generate the forecast
5.  Monitor accuracy over time and adjust

------------------------------------------------------------------------

## Types of Forecasting Methods

### Qualitative (Judgment-Based)

-   Based on human judgment, expertise, opinion
-   Useful when historical data is scarce or for new products/markets
-   Examples: Delphi method, expert panels, market research

### Quantitative (Model-Based)

-   Based on mathematical modeling of data
-   Objective and reproducible
-   Two broad categories:
    -   **Time Series Models** -- forecast based on past data patterns
    -   **Causal (Associative) Models** -- forecast based on external variables

------------------------------------------------------------------------

## Time Series Models

-   Assumes data = **historical pattern + random variation**
-   Patterns in data:
    -   **Level (horizontal)** -- fluctuates around a constant mean
    -   **Trend** -- consistent upward or downward movement
    -   **Seasonality** -- regular repeating pattern of fixed length (e.g., quarterly sales, holiday demand)
    -   **Cycles** -- long-term up and down fluctuations (e.g., economic cycles)
    -   **Random variation** -- unpredictable noise

------------------------------------------------------------------------

## Common Time Series Models

### Naïve Method

-   Forecast for next period = actual value from last period
-   Simple and effective for level data or as a baseline

$F_{t+1} = A_t$

The **Naïve Method** is expressed as:

where  

- $F_{t+1}$ = forecast for the next period  
- $A_t$ = actual value in the current period 

### Simple Mean

-   Forecast = average of all past data
-   Works best for stable level series, poor when trend/seasonality exists

The **Simple Mean** method is expressed as:

$F_t = \dfrac{1}{n} \sum_{i=1}^{n} A_i$

where  

- $F_t$ = forecast for period $t$  
- $A_i$ = actual value in period $i$  
- $n$ = number of past periods  

### Simple Moving Average

-   Forecast = average of most recent n observations
-   Each new forecast drops oldest value, adds newest
-   Smooths random noise, but lags behind if trend exists

The **Simple Moving Average** method is expressed as:

$F_{t+1} = \dfrac{A_t + A_{t-1} + \cdots + A_{t-n+1}}{n}$

where  

- $F_{t+1}$ = forecast for the next period  
- $A_t, A_{t-1}, \dots, A_{t-n+1}$ = actual values of the most recent $n$ periods  
- $n$ = number of periods included in the average 

### Weighted Moving Average

-   Forecast = weighted average of recent n observations
-   Weights must sum to 1.0
-   More responsive to recent changes than simple moving average


The **Weighted Moving Average** method is expressed as:

$F_{t+1} = w_1 A_t + w_2 A_{t-1} + \cdots + w_n A_{t-n+1}$

where  

- $F_{t+1}$ = forecast for the next period  
- $A_t, A_{t-1}, \dots, A_{t-n+1}$ = actual values of the most recent $n$ periods  
- $w_1, w_2, \dots, w_n$ = weights assigned to each period (with $\sum_{i=1}^n w_i = 1$) 

### Exponential Smoothing

-   Most commonly used due to simplicity and minimal data needs
-   Formula:
    -   Ft+1 = Ft + α(At − Ft)
    -   Ft = forecast for current period
    -   At = actual value for current period
    -   α = smoothing constant (0 < α < 1)
-   Higher α → forecast responds more strongly to recent changes


The **Exponential Smoothing** method is expressed as:

$F_{t+1} = F_t + \alpha (A_t - F_t)$

or

$F_{t+1} = \alpha A_t + (1 - \alpha) F_t$

where  

- $F_{t+1}$ = forecast for the next period  
- $F_t$ = forecast for the current period  
- $A_t$ = actual value in the current period  
- $\alpha$ = smoothing constant, $0 < \alpha < 1$  

------------------------------------------------------------------------

## Linear Trend Line

-   Models a trend with a straight line equation:
    -   Y = a + bx
    -   Y = forecast for period x
    -   a = intercept (value of Y when x = 0)
    -   b = slope (rate of change per time period)

------------------------------------------------------------------------

## Forecasting Seasonality

-   Seasonal = regularly repeating pattern each year/period
-   **Seasonal Index** = how much each season differs from the average

**Steps to forecast seasonality:**
1. Calculate average demand per season  
2. Compute seasonal index for each season: (actual ÷ average)  
3. Average indexes across years  
4. Forecast next year's total demand → divide evenly by number of seasons  
5. Multiply by each seasonal index to get seasonal forecasts  

------------------------------------------------------------------------

## Causal (Associative) Models

-   Forecasting based on cause-and-effect with outside variables
-   Example: housing starts predict appliance sales

### Linear Regression

-   Equation: Y = a + bX
    -   Y = dependent variable (forecast)
    -   X = independent variable (predictor)
-   Used to model relationship between two variables

**Measures of fit:**  
- **Correlation coefficient (r):** direction and strength of linear relationship (closer to ±1 = stronger)  
- **Coefficient of determination (r²):** percentage of variation in Y explained by X  

### Multiple Regression

-   Forecasts based on several independent variables
-   Equation: Y = B0 + B1X1 + B2X2 + ... + BkXk
-   Can model both **trend** (time variable) and **seasonality** (dummy binary variables)

------------------------------------------------------------------------

## Measuring Forecast Accuracy

-   Forecasts will never be perfect → need metrics to measure error

**Common measures:**  
- **MAD (Mean Absolute Deviation):** average of absolute errors  
- **MSE (Mean Squared Error):** squares errors → penalizes large deviations  
- **CFE (Cumulative Forecast Error):** tracks total bias (over/under forecasting)  
- **Tracking Signal (TS):** ratio of CFE to MAD  
- TS = CFE / MAD  
- If TS exceeds ±4, review model  

------------------------------------------------------------------------

## Selecting the Right Model

Depends on:  
1. Amount and type of data available  
2. Desired accuracy  
3. Forecast horizon (short vs. long term)  
4. Data patterns (trend, seasonality, cycles)  

------------------------------------------------------------------------

## Forecasting in Operations Management

Forecasts drive nearly all major operations decisions:  
- Product design (Ch. 2)  
- Quantity to produce (Ch. 5 & 6)  
- Materials and supplies needed (Ch. 12)  
- Facility space requirements (Ch. 10)  
- Capacity and location (Ch. 9)  
- Labor scheduling (Ch. 11)  

Forecasts also support strategic decisions:  
- Competitive priorities  
- Technology investments  
- Tactical planning (e.g., work schedules)  

------------------------------------------------------------------------

## Forecasting Across the Organization

-   **Marketing:** demand, sales, promotions
-   **Finance:** stock prices, capital investment, cash flow
-   **Human Resources:** hiring needs, training schedules
-   **Information Systems:** shared databases for forecasting

------------------------------------------------------------------------

## Chapter 8 Highlights

-   Forecasts are rarely perfect, more accurate for groups, and more accurate short term than long term
-   Five steps: decide → data → model → forecast → monitor
-   Two main methods:
    -   Qualitative (judgment-based)
    -   Quantitative (math-based)
-   Time series models: Naïve, mean, moving averages, exponential smoothing
-   Causal models: regression (linear, multiple)
-   Accuracy measures: MAD, MSE, CFE, tracking signal
-   Model selection depends on data, accuracy needs, horizon, and data patterns

------------------------------------------------------------------------

## Chapter 8 Key Takeaways

-   Core quantitative tools to master:
    -   Moving Averages
    -   Exponential Smoothing
    -   Linear Regression
-   Quantitative methods are relatively simple but highly effective
-   Understanding the **logic** of methods is as important as memorizing formulas
