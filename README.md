# 📈 Stock Market Forecasting

A Python-based exploratory analysis and prediction project that uses **linear regression** to forecast intraday stock price movements. The project investigates whether **opening price** or **trading volume** is a better predictor of a day's high and low prices.

> *"Yes, it's stonks."* 🚀

---

## Overview

This project analyzes historical stock data to understand the relationship between:
- **Open price** → Daily High & Low
- **Volume** → Daily High & Low

Using scikit-learn's Linear Regression, the notebook builds predictive models and visualizes how well each feature explains price movements.

---

## Project Structure

```
Forecasting-of-Stock-Market/
├── stonk.ipynb        # Main Jupyter notebook with analysis & models
├── stock_data.csv     # Stock price dataset (Open, High, Low, Volume, Close)
└── README.md          # This file
```

---

## Dataset

The dataset (`stock_data.csv`) is sourced from **Kaggle** and contains the following columns:

| Column  | Description                    |
|---------|--------------------------------|
| Open    | Opening price for the day      |
| High    | Highest price during the day   |
| Low     | Lowest price during the day    |
| Volume  | Number of shares traded        |
| Close   | Closing price for the day      |

---

## Methodology

### 1. Exploratory Data Analysis
- Scatter plots comparing **Open vs High** and **Open vs Low**
- Scatter plots comparing **Volume vs High** and **Volume vs Low**
- Visual inspection to assess which feature shows a stronger linear relationship with price targets

### 2. Model Training
- **Train/Test Split**: 80% training, 20% testing (`random_state=42`)
- **Model**: `sklearn.linear_model.LinearRegression`
- **Two models**:
  - **Model 1**: Predict High prices from Open prices
  - **Model 2**: Predict Low prices from Open prices

### 3. Results & Visualization
- Predictions plotted against actual values
- Blue/green scatter points = actual prices
- Red line = model predictions

---

## Key Finding

**Open price** is a stronger predictor of both daily High and Low prices compared to Volume. This makes intuitive sense: the opening price sets the baseline for the day's trading range, while volume reflects activity level rather than price direction.

---

## Requirements

```bash
pip install numpy pandas matplotlib scikit-learn jupyter
```

| Package      | Purpose                    |
|-------------|----------------------------|
| numpy       | Numerical operations        |
| pandas      | Data loading & manipulation |
| matplotlib  | Plotting & visualization   |
| scikit-learn| Linear regression model     |
| jupyter     | Running the notebook        |

---

## How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Forecasting-of-Stock-Market.git
   cd Forecasting-of-Stock-Market
   ```

2. **Install dependencies**
   ```bash
   pip install numpy pandas matplotlib scikit-learn jupyter
   ```

3. **Launch Jupyter and open the notebook**
   ```bash
   jupyter notebook stonk.ipynb
   ```

4. **Run all cells** (Cell → Run All) to execute the full analysis

---

## License

This project is open source. Feel free to use, modify, and share.

---

*Built with Python • Powered by stonks* 📊
