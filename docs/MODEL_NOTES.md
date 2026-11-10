# Model notes

## Original approach

1. Load international match results and FIFA player datasets.
2. Select the World Cup participant countries and top-rated players by nationality.
3. Aggregate player ratings and mentality attributes by country and year.
4. Join match records with country ratings and national player aggregates.
5. Impute missing values and prepare training features.
6. Train KNN, SVC, and Random Forest classifiers, tuning model parameters.
7. Combine selected estimators in a Voting Classifier.
8. Add random variation to team features and repeat head-to-head predictions to estimate simulated win frequencies.
9. Use head-to-head simulations to explore group and knockout-stage outcomes.

## Reproducibility checklist

Before treating a result as reproducible, record:

- Python and package versions
- Exact source dataset URLs, versions, and download dates
- Random seeds
- Train/test split strategy
- Feature columns and preprocessing fitted only on training data
- Hyperparameter search space and cross-validation strategy
- Evaluation metrics, including class-wise precision/recall and probability calibration

## Cautions

The original notebook is exploratory research, not a production prediction service. It includes historical assumptions and should be reviewed before drawing conclusions. In particular, assess possible temporal leakage, class imbalance, draw handling, neutral venues, and whether the random-noise scale is empirically justified.
