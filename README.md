# COMM 476 — Black-Litterman + Fama-French Factor Portfolio

## Overview
Implemented a Black-Litterman optimizer with Fama-French (MKT/SMB/HML) factor views to enhance a quality equity universe portfolio. The analysis includes portfolio construction, optimization, backtesting vs QUAL, and risk metrics.

## Repository Contents
- `black_litterman_fama_french.ipynb` — main analysis notebook (model construction, optimization, backtest, and risk metrics)
- `QUAL-holdings.csv` — QUAL holdings input file used by the notebook (required to reproduce the universe/benchmark mapping)

## Requirements
- Python (Jupyter Notebook)
- **Wharton Research Data Services (WRDS) access** (login required) to pull CRSP/Compustat data used in the analysis
- Standard Python packages (e.g., pandas, numpy, matplotlib; additional packages noted in the notebook)

## How to Run
1. Clone or download this repository.
2. Open `black_litterman_fama_french.ipynb` in Jupyter.
3. Ensure you have WRDS credentials configured (the notebook will prompt/require access).
4. Update the local file path for the QUAL holdings CSV in the notebook.

### Update the QUAL CSV path
In the notebook, the file is currently read using:
python
`qual_holdings = pd.read_csv(os.path.expanduser('~/Downloads/476 Data/QUAL-holdings.csv'))`
Change the path to wherever you saved QUAL-holdings.csv on your machine, e.g.:
`qual_holdings = pd.read_csv('/path/to/your/folder/QUAL-holdings.csv')`
