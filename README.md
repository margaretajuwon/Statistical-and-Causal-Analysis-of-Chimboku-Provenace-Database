# Statistical and causal-style analysis of the Chimbuko provenance database

Exploratory analysis of provenance records from the Chimbuko performance-anomaly framework (fields such as
`entry`, `exit`, `io_step_tstart`, `io_step_tend`, `is_gpu_event`, `outlier_score`, `outlier_severity`, `rid`).

## Notebooks
- `Binary Logistic Regression-Chimbuko Provenance Database.ipynb`: data cleaning, tree-based feature
  importance, hold-out split, and binary logistic regression with a sweep of the regularization parameter C.
  Best run reached about 62.9% test accuracy (log loss about 0.567); a poorly regularized run reached only about 52.9%,
  which the notebook uses to show why tuning matters. Treat the model as exploratory, not production-ready.
- `K-prototype-entire dataset.ipynb`: k-prototypes clustering for mixed numeric and categorical fields, with pair plots.
- `Theil's U Correlation.ipynb`: association between categorical variables using Theil's U (dython), used to
  ask whether function hashes, thread ids and outlier severity are related.

## Tools
Python, pandas, NumPy, scikit-learn, kmodes, dython, seaborn, matplotlib.

## Notes
This is exploratory analysis. Associations found here are not proof of causation.
