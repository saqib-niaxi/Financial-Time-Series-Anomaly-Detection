# Stock Anomaly Detection

Python tool for analyzing Dow Jones Industrial Average data (2018-2023) using Isolation Forest for anomaly detection and LSTM for price forecasting. Includes preprocessing, financial indicators (SMA, EMA, RSI, Bollinger Bands), and visualizations.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/stock-anomaly-detection.git
   cd stock-anomaly-detection
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn tensorflow matplotlib seaborn openpyxl
   ```

3. Add `yahoo_data.xlsx` to the root directory (columns: `Date`, `Open`, `High`, `Low`, `Close*`, `Volume`).

## Usage

### Python Script
Run the script:
```bash
python stock_anomaly_detection.py
```
Outputs:
- Plots in `plots/` (`price_indicators.png`, `rsi.png`, `anomalies.png`, `forecast_deviations.png`, `volume.png`).
- Console report with anomaly and deviation counts.

### Google Colab
1. Open `stock_anomaly_detection.ipynb` in Colab.
2. Upload `yahoo_data.xlsx` to `/content/`.
3. Run cells sequentially to preprocess data, compute indicators, detect anomalies, forecast prices, and visualize results.

## Results

- **Anomalies**: ~63 detected, mostly in volatile periods (e.g., March 2020).
- **Forecasting**: LSTM flags deviations during sudden price changes.
- See `Stock_Anomaly_Detection_Report.md` for detailed analysis and visualizations.

## Contributing

Fork, create a branch, commit changes, and open a pull request. Follow PEP 8 guidelines.

## License

MIT License. See [LICENSE](LICENSE) for details.