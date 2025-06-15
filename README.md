# AlphaCare Insurance Analytics

## Project Overview

This repository is part of AlphaCare Insurance Solutions' data analytics initiative to enhance risk modeling and optimize marketing strategies. It contains the analysis and data engineering work for:

- **Task 1:** Exploratory Data Analysis (EDA) & Statistical Investigation
- **Task 2:** Reproducible and auditable data pipeline setup using **Data Version Control (DVC)**

---


---

## Task 1: EDA & Statistical Analysis

### Objectives
- Understand the distribution and structure of historical insurance data (Feb 2014–Aug 2015)
- Detect patterns in **loss ratio**, **claim behavior**, and **geographical/temporal trends**
- Support business decisions such as premium adjustments and risk targeting

### Key Analyses Conducted
- Data Quality Assessment (null values, data types, formatting)
- Descriptive Statistics and Outlier Detection
- Univariate and Bivariate Exploratory Analysis
- Correlation between Premium and Claim Amounts by:
  - Province
  - Gender
  - Vehicle Type
- Temporal analysis of monthly claim and premium activity
- Top vehicle makes/models by average claims

## Task 2: Data Version Control with DVC

### Why DVC?
In the finance and insurance industry, reproducibility and auditability of data are critical. DVC enables versioning of data and model pipelines—much like Git for code.

### DVC Setup Steps
1. **Initialize DVC in the project:**   
```bash
   dvc init
```
2. Track raw data:
```bash
   dvc add data/raw/MachineLearningRating_v3.txt
```
3. Set up local DVC remote:
```bash
dvc remote add -d localstorage ~/dvc_storage
```
4. Push data to remote:
```bash
dvc push
```

## Branch Workflow
Main work happens in task-specific branches:
- task-1 — for EDA notebook & visualizations
- task-2 — for DVC setup & data pipeline configuration

Changes are merged via Pull Requests (PRs) to main.
