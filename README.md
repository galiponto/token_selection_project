# **Token Selection Project**

This project automates the selection and analysis of cryptocurrency tokens by fetching historical and current data from CoinGecko and calculating various features. The final dataset is optimized for identifying high-value altcoins and evaluating their risk and reward profiles.

---

## **Features**

The project calculates a comprehensive set of features for each token, grouped into the following categories:

### **1. Price Metrics**
- Current price, mean, median, and quantiles over various timeframes (3, 7, 30, 90, 365 days).

### **2. Volatility Metrics**
- Standard deviation, upside and downside volatility, relative volatility to BTC/ETH.

### **3. Drawdown Metrics**
- Maximum drawdown, drawdown count, and recovery time over different periods.

### **4. Market Cap Metrics**
- Current market cap, market cap evolution, relative dominance.

### **5. Trading Volume Metrics**
- Current trading volume, mean and median volumes, volume spike counts, volume-to-market cap ratio.

### **6. Momentum Metrics**
- Price and market cap momentum over rolling windows (3, 7, 30 days).

### **7. Rarity and Inflation Metrics**
- Circulating supply/total supply ratio, token inflation, and relative inflation compared to BTC/ETH.

### **8. Risk-Reward Ratios**
- Sortino Ratio, Omega Ratio, and Upside Potential Ratio.

### **9. Correlation Metrics**
- Price and market cap correlation with BTC and ETH over rolling windows.

### **10. Anomalies and Stability Metrics**
- Single-day extreme losses, high-low price ranges.

---

## **Project Structure**

```plaintext
token_selection_project/
│
├── venv/                 # Virtual environment
├── data/                 # Stores raw and processed data
│   ├── raw/              # Raw data fetched from CoinGecko
│   ├── processed/        # Final feature dataset
│
├── src/                  # Python scripts for the project
│   ├── api.py            # API functions for data fetching
│   ├── filters.py        # Logic for token filtering
│   ├── analysis.py       # Feature calculations (volatility, momentum, etc.)
│   └── main.py           # Main script for running the project
│
├── notebooks/            # Jupyter notebooks for prototyping
├── requirements.txt      # Required Python libraries
├── tests/                # Unit tests for scripts
└── README.md             # Project description and usage instructions
```

---

## **How to Use**

### **1. Set Up the Environment**
- Create a virtual environment:
  ```bash
  python -m venv venv
  source venv/bin/activate    # For Mac/Linux
  venv\\Scripts\\activate     # For Windows
  ```

- Install dependencies:
  ```bash
  pip install -r requirements.txt
  ```

### **2. Run the Project**
- Fetch data and generate the dataset by running the main script:
  ```bash
  python src/main.py
  ```

### **3. View or Analyze the Data**
- Access the raw data and feature datasets in the `data/` folder.
- Use Jupyter notebooks in the `notebooks/` folder for additional exploration or prototyping.

---

## **Roadmap**

### **Phase 1: Dataset Creation**
- Fetch 5 years of historical data for 16,000 tokens.
- Calculate token-specific and cross-token metrics.
- Store the dataset in an efficient format (Parquet).

### **Phase 2: Quarterly Updates**
- Automate fetching daily data incrementally.
- Recalculate features quarterly for updated insights.

### **Phase 3: Advanced Features**
- Add support for derivatives data and on-chain metrics.
- Explore advanced visualizations and predictive analytics.

---

## **Contributing**

Contributions are welcome! If you’d like to add new features or improve existing ones:
1. Fork the repository.
2. Create a new branch for your changes.
3. Submit a pull request with a detailed description of your modifications.

---

## **License**

This project is licensed under the MIT License. See the `LICENSE` file for details.

---