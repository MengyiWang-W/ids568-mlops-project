## IDS 568 – MLOps Project
[![CI](https://github.com/MengyiWang-W/ids568-mlops-project/actions/workflows/ci.yml/badge.svg)](https://github.com/MengyiWang-W/ids568-mlops-project/actions)

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
Reproducible environments are essential throughout the machine learning lifecycle, from experimentation to deployment. During development and testing, consistent environments allow experiments to be reliably reproduced and validated without being affected by differences in system configuration or package versions.

In this project, reproducibility is achieved by pinning dependency versions, specifying a fixed Python version in the CI workflow, and validating the environment through automated tests. This approach reduces discrepancies between local development and automated testing environments.

Establishing reproducibility early in the pipeline helps reduce deployment risk and provides a stable foundation for later ML lifecycle stages such as model training, evaluation, and deployment. By ensuring environment consistency from the start, this project supports more reliable and maintainable ML workflows as they transition from experimentation to real-world use.