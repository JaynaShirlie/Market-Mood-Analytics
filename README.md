# 🧠 MarketMoodTrader

**Analyzing the Relationship Between Bitcoin Market Sentiment and Hyperliquid Trader Performance**

---

## 📖 Overview

MarketMoodTrader is a data analysis project that explores how **Bitcoin market sentiment** — measured by the [Crypto Fear & Greed Index](https://alternative.me/crypto/fear-and-greed-index/) — correlates with **real trading performance** on the [Hyperliquid](https://hyperliquid.xyz/) decentralized exchange.

The project merges ~211K+ on-chain trade records with daily sentiment data spanning from 2018–2025 to answer questions like:

- 📈 Do traders perform better during *Extreme Fear* or *Extreme Greed*?
- 🏆 Which sentiment regime yields the highest win rate?
- 💰 How does trade volume and PnL vary across sentiment classifications?
- 🔄 Are contrarian strategies (buying during fear, selling during greed) profitable?
- 📊 How does sentiment momentum affect trading outcomes?

## 📊 Visualizations

The notebook generates **14 detailed charts**, including:

| # | Chart | Description |
|---|-------|-------------|
| 1 | Sentiment Distribution | Count of unique trading days per sentiment class |
| 2 | Fear/Greed Timeline | Sentiment index value over time with colored regions |
| 3 | Volume per Sentiment | Total trading volume (USD) by sentiment class |
| 4 | Trades per Sentiment | Number of trades executed per sentiment class |
| 5 | Avg PnL per Sentiment | Average closed PnL by sentiment classification |
| 6 | Win Rate per Sentiment | Win percentage across sentiment regimes |
| 7 | Avg Fee per Sentiment | Average trading fees by sentiment class |
| 8 | Buy/Sell Ratio | Buy vs sell distribution per sentiment class |
| 9 | Contrarian Signal | Performance of contrarian strategies |
| 10 | Sentiment Momentum | How sentiment shifts affect trading outcomes |
| 11 | Coin-Sentiment Heatmap | Per-coin performance across sentiment regimes |
| 12 | Shift vs Stable | Trading performance during sentiment transitions |
| 13 | Tier Sentiment Distribution | Trade size tiers across sentiment classes |
| 14 | Tier Size Heatmap | Trade size distribution heatmap by sentiment |

> All charts are automatically generated and saved to the `charts/` directory when running the notebook.

## 🗂️ Project Structure

```
MarketMoodTrader/
├── MarketMoodTrader.ipynb    # Main analysis notebook (fully executable)
├── fear_greed_index.csv      # Daily Crypto Fear & Greed Index data (2018–2025)
├── historical_data.csv       # Hyperliquid trade records (~211K rows, ~47MB)
├── charts/                   # Generated visualization outputs (14 PNGs)
├── requirements.txt          # Python dependencies
├── .gitignore                # Git ignore rules
└── README.md                 # This file
```

## 🚀 Getting Started

### Prerequisites

- Python 3.9+
- Jupyter Notebook or JupyterLab

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/<your-username>/MarketMoodTrader.git
   cd MarketMoodTrader
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch the notebook:**
   ```bash
   jupyter notebook MarketMoodTrader.ipynb
   ```

4. **Run all cells** to reproduce the analysis and generate all 14 charts.

## 📁 Data Sources

| File | Description | Size |
|------|-------------|------|
| `fear_greed_index.csv` | Daily Bitcoin Fear & Greed Index with timestamp, value (0–100), classification, and date | ~90 KB |
| `historical_data.csv` | Hyperliquid DEX trade records including execution price, size, side, PnL, fees, and more | ~47 MB |

### Sentiment Classifications

| Range | Classification |
|-------|---------------|
| 0–24 | Extreme Fear |
| 25–49 | Fear |
| 50–54 | Neutral |
| 55–74 | Greed |
| 75–100 | Extreme Greed |

## 🛠️ Tech Stack

- **Python** — Core language
- **pandas** — Data manipulation and merging
- **NumPy** — Numerical computations
- **Matplotlib** — Chart rendering
- **Seaborn** — Statistical visualizations
- **Jupyter Notebook** — Interactive analysis environment

## 📝 Key Findings

The analysis reveals several interesting patterns in how market sentiment affects trader behavior and performance on Hyperliquid:

- Trading volume and activity levels vary significantly across sentiment regimes
- Win rates and average PnL show distinct patterns during extreme sentiment periods
- Contrarian signals provide actionable insights for timing trades
- Sentiment momentum (shifts between classifications) impacts short-term trading outcomes

> For detailed findings, run the notebook and explore the inline commentary with each visualization.

## 📄 License

This project is for educational and research purposes. The trading data is anonymized on-chain data from public blockchain records.