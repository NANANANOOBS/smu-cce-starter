 # Cloud Computing for Economics

This repository is a starter project for collecting and exploring financial data with Python. The lessons introduce GitHub Codespaces, Jupyter notebooks, Streamlit, Git, and cloud deployment concepts.

## Learning outcomes

By the end of the course, you will be able to:

1. Build a small financial-data application with a front end and back end.
2. Integrate public data sources and APIs into an analytics workflow.
3. Explain the basic cloud architecture needed to share an application securely.
4. Present a reproducible analytics project in GitHub.

## Project structure

```text
.
├── README.md
├── requirements.txt
├── lessons/                  # Step-by-step course instructions
├── notebooks/                # Exploratory financial-data analyses
├── data/                     # Local or downloaded data files (not committed)
├── models/                   # Saved models and model artifacts
├── src/                      # Reusable Python modules for application code
├── output/                   # Generated tables, charts, and reports
└── .gitignore                # Local files and generated artifacts excluded from Git
```

## Installation

The recommended environment is GitHub Codespaces, although the same commands work in a local Python 3.10+ environment.

```bash
git clone https://github.com/<your-username>/smu-cce-starter.git
cd smu-cce-starter
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

On Windows PowerShell, activate the environment with:

```powershell
.venv\Scripts\Activate.ps1
```

## Code walkthrough

The notebooks are intentionally small and build from one data source:

1. `stock_price_ratings.ipynb` retrieves a current price and recent analyst recommendations for a ticker.
2. `sec_filings_analysis.ipynb` retrieves the latest income statement, balance sheet, and cash-flow data.
3. `news.ipynb` retrieves and prints recent news headlines and descriptions.

Open a notebook in VS Code or Jupyter and run its cells from top to bottom. Replace the example ticker with another supported Yahoo Finance ticker when experimenting. Network access is required because the examples request live data from Yahoo Finance, and the returned fields may change over time.

The `src/`, `data/`, `models/`, and `output/` directories are extension points for later lessons. Keep reusable functions in `src/`, raw or downloaded inputs in `data/`, trained artifacts in `models/`, and generated results in `output/` rather than mixing them into notebooks.

## Lessons

- [Lesson 1](lessons/lesson1.md): create a GitHub account and start a Codespace.
- [Lesson 2](lessons/lesson2.md): fork, clone, install dependencies, and run a notebook.

## Notes on generated files

Downloaded data, model artifacts, notebook checkpoints, virtual environments, and generated output are ignored by Git. Add a deliberately chosen, shareable sample to the repository only when it is useful for reproducing an example.