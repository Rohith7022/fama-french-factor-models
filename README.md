# Fama-French Factor Models
## VCU – Advanced Financial Analytics (FIRE 691)

Replication of the **Fama-French 3-Factor Model** and **Carhart 4-Factor Model** using CRSP-Compustat merged institutional data spanning 1962–2025 (1.04M+ stock-month observations).

---

## Overview

This project reproduces Fama & French (1992) Tables 1–3 within tolerance and extends the framework with Carhart (1997) momentum. All analysis is conducted in Python (Google Colab) using CRSP monthly return data and Compustat fundamentals from WRDS.

---

## Factors Constructed

| Factor | Definition |
|--------|-----------|
| **Mkt-RF** | Market excess return |
| **SMB** | Small Minus Big (size factor) |
| **HML** | High Minus Low (value factor) |
| **MOM** | Winners Minus Losers (momentum factor) |

---

## Methodology

- **Universe**: NYSE, AMEX, NASDAQ common stocks (ShareType: NS, OS)
- **Size breakpoints**: NYSE median market cap (monthly)
- **Book-to-market breakpoints**: NYSE 30th/70th percentiles
- **Weighting**: Value-weighted portfolio returns
- **Date alignment**: Precise fiscal-year-end lag to eliminate look-ahead bias

---

## Key Results

- Successfully reproduced FF (1992) Tables 1–3 within tolerance
- Merged 1.04M stock-month observations across two CRSP data files (1962–1989, 1990–2025)
- Final output: `my_ff3_factors_complete.csv` (Mkt-RF, SMB, HML, RF by month)

---

## Tech Stack

`Python` · `pandas` · `numpy` · `Google Colab` · `WRDS/CRSP` · `Compustat`

---

## Files

```
├── ff3_factor_construction.ipynb   # Full factor construction notebook
├── ff4_carhart_extension.ipynb     # Momentum factor extension
├── my_ff3_factors_complete.csv     # Output: FF3 monthly factors
└── my_ff4_factors.csv              # Output: Carhart 4-factor monthly factors
```

---

*Virginia Commonwealth University · MS Business (Financial Analytics) · FIRE 691*
