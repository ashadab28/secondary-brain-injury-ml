# Secondary Brain Injury ML

Explainable machine learning for early prediction of secondary brain injury in neurocritical care using MIMIC-IV data.

## Overview

Secondary brain injury (SBI) is an important complication in critically ill neurological patients. This project focuses on developing and validating machine learning models for early prediction of secondary brain injury using clinical and physiological variables from neurocritical care patients.

The project is designed as a reproducible research framework, including data extraction, preprocessing, feature engineering, model development, evaluation, and explainability.

## Research Objective

To develop and evaluate machine learning models for predicting secondary brain injury among adult neurocritical care patients using routinely available clinical and physiological data.

## Dataset

This project uses:

- MIMIC-IV Clinical Database
- MIMIC-IV Waveform Database
- PhysioNet

Access to MIMIC-IV requires completion of the applicable PhysioNet credentialing and data-use requirements.

> **Data restriction:** Patient-level MIMIC-IV data are not included in this repository. Only code, documentation, and permitted derived materials are shared.

## Study Population

The study focuses on adult critically ill patients with major neurological conditions, including:

- Traumatic Brain Injury (TBI)
- Intracerebral Hemorrhage (ICH)
- Ischemic Stroke
- Subarachnoid Hemorrhage (SAH)

The analytical unit is based on ICU stays, with appropriate patient-level separation during model development and evaluation.

## Outcome Definition

The primary outcome is a binary classification of Secondary Brain Injury (SBI):

- SBI = Yes
- SBI = No

Potential clinical indicators include sustained physiological deterioration and neurological worsening, including:

- Intracranial pressure (ICP) elevation
- Mean arterial pressure (MAP) reduction
- Oxygen desaturation
- Neurological deterioration
- Escalation of neuroprotective management
- Relevant radiological evidence where available

The operational outcome definition is documented in the study methodology.

## Predictors

The machine learning pipeline includes routinely available clinical and physiological variables such as:

- Heart Rate (HR)
- Mean Arterial Pressure (MAP)
- Oxygen Saturation (SpO₂)
- Respiratory Rate (RR)
- Glasgow Coma Scale (GCS)
- GCS-derived features
- MAP-derived features
- Other eligible physiological measurements

Time-window based features include summary measures such as mean, minimum, maximum, first, last, and measurement counts where applicable.

## Machine Learning Models

The project framework supports evaluation of multiple machine learning approaches, including:

- Logistic Regression
- Random Forest
- Gradient Boosting
- XGBoost
- Long Short-Term Memory (LSTM)

Model development includes training, validation, hyperparameter optimization, threshold selection, and independent test evaluation.

## Model Evaluation

Model performance is evaluated using:

- AUROC
- Sensitivity
- Specificity
- Precision
- Recall
- F1-score
- Accuracy
- Brier score
- Calibration analysis
- Confusion matrix

Where applicable, confidence intervals and statistical comparisons are also considered.

## Explainability

Explainable AI methods are incorporated to understand model predictions and identify important clinical predictors.

The project includes:

- SHAP analysis
- Feature importance
- Global feature interpretation
- Individual prediction interpretation
- Model calibration

## Reproducibility

The repository is structured to support reproducible machine learning research.

The workflow includes:

1. Data extraction
2. Data cleaning
3. Feature engineering
4. Missing-data handling
5. Dataset construction
6. Patient/ICU-level data splitting
7. Model training
8. Hyperparameter optimization
9. Model evaluation
10. Explainability analysis

## Repository Structure

```text
secondary-brain-injury-ml/
│
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
│
├── data/
│   └── README.md
│
├── notebooks/
│   ├── 01_data_extraction.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_model_training.ipynb
│   └── 05_model_evaluation.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   ├── train.py
│   ├── evaluate.py
│   └── explainability.py
│
├── results/
│   ├── figures/
│   ├── metrics/
│   └── shap/
│
└── docs/
    └── methodology.md
