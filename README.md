# ml-pipeline-assignment4

![CI Status](https://github.com/HAMZA2FEKRY/ml-pipeline-assignment4/actions/workflows/ml-pipeline.yml/badge.svg)

## Overview
This repository demonstrates an automated ML model validation 
pipeline using GitHub Actions CI/CD for Assignment 4.

## Workflow Summary
The pipeline `.github/workflows/ml-pipeline.yml` performs:
1. **Checkout** – clones the repository code
2. **Python Setup** – configures Python 3.10
3. **Install Dependencies** – runs `pip install -r requirements.txt`
4. **Linter Check** – runs flake8 for code quality validation
5. **Model Dry Test** – verifies the ML environment is ready
6. **Artifact Upload** – uploads this README as `project-doc`

## Trigger Logic
- Runs on every **push** to any branch **except** `main`
- Runs on every **pull_request**

## Bugs Fixed in Original YAML
| # | Bug | Fix Applied |
|---|-----|-------------|
| 1 | Missing checkout step | Added `actions/checkout@v4` as first step |
| 2 | Wrong YAML indentation | Fixed all step indentation to correct levels |
| 3 | Empty Linter Check step | Added `flake8` run command |
| 4 | Mis-indented run block | Indented Python command inside block scalar |

## Repository
**GitHub:** https://github.com/HAMZA2FEKRY/ml-pipeline-assignment4
