# IDS 568 – MLOps Project

## Overview
This repository is created for the IDS 568 MLOps course.  
The purpose of this project is to set up a reproducible Python environment and verify it using continuous integration.
This milestone focuses on environment setup, dependency management, and basic CI validation.

## Dependencies
All required Python packages are listed in `requirements.txt` with pinned versions.
Using pinned versions ensures that the same environment can be recreated on different machines, including local development and GitHub Actions CI.
Dependencies can be installed with:

```bash
pip install -r requirements.txt
```
## Continuous Integration (CI)
This project uses a GitHub Actions workflow to automatically test the environment setup.

On each push or pull request to the `main` branch, the workflow installs dependencies from `requirements.txt` in a clean environment and runs a basic pytest smoke test. This ensures the project can run successfully without relying on any local configuration.

## Relation to the ML Lifecycle
Reproducible environments help ensure that experiments and results can be consistently reproduced across development and testing stages. This setup provides a starting point for later stages such as model training and deployment.