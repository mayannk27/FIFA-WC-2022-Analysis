# Project structure guide

- `notebooks/` — exploratory analysis and end-to-end research workflow.
- `data/raw/` — original CSV inputs; keep these immutable.
- `scripts/` — standalone utilities. The FIFA Index crawler is retained as a legacy reference and may need maintenance.
- `reports/` — original project write-up and presentation.
- `assets/images/` — images used by the original project.
- `docs/` — data dictionary, model notes, and repository guidance.

When the project grows, consider adding `src/fifa_wc/` for reusable Python modules, `tests/` for automated checks, and `data/processed/` for generated datasets. Avoid moving notebook logic into modules until the code has been refactored and tested.
