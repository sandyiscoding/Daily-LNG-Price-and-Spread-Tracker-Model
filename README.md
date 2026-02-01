# Daily LNG Price and Spread Tracker Model

## 📊 Overview
A Python-based tool for tracking daily LNG (Liquefied Natural Gas) benchmark prices and calculating arbitrage opportunities between major global markets. This tool helps energy traders and analysts monitor price spreads and identify profitable trading opportunities in real-time.

## 🌍 Key Features

### 🔍 **Market Monitoring**
- **Three Major Benchmarks**:
  - **Henry Hub (HH)**: US benchmark ($/MMBtu)
  - **Title Transfer Facility (TTF)**: European benchmark ($/MMBtu, converted from €/MWh)
  - **Japan Korea Marker (JKM)**: Asian spot LNG benchmark ($/MMBtu)

### 📈 **Core Analytics**
- **Spread Calculations**:
  - JKM-TTF Spread (Asia vs Europe premium)
  - TTF-HH Spread (Europe vs US premium)
  - JKM-HH Spread (Asia vs US premium)
- **10-day average spreads**
- **Daily price trend analysis**

### 💰 **Arbitrage Analysis**
- **US Export Profitability Calculator**:
  - **To Europe**: HH → TTF margin analysis
  - **To Asia**: HH → JKM margin analysis
- **Industry-standard cost assumptions**:
  - Liquefaction fee: $2.25/MMBtu
  - Freight US→Europe: $1.80/MMBtu
  - Freight US→Asia: $3.20/MMBtu

### 📊 **Visual Dashboard**
Four-panel visualization showing:
1. **Price Trends** - Historical price movements
2. **Spread Trends** - Spread evolution over time
3. **Latest Prices** - Current market snapshot
4. **Spread Distribution** - Profit/loss visualization


## 📁 Output Files

### Generated Files:
- **`lng_daily_tracker.csv`**: Complete dataset with prices and spreads
- **`lng_price_tracker.png`**: Visual dashboard (4-panel chart)

## 📊 Sample Output

### Terminal Output:
```
==================================================
DAILY PRICE TRACKER - LNG BENCHMARKS
==================================================

Data from 2024-03-04 to 2024-03-15

Latest Spreads (as of 2024-03-15):
JKM-TTF Spread: $0.70/MMBtu
TTF-HH Spread:  $8.53/MMBtu
JKM-HH Spread:  $9.23/MMBtu
```

### Arbitrage Analysis:
```
Breakeven Analysis:
  US→Europe DES cost: $5.82/MMBtu
  Current TTF price:  $10.30/MMBtu
  Margin: $4.48/MMBtu → ✅ PROFITABLE

  US→Asia DES cost:   $7.22/MMBtu
  Current JKM price:  $11.00/MMBtu
  Margin: $3.78/MMBtu → ✅ PROFITABLE
```

## 🎯 Use Cases

### For Energy Traders:
- **Daily Market Monitoring**: Track global LNG price movements
- **Arbitrage Identification**: Spot profitable shipping opportunities
- **Portfolio Optimization**: Make data-driven trading decisions

### For Analysts:
- **Market Research**: Study price relationships between regions
- **Report Generation**: Create daily/weekly market reports
- **Trend Analysis**: Identify emerging market patterns

### For Portfolio Managers:
- **Risk Assessment**: Monitor spread volatility
- **Strategy Development**: Test different trading scenarios
- **Performance Tracking**: Compare actual vs. expected spreads


## 📈 Data Sources

| Benchmark | Source | Frequency |
|-----------|---------|-----------|
| Henry Hub | EIA Website | Daily |
| TTF | tradingeconomics.com | Daily |
| JKM | LNG market reports | Daily |

**Note**: TTF prices require conversion from €/MWh to $/MMBtu using formula: `€/MWh × 0.293 × EURUSD_rate`

**Disclaimer**: This tool is for educational and analytical purposes only. Trading decisions should be made based on comprehensive market analysis and professional advice. The creators are not responsible for any trading losses incurred using this tool.
