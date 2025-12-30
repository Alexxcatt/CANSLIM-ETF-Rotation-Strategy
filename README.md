# CANSLIM ETF Rotation Strategy

This repository implements a **CANSLIM-based ETF rotation strategy** with systematic backtesting and machine learning–assisted optimisation.  
The project is designed as a **research-oriented and reproducible pipeline**, focusing on factor construction, portfolio formation, and robustness analysis.

---

## Project Overview

The strategy combines **CANSLIM-style fundamental, analyst sentiment, and market indicators** with **industry-level ETF rotation**, aiming to capture structural alpha across different market regimes.

Key characteristics:

- Industry-level rotation using ETF proxies  
- Multi-factor framework inspired by CANSLIM philosophy  
- Cross-sectional ranking and periodic rebalancing  
- Optional XGBoost-based ranking optimisation  
- Clear separation between data, research notebooks, and documentation  

Only **sample datasets** are included for illustration and reproducibility.  
No proprietary or raw Wind data is published.

---

## Repository Structure

```text
CANSLIM-ETF-Rotation-Strategy/
├── data/
│   ├── canslim_factors_sample.csv    # Sample factor dataset (illustrative)
│   ├── canslim_ret_sample.csv        # Sample ETF return data
│   └── data_readme.md                # Data description and field definitions
├── notebook/
│   ├── 01_data.ipynb                 # Data preparation & preprocessing
│   ├── 02_strategy.ipynb             # Strategy construction & backtesting
│   └── 03_xgboost_optimisation.ipynb # XGBoost-based ranking optimisation
├── docs/
│   └── notes.docx                    # Research notes and methodology
└── README.md
```

---

## Strategy Logic

### 1. Factor Construction
- CANSLIM-inspired indicators such as:
  - Earnings surprise  
  - Analyst recommendation changes  
  - Profitability and growth metrics  
  - Industry crowding indicators  
- Factors are aggregated at the industry level.

### 2. Cross-Sectional Ranking
- Industries are ranked based on composite factor scores.
- Higher-ranked industries receive higher portfolio weights.

### 3. Portfolio Formation
- Periodic rebalancing (e.g. monthly or quarterly).
- Equal-weighted or score-weighted allocation schemes.

### 4. Machine Learning Optimisation (Optional)
- XGBoost ranking model to capture non-linear factor interactions.
- Used as a **scoring and ranking layer**, not direct return prediction.

---

## Backtesting Framework

- Vectorised backtesting implemented with pandas
- Net asset value (NAV), drawdown, and performance metrics
- Benchmark comparison
- Modular design for easy extension

A dedicated **stress testing module** (subsample analysis, crisis periods, and parameter sensitivity) is planned to further assess robustness.

---

## Data Disclaimer

- All datasets in this repository are **sample or derived data**
- Original data sources (e.g. Wind) are **not redistributed**
- Sample files are truncated and provided **for demonstration only**

This repository is intended for **research and educational purposes**.

---

## Future Work

- Stress testing across market regimes  
- Transaction cost modelling  
- Alternative weighting and risk control schemes  
- Extended machine learning models  
- Automated experiment tracking  

---

## Notes

This project does **not constitute investment advice**.  
All results are for academic and research discussion only.
