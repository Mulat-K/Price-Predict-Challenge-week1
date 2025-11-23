````markdown
# Predicting Price Moves with News Sentiment 📈📰  

![Python Version](https://img.shields.io/badge/Python-3.8%2B-blue)
![Project Status](https://img.shields.io/badge/Status-Interim%20Submission-orange)
![TA-Lib](https://img.shields.io/badge/Library-TA--Lib-green)
![NLTK](https://img.shields.io/badge/Library-NLTK-yellow)

---

## 1. Project Overview

Nova Financial Solutions aims to enhance its predictive analytics capabilities to improve financial forecasting accuracy.  

This project sits at the intersection of **Data Engineering**, **Financial Analytics**, and **Machine Learning**. Using the **Financial News and Stock Price Integration Dataset (FNSPID)**, this repository contains the code and analysis to:

- Quantify the tone of financial news using **Sentiment Analysis**
- Analyze stock performance using **Technical Indicators** (RSI, MACD, SMA)
- Establish statistical correlations between news sentiment and stock price movements

---

## 2. Business Objective

The primary goal is to derive **actionable investment insights** by answering:

> **Does the sentiment of financial news headlines accurately predict daily stock price movements?**

Key focus areas:

- **Sentiment Analysis**: Quantifying "positive", "negative", or "neutral" tones in headlines  
- **Correlation Analysis**: Measuring the relationship between sentiment scores and daily stock returns  
- **Strategy Design**: Suggesting how news data can be leveraged for trading strategies  

---

## 3. Folder Structure

The project follows a production-grade data science directory structure:

```bash
├── .github/
│   └── workflows/          # CI/CD configurations (GitHub Actions)
├── .vscode/                # VSCode settings
├── notebooks/              # Jupyter Notebooks for analysis
│   ├── 1_eda_news.ipynb    # Task 1: Exploratory Data Analysis
│   ├── 2_technical.ipynb   # Task 2: Quantitative Analysis (TA-Lib)
│   └── 3_correlation.ipynb # Task 3: Sentiment & Correlation
├── scripts/                # Utility scripts for data processing
├── src/                    # Source code for modular functions
├── tests/                  # Unit tests
├── .gitignore              # Git ignore rules
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies
````

---

## 4. Installation & Setup

### Prerequisites

* **Python 3.8+**
* **Git**
* **TA-Lib** (Technical Analysis Library)

  > Note: TA-Lib often requires a binary installation before installing the Python wrapper.

### Step-by-Step Guide

#### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd nova-financial-analysis
```

#### 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

#### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

If **TA-Lib** fails to install via `pip`, please refer to the official TA-Lib installation guide for your operating system.

---

## 5. Methodology & Workflow

### Task 1: Exploratory Data Analysis (EDA)

**Objective**: Understand the FNSPID dataset structure and quality.

**Key Activities:**

* Analyzed distribution of headline lengths
* Identified top publishers contributing to the dataset
* Visualized publication frequency over time to detect market event spikes

**Tools**: `pandas`, `seaborn`, `matplotlib`

---

### Task 2: Quantitative Analysis (Technical Indicators)

**Objective**: Apply technical analysis to stock data (using **YFinance** as a proxy for market data).

**Indicators Calculated:**

* **SMA (Simple Moving Average)** – Identify trend direction
* **RSI (Relative Strength Index)** – Detect overbought/oversold conditions
* **MACD (Moving Average Convergence Divergence)** – Identify momentum changes

**Tools**: `TA-Lib`, `yfinance`

---

### Task 3: Sentiment & Correlation Analysis

**Objective**: Link qualitative news data to quantitative price action.

**Process:**

1. **NLP**: Used **TextBlob** to generate polarity scores (−1 to +1) for headlines
2. **Aggregation**: Averaged sentiment scores daily per stock
3. **Returns**: Calculated daily percentage change in closing price
4. **Statistics**: Computed **Pearson Correlation Coefficient** between sentiment and returns

---

## 6. Key Findings (Interim)

* **Publisher Dominance**:
  A small number of publishers account for the majority of financial news, suggesting potential bias in news flow.

* **Sentiment Distribution**:
  Financial headlines tend to be **neutral-to-positive**. Extreme negative sentiment is rarer but often correlates with **higher volatility**.

* **Correlation**:
  Initial analysis suggests a **weak positive correlation** between daily sentiment and same-day returns.
  This implies that while news affects prices, it is **not the sole predictor**, and **lag effects** (e.g., news impacting price the next day) should be investigated further.

---

## 7. Future Work

Planned enhancements:

* **Advanced NLP**: Implement **BERT** or **FinBERT** for more accurate financial sentiment scoring compared to TextBlob
* **Time-Lag Analysis**: Analyze whether news sentiment predicts price movements **1, 2, or more days later**
* **Intraday Analysis**: Use minute-level data to capture immediate market reactions to headlines

---

## 8. Contributors

* **Your Name** – Data Analyst @ Nova Financial Solutions

> Replace `Your Name` with your actual name or GitHub handle.

---

## 9. License

This project is for **educational purposes** as part of the **10 Academy Challenge**.
Please refer to the LICENSE file if added in the future.

---

```
```
