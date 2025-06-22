# 📈 Tesla Stock Price Prediction using Machine Learning and LSTM

## 🚀 Project Overview

This project analyzes and predicts **Tesla Inc. (TSLA)** stock prices using both traditional regression and advanced deep learning techniques. The workflow integrates **exploratory data analysis**, **statistical learning**, and **time-series modeling**. To enhance prediction robustness, we incorporate **market-wide indicators**—specifically the **SPY ETF** (representing the S&P 500)—to account for broader economic trends.

The final model leverages a **Long Short-Term Memory (LSTM)** neural network trained on historical TSLA price data to predict future stock values.

---

## 📊 Key Visualizations and Why They Matter

### 1. 📉 Line Plot of TSLA Closing & Opening Prices
- **Purpose:** Observe daily price fluctuations and overall trend.
- **Why:** Helps detect general direction and seasonal behavior.

### 2. 🔄 Pairplot
- **Purpose:** Understand correlation between variables (e.g., open, high, low, volume).
- **Why:** Highlights multicollinearity or redundancy.

### 3. 📈 50-day and 200-day Moving Averages
- **Purpose:** Identify medium and long-term trends.
- **Why:** Common indicators in technical analysis to detect momentum shifts or support/resistance zones.

### 4. 🕯️ Candlestick Chart using Plotly
- **Purpose:** Visualize daily market behavior in detail.
- **Why:** Offers granular insight into volatility and investor sentiment per trading day.

### 5. 🔗 Correlation Heatmap & Line Plot (TSLA vs SPY)
- **Purpose:** Compare Tesla with broader market trends (SPY ETF).
- **Why:** SPY serves as a proxy for macroeconomic behavior—Tesla does not exist in a vacuum. The observed correlation (R ≈ -0.70) justifies its inclusion as a predictive feature.

### 6. 🧠 Actual vs Predicted Prices
- **Purpose:** Visually assess model performance.
- **Why:** Ensures predictions follow realistic stock behavior without overshooting or underfitting.

### 7. 📉 Loss Curve (Training vs Validation)
- **Purpose:** Monitor overfitting during LSTM training.
- **Why:** Helps fine-tune model architecture and regularization.

---

## 🧠 Models Used

### 🔹 Linear Regression
- **Why:** Baseline model for understanding linear relationships between TSLA and SPY prices.
- **Pros:** Interpretable, fast, good starting point.
- **Cons:** Assumes linearity and fails on sequential dependencies.

### 🔹 LSTM (Long Short-Term Memory)
- **Why Chosen:** Financial time series have sequential dependencies and patterns that change over time. LSTM is capable of learning such **long-term temporal patterns** without needing feature engineering.
- **Advantages:**
  - Handles nonlinearities and trends
  - Excellent for sequence data
  - Learns from past 60-day windows to predict future prices

---

## 🔄 Why Include SPY ETF?

Tesla stock often correlates with broader market movements. By merging SPY (an index-tracking ETF for the S&P 500), we capture **market sentiment** and **systemic risk**, which could impact Tesla's price. This **macroeconomic context** improves model accuracy and real-world applicability.

---

## 🧪 Evaluation Metrics

- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score**
- **Visual inspection** (Actual vs Predicted plot)

These metrics offer insight into prediction error and model reliability.

---

## 📦 Dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow yfinance plotly
