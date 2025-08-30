# Twitter Stock Analysis and Forecasting with Prophet

This project analyzes Twitter’s stock market performance using visualization techniques and machine learning–based forecasting.  
The workflow includes data exploration, financial charting, moving average analysis, and stock price prediction using **Facebook Prophet**.

---

## Objectives

- Explore and visualize Twitter stock price trends and trading volumes.  
- Identify key events and their impact on stock prices.  
- Analyze stock movements with **OHLC and candlestick charts**.  
- Apply **moving averages** to study long-term vs short-term market behavior.  
- Build and evaluate a **Prophet forecasting model** for stock price prediction.  

---

## Steps

### 1. Load and Explore Data
- A dataset containing Twitter’s stock prices (`Open`, `High`, `Low`, `Close`, `Volume`) was loaded.  
- Dates were converted into a proper datetime format.  
- Summary statistics were generated to understand stock price distributions and trading volumes.  

---

### 2. Visualize Stock Trends
- Subplots were created to visualize different stock price metrics over time.  
- Trends across `Open`, `High`, `Low`, `Close`, and `Volume` were explored interactively using **Plotly**.  

---

### 3. Yearly Trading Volume Analysis
- A **pie chart** was generated showing the total trading volume by year.  
- This highlighted years with unusually high or low trading activity, providing insight into market interest.  

---

### 4. OHLC and Candlestick Charts
- An **OHLC chart** was built to represent stock price fluctuations, enriched with annotations for major events:  
  - *October 5, 2015*: Jack Dorsey became CEO of Twitter.  
  - *March 15, 2020*: U.S. COVID-19 lockdown began.  
- After the COVID period, a **candlestick chart** was created, focusing on daily averages and identifying the peak post-COVID stock value.  

---

### 5. Moving Average Analysis
- Short-term (10-day), medium-term (50-day), and long-term (200-day) **moving averages** were plotted alongside closing prices.  
- This enabled comparison between daily fluctuations and broader market trends, useful for identifying bullish or bearish momentum.  

---

### 6. Forecasting Stock Prices with Prophet
- Data was prepared for Prophet by renaming columns (`Date → ds`, `Close → y`).  
- Prophet was trained to predict **daily stock prices for the next 365 days**.  
- The model produced forecasts with uncertainty intervals (`yhat_lower`, `yhat_upper`).  
- Components such as **trend** and **seasonality** were plotted for deeper insights.  

---

### 7. Monthly Forecasting
- Prophet was re-trained with adjusted parameters (`changepoint_prior_scale=0.03`) for more flexible trend detection.  
- A **12-month forecast** was generated, providing a medium-term view of expected stock dynamics.  

---

### 8. Model Evaluation
- Model accuracy was assessed using **Mean Absolute Error (MAE)** between actual and predicted values.  
- A comparison line chart was plotted to visualize differences between true and forecasted stock prices.  

---

## Results
- Historical analysis revealed distinct stock behaviors around significant events like leadership changes and the COVID-19 pandemic.  
- Moving averages confirmed **longer-term stability versus short-term volatility**.  
- Prophet successfully captured overall trends and produced **reliable forecasts with interpretable confidence intervals**.  

---
