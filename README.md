# Robust Investment Strategy Validation

Public code repository for the Bachelor's Thesis:

**Evaluación robusta de estrategias de inversión: backtesting, sobreajuste y validación estadística**  
Albert Cabré Carrera · Physics, UNED · 2025/2026

This repository contains the **public appendix code** used to support a robust empirical evaluation of investment strategies. The project studies how historical performance should be interpreted together with risk, costs, temporal stability, overfitting control and factor exposure.

> This is a public/sanitized repository. Proprietary components and private datasets are not included.

## What this project covers

The code is organized into six blocks:

| Block | Topic |
|---|---|
| `C0` | Common data engine, S&P 100 universe reconstruction, backtesting and metrics |
| `C1` | Classical technical indicators and cost-sensitive backtests |
| `C2` | Language models and synthetic signal detection |
| `C3` | Genetic algorithms, ex-post selection and White's Reality Check |
| `C4` | Markowitz portfolio optimization and factor validation |
| `C5` | Public/censored evaluation of a proprietary strategy using observed returns only |

## Repository structure

```text
.
├── appendix_code/
│   ├── original_colab_exports/   # direct public exports from the appendix/Colab
│   └── clean_python/             # portable Python versions with Colab commands commented
├── notebooks/                    # GitHub-renderable notebooks for each block
├── docs/                         # thesis summary, module map and usage notes
├── data/                         # no private data included
├── results/                      # generated outputs should go here
├── requirements.txt
├── LICENSE
└── CITATION.cff
```

## Quick start

Clone the repository:

```bash
git clone https://github.com/albertcabre6626/robust-investment-validation.git
cd robust-investment-validation
```

Create an environment and install dependencies:

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

The notebooks in `notebooks/` are the easiest way to inspect and reproduce the workflow. Some blocks were originally designed for Google Colab and may require path adjustments before running locally.

## Important reproducibility notes

- Market data is downloaded with `yfinance`, so results can vary slightly depending on data-provider updates.
- The S&P 100 historical membership reconstruction relies on historical Wikipedia revisions.
- The public `data/C5_public_returns.csv` file is included as input for the censored/public C5 workflow.
- No private datasets or proprietary model logic are included.
- The `C5` block is intentionally public/censored and does **not** reveal proprietary model logic.
- This repository is for academic and research purposes only. It is not investment advice.

## Thesis abstract

The thesis approaches the evaluation of investment strategies as a statistical-inference problem on noisy financial time series. It combines conventional performance/risk metrics with transaction-cost analysis, temporal bootstrap, studentized White's Reality Check and Fama-French factor regressions with momentum.

The goal is not to predict markets, but to distinguish apparent historical profitability from stronger evidence of robustness after accounting for costs, overfitting, benchmark comparison and factor exposure.

## Suggested GitHub description

`Robust validation framework for investment strategies: backtesting, bootstrap, White's Reality Check, factor regression and portfolio optimization.`

## License

The public code in this repository is released under the MIT License. See `LICENSE`.
