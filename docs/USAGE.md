# Usage notes

## Recommended workflow

1. Start with `notebooks/C0_common_backtesting_engine.ipynb`.
2. Review the specific case-study notebook you want to inspect.
3. Generated data, plots and tables should be written under `results/`.
4. Keep private datasets outside the repository.

## Local execution

The `appendix_code/clean_python/` files are cleaned exports where Colab-specific commands have been commented out. They are useful for inspection and gradual refactoring, but the notebooks are the most faithful representation of the appendix workflow.

## Colab execution

The original exports in `appendix_code/original_colab_exports/` preserve Colab-specific commands such as package installation and Google Drive mounting.
