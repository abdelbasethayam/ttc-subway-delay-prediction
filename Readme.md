# TTC Subway Delay Prediction

## Overview
Machine learning project that predicts whether a TTC subway incident will result in a service delay using only information available at the time of logging.

## Problem
TTC delays affect over 1 million daily riders. Early prediction allows proactive operational responses.

## Dataset
- Source: City of Toronto Open Data Portal (2025)
- Records: ~25,000 subway incidents
- Target: Binary (delay occurred or not)

## Approach
- Feature engineering (57 features):
  - Temporal (cyclical time, rush hour flags)
  - Station & line history
  - Incident code frequency
  - Rolling lag features (no data leakage)
- Chronological train/test split (80/20)
- Class imbalance handled using class weighting

## Models
- Logistic Regression (baseline)
- Gradient Boosting
- XGBoost
- LightGBM (best model)
- Random Forest
- Extra Trees
- KNN (failed baseline)

## Key Results
- 6/7 models achieved ≥ 0.80 recall
- Best F1: **0.749 (LightGBM)**
- Strongest predictor: incident cause code frequency

Repo structure
ttc-subway-delay-prediction/
│
├── README.md
├── ttc_subway_delay_prediction.ipynb
├── report.pdf
├── presentation.pptx
├── requirements.txt
└── .gitignore

## Authors
- Hayam Rezk
- Shorouk Rashed