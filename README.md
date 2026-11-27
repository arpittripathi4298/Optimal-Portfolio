# Portfolio Optimization & Efficient Frontier Analysis

This repository contains a financial model that applies Modern Portfolio Theory (MPT) to identify the optimal asset allocation among a diversified basket of Indian equities and commodities.

By simulating hundreds of portfolio weighting combinations, this project maps the **Efficient Frontier** to find the portfolio that offers the highest expected return for a given level of risk, ultimately maximizing the Sharpe Ratio.

## 📂 Repository Contents

* **`Optimal Portfolio.xlsx`**: The core Excel model containing raw historical price data, log return calculations, the covariance matrix, and the optimization solver used to plot the Efficient Frontier.

## 📊 Assets Analyzed

The portfolio model is built using historical data from the following assets:

* **HUL** (Hindustan Unilever Limited)
* **TCS** (Tata Consultancy Services)
* **HDFC Bank**
* **Bharti Airtel**
* **Gold** (Commodity Hedge)

## 📈 Methodology

1. **Data Processing:** Calculated daily log returns from historical asset prices.
2. **Risk & Return Metrics:** Computed the annualized expected returns and the standard deviation (risk) for each asset.
3. **Covariance Matrix:** Built a variance-covariance matrix to measure how these assets move relative to one another.
4. **Optimization:** Used a non-linear solver to maximize the **Sharpe Ratio** formula:

   Sharpe Ratio = {R_p - R_f}/{$\sigma_p$}

   *(Where* $R_p$ *is portfolio return,* $R_f$ *is the risk-free rate, and* $\sigma_p$ *is portfolio standard deviation).*

## 🚀 Key Findings: The Tangency Portfolio

Assuming a risk-free rate of **5.93%**, the optimization engine identified the maximum Sharpe Ratio portfolio with the following characteristics based on the data in `Optimal Portfolio_2.xlsx`:

* **Expected Annual Return:** 26.33%
* **Portfolio Risk (Standard Deviation):** 19.78%
* **Maximum Sharpe Ratio:** 1.03

### Optimal Asset Allocation:

To achieve this optimal risk-adjusted return, the solver determined the following weight distribution, favoring out-performers and zeroing out under-performers:

* **Bharti Airtel:** 50%
* **Gold:** 50%
* **HUL:** 0%
* **TCS:** 0%
* **HDFC Bank:** 0%
