# Nucor Corporation (NUE) Statistical Analysis

A comprehensive financial analysis of Nucor Corporation (NYSE: NUE) using Python for statistical modeling, risk assessment, and performance evaluation.

## Overview

This project provides an in-depth statistical and financial analysis of Nucor Corporation, one of the largest steel producers in the United States. The analysis includes risk metrics, performance comparisons with market indices and industry peers, and various statistical models including CAPM (Capital Asset Pricing Model).

## Features

### Financial Metrics Calculated
- **Return Analysis**: Daily, annualized, and excess returns
- **Risk Metrics**: 
  - Annualized Volatility
  - Maximum Drawdown
  - Value at Risk (VaR)
  - Conditional Value at Risk (CVaR)
- **Risk-Adjusted Performance**:
  - Sharpe Ratio
  - Sortino Ratio
  - Calmar Ratio
- **Market Analysis**:
  - Beta (systematic risk)
  - Alpha (excess return)
  - Correlation analysis with market and peers
- **Additional Metrics**:
  - Win Rate (percentage of positive return periods)
  - Drawdown analysis

### Comparative Analysis
The notebook compares Nucor's performance against:
- **Market Index**: S&P 500 (SPY)
- **Industry Peers**: 
  - Steel Dynamics (STLD)
  - Cleveland-Cliffs (CLF)
  - Steel ETF (SLX)
  - Commercial Metals Company (CMC)
  - ArcelorMittal (MT)

## Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Setup

1. Clone this repository:
```bash
git clone <repository-url>
cd Nucor_Statist
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

Or run the first cell in the notebook, which automatically installs all dependencies.

### Required Packages
- `yfinance` - For downloading financial data
- `pandas` - Data manipulation and analysis
- `numpy` - Numerical computations
- `matplotlib` - Data visualization
- `seaborn` - Statistical data visualization
- `scipy` - Scientific computing and statistics
- `scikit-learn` - Machine learning algorithms (Linear Regression for CAPM)

## Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook NUCOR_Statistical.ipynb
```

2. Run all cells sequentially to:
   - Download the latest market data
   - Calculate financial metrics
   - Generate visualizations
   - Perform statistical analysis

### Configuration

You can modify the following parameters in the notebook:

```python
TICKER = "NUE"                    # Primary stock ticker
MARKET = "SPY"                    # Market index benchmark
PEERS = ["STLD", "CLF", "SLX", "CMC", "MT"]  # Peer companies
START_DATE = "2014-01-01"         # Analysis start date
TRADING_DAYS = 252                # Annual trading days
RISK_FREE = 0.04081               # Risk-free rate (update as needed)
```

## Analysis Components

### 1. Data Collection
- Automatically downloads historical price data using Yahoo Finance API
- Handles missing data and validates data integrity
- Filters data to the most recent 10-year period for analysis

### 2. Return Calculations
- Computes daily simple returns
- Calculates excess returns for CAPM analysis
- Derives risk-free rate adjusted metrics

### 3. Risk Assessment
- Quantifies various risk measures
- Identifies maximum drawdown periods
- Calculates tail risk metrics (VaR and CVaR)

### 4. Performance Evaluation
- Compares risk-adjusted returns across assets
- Evaluates consistency of positive returns
- Assesses downside risk specifically

### 5. Market Relationship Analysis
- CAPM beta calculation using proper excess return methodology
- Alpha generation analysis
- Correlation matrices with market and peers

### 6. Visualizations
- Price performance charts
- Return distributions
- Risk-return scatter plots
- Correlation heatmaps
- Drawdown visualizations

## Methodology

### CAPM (Capital Asset Pricing Model)
The analysis uses the proper CAPM methodology:

```
Expected Return = Risk-Free Rate + Beta × (Market Return - Risk-Free Rate)
```

Where:
- **Beta**: Measures systematic risk relative to the market
- **Alpha**: Excess return not explained by market movements
- **Excess Returns**: Returns adjusted for the risk-free rate

### Risk-Adjusted Metrics

**Sharpe Ratio**: Measures return per unit of total risk
```
Sharpe Ratio = (Annualized Return - Risk-Free Rate) / Annualized Volatility
```

**Sortino Ratio**: Similar to Sharpe but focuses only on downside risk
```
Sortino Ratio = (Annualized Return - Risk-Free Rate) / Downside Deviation
```

**Calmar Ratio**: Return per unit of maximum drawdown
```
Calmar Ratio = Annualized Return / |Maximum Drawdown|
```

## Data Sources

All price data is sourced from Yahoo Finance via the `yfinance` Python library, which provides:
- Historical adjusted closing prices
- Automatic adjustment for splits and dividends
- Reliable data for US equities and ETFs

## Project Structure

```
Nucor_Statist/
│
├── NUCOR_Statistical.ipynb    # Main analysis notebook
├── requirements.txt           # Python dependencies
└── README.md                  # Project documentation
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is for educational and analytical purposes only. The financial data and analysis provided should not be considered as investment advice.

## Disclaimer

This analysis is provided for informational purposes only and should not be construed as financial advice. Always conduct your own research and consult with a qualified financial advisor before making investment decisions.

## Contact

For questions or suggestions, please open an issue in this repository.

---

*Last Updated: November 2025*

