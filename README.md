## IDS 568 – MLOps Project
[![CI](https://github.com/MengyiWang-W/ids568-mlops-project/actions/workflows/ci.yml/badge.svg)](https://github.com/MengyiWang-W/ids568-mlops-project/actions)

## Overview
This repository is created for the IDS 568 MLOps course. The purpose of this project is to set up a reproducible Python environment and verify it using continuous integration.
This milestone focuses on environment setup, dependency management, and basic CI validation.

## Dependencies
All required Python packages are listed in `requirements.txt` with pinned versions.  
The project targets Python 3.10, consistent with the GitHub Actions CI configuration.  
Dependencies can be installed using:

```bash
pip install -r requirements.txt
```
## Continuous Integration (CI)
This project uses a GitHub Actions workflow to automatically test the environment setup.
On each push or pull request to the `main` branch, the workflow installs dependencies from `requirements.txt` in a clean environment and runs a basic pytest smoke test. This ensures the project can run successfully without relying on any local configuration.

## Relation to the ML Lifecycle

Reproducible environments are essential throughout the machine learning lifecycle, from experimentation to deployment.
By pinning dependency versions, fixing the Python version, and validating the environment through automated tests, this project reduces discrepancies between local development and CI environments and supports reliable, maintainable ML workflows.