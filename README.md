# DuPont × Brinson (Brazil) — Where Did Alpha Come From?

This project combines **equity portfolio attribution (Brinson–Fachler)** with an **Extended DuPont decomposition** to answer a simple question:

> **Where did active return come from — and what kind of ROE did we buy?**  
> (Operating performance vs. leverage-driven ROE)

## What’s inside
- **Attribution (performance lens):** sector **Allocation** vs. **Selection** effects vs. **Ibovespa** (cumulative, in **bps**).
- **Fundamentals (quality lens):** Extended **DuPont** snapshot (Profit Margin × Asset Turnover × Equity Multiplier).
- **Bridge view:** links sector/ticker attribution with DuPont drivers to interpret *how* winners/losers generated ROE.

## Universe and benchmark
- **Universe:** 12 Brazilian equities across 6 sectors  
  Financials (ITUB4, BBDC4) • Commodities (VALE3, PETR4) • Utilities (ELET3, SBSP3) •  
  Consumer (ABEV3, LREN3) • Industrials/Logistics (WEGE3, RAIL3) • Real Estate (CYRE3, ALOS3)
- **Benchmark:** Ibovespa (`^BVSP`)
- **Frequency:** monthly

## Repository structure
- `notebooks/data/01_project_overview.ipynb` — main notebook (end-to-end analysis)
- `notebooks/data/universe_cvm_map.csv` — ticker ↔ CVM identifiers mapping
- `notebooks/data/outputs/` — generated artifacts  
  - `figures/` — charts (PNG)
  - `tables/` — tables (Parquet/CSV, when applicable)

## Key outputs (figures)
Some charts you’ll find in the outputs folder:
- Sector Allocation vs. Selection (cumulative, bps)
- Active Return Waterfall (sector contributions, bps)
- Bridge view: ticker-level attribution + DuPont snapshot
- Attribution vs. Fundamentals scatter views (sector-level)

## How to run
1. Create an environment (example):
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   pip install -r requirements.txt