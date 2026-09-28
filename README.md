# Secondary Brain Injury ML

## Overview
This project focuses on developing an explainable machine learning model for predicting Secondary Brain Injury (SBI) in neurocritical care patients using the MIMIC-IV Database. The project aims to identify clinically relevant patterns in routinely recorded ICU data and evaluate machine learning approaches for early SBI prediction.

## Research Objective
To develop and validate a machine learning model for predicting secondary brain injury (SBI) in neurocritical care patients using clinical data from the MIMIC-IV Database.

## Dataset
MIMIC-IV Database

## Study Population
Adult neurocritical-care ICU patients
TBI
ICH
ischemic stroke
SAH

## Outcome Definition
Secondary Brain Injury (SBI)
ICP/MAP/SpO₂/neurological deterioration criteria

## Predictors
HR
MAP
SpO₂
RR
GCS
derived 6-hour GCS/MAP features

## Machine Learning Models
Logistic Regression
Random Forest
Gradient Boosting
XGBoost
LSTM

## Explainability
SHAP
feature importance
calibration
AUROC

## Repository Structure
secondary-brain-injury-ml/
├── README.md
├── LICENSE
├── .gitignore
├── data/
├── notebooks/
├── src/
├── models/
├── results/
└── docs/

## Reproducibility
The repository provides reproducible code and documentation for data preprocessing, feature engineering, model development, evaluation, and explainability. Random seeds and analysis workflows are documented where applicable. MIMIC-IV data are not included in this repository and require authorized access through PhysioNet.

## Data Access
The study uses the MIMIC-IV Database. Access to the dataset is restricted and requires credentialed access through PhysioNet. No patient-level data are included in this repository. Researchers should obtain access directly from PhysioNet and comply with all applicable data-use requirements.

## Ethical and Data-Use Considerations
This project uses the MIMIC-IV Database, which contains de-identified clinical data. Access to the database is restricted and requires completion of the applicable PhysioNet credentialing and data-use requirements.

No raw MIMIC-IV patient-level data are included in this repository.
Patient privacy and confidentiality are maintained throughout the project.
The repository contains only code, documentation, and permitted non-identifiable research outputs.
Users must obtain authorized access to MIMIC-IV independently and comply with the applicable PhysioNet Data Use Agreement and database terms.
The models developed in this repository are intended for research purposes and should not be used as a standalone clinical decision-making tool.

## Current Status
Research and model development are ongoing. The repository is being developed to support reproducible preprocessing, feature engineering, machine learning model development, evaluation, and explainability for secondary brain injury prediction.

## Citation
## Citation

If you use the MIMIC-IV database in this project, please cite:

Johnson AEW, Bulgarelli L, Shen L, Gayles A, Shammout A, Horng S, et al. MIMIC-IV, a freely accessible electronic health record dataset. Scientific Data. 2023;10:1. https://doi.org/10.1038/s41597-022-01899-x

## License
This project is licensed under the MIT License.

The source code may be used, modified, and distributed under the terms of the MIT License. The MIMIC-IV database is not included in this repository and remains subject to the data-use terms and access requirements of PhysioNet.
