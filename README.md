# Early DVC Practice Repository

An early data-versioning practice repository created while developing the workflow that later expanded into [AI Job Market Trend Analysis](https://github.com/dnddlek8275/AI_Job_Market_Trend_Analysis).

This repository preserves the initial Git, DVC, and Google Drive remote-storage experiments. The main project extends that foundation with AI job market data, model comparison, MLflow experiment tracking, evaluation, and model registration.

## Continued Project

Current development and the complete machine learning workflow are available in:

### [AI Job Market Trend Analysis](https://github.com/dnddlek8275/AI_Job_Market_Trend_Analysis)

The main project includes:

- DVC-based dataset management
- Logistic Regression, Random Forest, XGBoost, LightGBM, and CatBoost experiments
- MLflow parameter, metric, and artifact tracking
- Model evaluation and comparison
- MLflow Model Registry integration
- Production alias assignment for the best model

## What This Repository Contains

- Initial Git and DVC practice
- A Google Drive DVC remote named `mlops_dvc_storage`
- A small Titanic dataset tracking example
- Basic files used to verify the Git workflow

## Repository Structure

```text
.
├── .dvc/
│   └── config
├── data/
│   └── titanic.csv.dvc
├── .dvcignore
├── .gitignore
├── hello.txt
└── README.md
```

## Data Versioning Example

The actual `titanic.csv` file is not stored directly in Git. Git tracks `data/titanic.csv.dvc`, which records the dataset path and content hash. DVC uses this metadata to restore the matching file from the configured Google Drive remote.

Restore the tracked data with:

```bash
dvc pull
```

Access depends on the appropriate Google Drive credentials and permissions.

## Status

This repository is retained as a record of the initial DVC learning process. It is not an independent production project and is not actively developed.

For the current implementation, see [AI Job Market Trend Analysis](https://github.com/dnddlek8275/AI_Job_Market_Trend_Analysis).
