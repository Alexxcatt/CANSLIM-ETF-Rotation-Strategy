# Data Overview

This directory contains **sample datasets** used in the CANSLIM-based
industry / ETF rotation research.

The files provided here are **truncated samples (first 20 rows only)**,
intended for demonstrating data structure and code execution flow.

---

## Files

### 1. `canslim_factors.csv`

Panel data of factor values at the industry level.

**Columns**
- `TRADE_DT` : Trading date (YYYYMMDD)
- `INDEX_CODE` : Industry index code (Wind)
- `CROWD` : Industry crowding indicator
- `ANALYST_REV` : Analyst forecast revision
- `ANALYST_UP` : Analyst upgrade ratio
- `NP_SUE` : Earnings surprise (standardized)
- `NP_DELTA_R` : Profit growth acceleration
- `NP_PROFIT` : Profitability metric
- `SMART` : Smart money / flow-related factor
- `PM` : Price momentum factor
- `VA` : Valuation-related factor
- `I_SELLSIDE` : Sell-side sentiment indicator
- `I_SELLSIDE_C` : Change in sell-side sentiment
- `I_UNDER_W` : Underweight indicator
- `M_MACROPB` : Macro valuation (PB-based)

Each row corresponds to one industry on one trading date.

---

### 2. `canslim_ret.csv`

Daily return data for industry indices.

**Columns**
- `TRADE_DT` : Trading date (YYYYMMDD)
- `INDEX_CODE` : Industry index code (Wind)
- `RET` : Daily return

---

## Notes

- Only the **first 20 rows** of each dataset are included.
- Full datasets are **not published** to avoid redistribution of research assets
  derived from Wind-based data.
- These sample files are **not suitable for performance evaluation or strategy replication**.

To reproduce full results, users should generate complete datasets locally
following the same schema.
