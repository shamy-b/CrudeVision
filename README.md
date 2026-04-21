# 🛢️ CrudeVision: Crude Oil Price Forecasting & Analytics

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.15-orange.svg)](https://www.tensorflow.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.32-FF4B4B.svg)](https://streamlit.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**CrudeVision** is an enterprise-grade deep learning pipeline designed to forecast Crude Oil (WTI) prices. Leveraging a **Stacked LSTM (Long Short-Term Memory)** architecture and advanced Technical Analysis, it provides traders and analysts with actionable insights through a high-performance interactive dashboard.

---

## 🚀 Key Features

*   **Deep Learning Engine**: Stacked LSTM network regularized with L2 and Dropout to capture complex temporal dependencies.
*   **Technical Indicator Suite**: Automatic generation of 30+ features including RSI, MACD, Bollinger Bands, ATR, and multiple SMAs/EMAs.
*   **Recursive Forecasting**: Multi-step inference engine capable of predicting price trends up to 14 days into the future.
*   **Robust Preprocessing**: Automatic handling of "Black Swan" events (like the 2020 negative price crash) using Huber Loss functions.
*   **Interactive Analytics**: A modern Streamlit dashboard featuring Plotly candlestick charts, momentum gauges, and forecast overlays.

---

## 🛠️ Tech Stack

| Category | Tools |
| :--- | :--- |
| **Language** | Python 3.9+ |
| **Deep Learning** | TensorFlow, Keras |
| **Data Science** | Pandas, NumPy, Scikit-Learn |
| **Financial Analysis** | `ta` (Technical Analysis Library), Statsmodels |
| **Visualization** | Plotly, Matplotlib, Seaborn |
| **Deployment** | Streamlit |

---

## 📈 Model Performance

The model is evaluated on a held-out test set (the most recent 15% of historical data) to ensure real-world reliability.

*   **RMSE**: `$2.76`
*   **MAE**: `$1.95`
*   **MAPE**: `2.59%`

> [!TIP]
> The use of **Huber Loss** allows the model to ignore extreme volatility noise while remaining highly sensitive to actual price trends.

---

## 💻 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/CrudeVision.git
   cd CrudeVision
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Pipeline**:
   Open `pipeline.ipynb` to train the model or run the analytics.

4. **Launch the Dashboard**:
   ```bash
   streamlit run app.py
   ```

---

## 📊 Dataset

| Column | Description |
| :--- | :--- |
| `Date` | Trading date (YYYY-MM-DD) |
| `Open` | Opening price (USD) |
| `High` | Daily high price (USD) |
| `Low` | Daily low price (USD) |
| `Close` | Closing price (USD) |
| `Volume` | Trading volume |
| `Daily_Return_%` | Daily return percentage |
| `Intraday_Volatility` | Intraday volatility measure |

---

## 🧬 Project Structure

```text
├── Crude_Oil.csv          # Historical dataset (2000 - Present)
├── pipeline.ipynb         # Full End-to-End Research Pipeline (EDA -> Training)
├── crude_oil_lstm.keras   # Pre-trained Stacked LSTM Model
├── app.py                 # Streamlit Interactive Dashboard
├── requirements.txt       # Environment Dependencies
└── README.md              # Project Documentation
```

---

## 🔭 Roadmap

- [ ] **Exogenous Variables**: Integrate US Dollar Index (DXY) and Gold (XAU) correlations.
- [ ] **Sentiment Analysis**: Scrape energy news and Twitter (X) sentiment for "fear/greed" indexing.
- [ ] **Transformer Architecture**: Experiment with Temporal Fusion Transformers (TFT) for longer-range forecasting.

---

## ⚖️ License

Distributed under the MIT License. See `LICENSE` for more information.

---
**Developed with ❤️ by [Your Name/Handle]**
