# 📈 Stock Price Prediction using Deep Learning

This project predicts future stock prices using historical data and a deep learning model (LSTM). It also visualizes key technical indicators like Exponential Moving Averages (EMA) and compares real vs. predicted trends.

## 🔍 Features

- Predict stock prices using historical data (default: POWERGRID.NS).
- Uses LSTM (Long Short-Term Memory) neural network for time-series prediction.
- Visualizes:
  - 20 & 50 Days EMA
  - 100 & 200 Days EMA
  - Original vs Predicted price trend
- CSV download of stock dataset used
- Simple web interface powered by Flask

## 📁 Project Structure

```
stock_price_prediction/
│
├── app.py                         # Flask app for web interface
├── stock_dl_model.h5              # Trained LSTM model
├── powergrid.csv                  # Sample stock dataset
├── static/
│   ├── AAPL_dataset.csv
│   ├── ema_20_50.png
│   ├── ema_100_200.png
│   └── stock_prediction.png
├── templates/
│   └── index.html                 # HTML template for UI (if included)
├── Stock Price Prediction .ipynb  # Jupyter Notebook (model training & analysis)
└── README.md                      # Project README
```

## 🧠 Model Overview

- **Algorithm**: LSTM Neural Network
- **Frameworks**: TensorFlow/Keras, Scikit-learn
- **Scaler**: MinMaxScaler (to normalize stock prices)
- **Window Size**: 100 previous days used to predict the next

## ⚙️ How to Run

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install flask numpy pandas matplotlib yfinance scikit-learn keras tensorflow
```

### 2. Run the Flask App

```bash
python app.py
```

Visit `http://127.0.0.1:5000/` in your browser.

### 3. Usage

- Enter a stock ticker (e.g., `AAPL`, `INFY.NS`) in the form
- View EMAs, predicted trends, and download dataset

## 📊 Sample Output

- Closing price with EMA overlays
- Prediction vs Real stock price
- Descriptive statistics of the dataset

## 📌 Note

- Default stock used is `POWERGRID.NS` if no input is provided.
- Make sure you are connected to the internet — the app fetches data using `yfinance`.

## 📜 License

This project is for educational purposes.
