# Stock Price Prediction
Using a deep learning (ML) model to predict Stock prices using Time series data

## 🎯 Business Problem

This project develops a deep learning model to predict Tesla stock prices using historical price and volume data. Long Short-Term Memory (LSTM) neural networks are employed to capture temporal dependencies in stock price movements, enabling investors to make data-driven trading decisions.

**Key Business Question:** Can we accurately predict future stock prices using historical OHLCV (Open, High, Low, Close, Volume) data with LSTM deep learning models?

## 📁 Repository Structure

```
Stock_Prediction.ipynb
├── 1. Imports & Environment Setup
├── 2. Data Loading & EDA
├── 3. Data Preprocessing
│   ├── Feature Scaling (MinMaxScaler)
│   ├── Time Series Preparation
│   └── Train-Test Split
├── 4. LSTM Model Development
├── 5. Model Training
│   ├── Optimization & Loss Function
├── 6. Prediction & Evaluation
│   ├── Stock Price Predictions
│   ├── Visualizations (Plotly)
│   └── Performance Metrics
└── 7. Results Analysis

TSLA.csv - Tesla historical stock price data
```
## ⚒️ Tools and Programming Languages

- **Language:** Python 3
- **Deep Learning:**
  - TensorFlow (computational framework)
  - Keras Sequential Models
  - LSTM (Long Short-Term Memory) layers
  - Dense layers
  - Dropout regularization
- **Data Processing:**
  - Pandas (time series data manipulation)
  - NumPy (numerical computations)
- **Data Scaling:**
  - MinMaxScaler (feature normalization to [0,1] range)
  - StandardScaler (alternative normalization)
- **Evaluation Metrics:**
  - RootMeanSquaredError (RMSE)
  - Custom loss functions
- **Visualization:**
  - Plotly (interactive financial charts)
  - Matplotlib & Seaborn (static plots)

## 🔑 Key Insights & Results

### Dataset Characteristics
- **Data Source:** Tesla (TSLA) historical stock prices
- **Features:** Open, High, Low, Close, Adjusted Close, Volume
- **Time Series:** Chronologically sorted daily stock data

### Reproducibility & Configuration
- **Fixed Random Seed:** SEED = 42 for reproducible results
- **Environment Variables Set:**
  - Python hash seed for consistent randomization
  - TensorFlow deterministic operations enabled
  - Single-threaded execution for GPU consistency
- **Purpose:** Ensures model results are reproducible across different runs

### Data Preprocessing
- **Feature Scaling:** MinMaxScaler used to normalize prices to [0,1] range
- **Volume Analysis:** Tracked trading volume trends over time
- **Price Tracking:** Monitored open, high, low, and close prices

### Model Architecture
- **Type:** Sequential LSTM Neural Network
- **Layers:**
  - Multiple LSTM layers capturing temporal patterns
  - Dropout layers for regularization (preventing overfitting)
  - Dense output layer for price prediction
- **Loss Function:** RMSE for continuous stock price prediction

### Key Performance Metrics
- **Root Mean Squared Error (RMSE):** Primary evaluation metric
- **Time Series Validation:** Walk-forward validation approach

### Business Applications
1. **Price Forecasting:** Predict future Tesla stock prices
2. **Trading Signals:** Generate buy/sell signals based on predictions
3. **Risk Management:** Estimate price volatility and trading risk
4. **Portfolio Management:** Use predictions for investment decisions

### 🏆 Best Model & Performance

**Winning Model:** LSTM (Long Short-Term Memory) Neural Network

**Key Performance Metrics:**
- **Mean Absolute Percentage Error (MAPE):** 5.45%
- **Root Mean Squared Error (RMSE):** Calculated on test predictions
- **Mean Absolute Error (MAE):** Calculated on test predictions
- **Architecture:** 
  - Layer 1: LSTM(64 units) with return_sequences=True
  - Layer 2: LSTM(128 units) with return_sequences=False
  - Layer 3: Dense(64 units) with ReLU activation
  - Layer 4: Dropout(0.3) for regularization
  - Output: Dense(1 unit) for price prediction
- **Training Configuration:**
  - Optimizer: Adam
  - Loss Function: MAE (Mean Absolute Error)
  - Metrics: RootMeanSquaredError
  - Batch Size: 32, Epochs: 20
- **Validation Method:** 60-day sliding window for time series preparation
- **Model Assessment:** MAPE of **5.45%** indicates excellent predictive accuracy

[!Prediction_plot](images/Stock_Prediction.ipynb)

### Technical Achievements
- Proper reproducibility setup for reliable model training
- Advanced deep learning with LSTM for sequence prediction
- Interactive visualizations for financial analysis
- Scalable architecture for other stock predictions
