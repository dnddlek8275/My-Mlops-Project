# My MLOps Project

A minimal practice repository for learning Git basics and DVC-based data versioning.

The project tracks a small Titanic dataset with DVC and configures Google Drive as the default DVC remote. It is an initial data-versioning exercise rather than a complete model-training or deployment project.

## What Is Included

- A Git repository with a basic commit history
- DVC project configuration
- A Google Drive DVC remote named `mlops_dvc_storage`
- A DVC metadata file for `data/titanic.csv`
- A small text file used for Git practice

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

## Data Versioning Flow

The actual `titanic.csv` file is not stored directly in Git. Git tracks `data/titanic.csv.dvc`, which records the dataset path, size, and content hash. DVC uses that metadata to restore the matching file from the configured remote.

Restore tracked data with:

```bash
dvc pull
```

After changing the dataset, update its DVC metadata with:

```bash
dvc add data/titanic.csv
```

Then commit the updated `.dvc` metadata file through Git.

## DVC Remote

The repository configures a Google Drive remote as the default DVC storage. Access to the remote depends on the appropriate Google Drive credentials and permissions.

## Current Scope

This repository does not currently include:

- Data preprocessing code
- Model training or evaluation code
- MLflow experiment tracking
- An inference API
- CI/CD or deployment configuration

Those components should only be added if the repository grows beyond its current DVC learning purpose.
