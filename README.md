# 📊 VaR-Projects

A collection of **Value at Risk (VaR)** and **Expected Shortfall (ES)** demonstrations implemented as Jupyter notebooks in Python.  
The repository implements three standard VaR methodologies applied to an equally-weighted multi-asset portfolio:

- Historical VaR (non-parametric)
- Parametric (Variance–Covariance) VaR
- Monte Carlo VaR

These notebooks are intended for **learning, experimentation, and FRM preparation**.

---

## 📁 Contents

- `Historical_VaR.ipynb` — historical simulation VaR and ES (visualisations included)
- `Parametric_VaR.ipynb` — variance-covariance (parametric) VaR and ES; comparison with historical results
- `MonteCarlo_VaR.ipynb` — Monte Carlo simulation of portfolio P&L, Monte Carlo VaR and ES (visualisations included)

---

## 🧠 Summary of Each Notebook

### 🔹 Historical_VaR.ipynb
- Downloads adjusted close prices for sample tickers (default: `['SPY','BND','GLD','QQQ']`) using **yfinance**.
- Computes daily log returns and constructs an equally-weighted portfolio.
- Calculates X-day rolling portfolio returns.
- Estimates **Historical VaR** (empirical quantile) and **Expected Shortfall** (average losses beyond VaR).
- Visualises return distributions with VaR and ES markers and tail shading.
- *Illustrative output (varies by data window):*  
  - 5-day VaR (95%): ~2,209  
  - 5-day ES (95%): ~3,534  

---

### 🔹 Parametric_VaR.ipynb
- Computes portfolio mean returns and covariance matrix (annualised).
- Estimates **Parametric VaR** assuming normally distributed returns.
- Computes **Parametric ES** using the analytical formula under normality.
- Compares parametric VaR/ES with historical VaR/ES across confidence levels (90%, 95%, 99%).
- Includes histograms and visual comparisons.
- *Illustrative output:*  
  - 95% Parametric VaR: ~2,804 
  - 95% Historical VaR: ~2,217

---

### 🔹 MonteCarlo_VaR.ipynb
- Uses historical return estimates to parameterise a Monte Carlo simulation.
- Simulates portfolio P&L scenarios for an X-day horizon.
- Computes **Monte Carlo VaR** and **Monte Carlo ES** from the simulated loss distribution.
- Visualises simulated P&L with VaR and ES markers.
- *Illustrative output:*  
  - Monte Carlo VaR (95%): ~2,372  
  - Monte Carlo ES (95%): ~3,043  

---

## 🛠 Requirements / Dependencies

Minimum Python packages used:

- Python 3.8+
- numpy
- pandas
- matplotlib
- scipy
- yfinance
- jupyter / jupyterlab

---

## 🎯 Why This Project

VaR and Expected Shortfall are core tools in **financial risk management**.  
This project demonstrates:
- Multiple VaR methodologies
- Portfolio-level risk estimation
- Distributional assumptions vs empirical risk
- Clear visualisation and interpretation of tail risk

Built as part of **FRM preparation and quantitative finance practice**.
