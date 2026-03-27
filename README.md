# unsupervised-anomaly-detection-zero-day
# A Comparative Analysis of Unsupervised Anomaly Detection Methods for Zero-Day Attack Detection in Real-World Network Traffic

## Overview
This project investigates the effectiveness of unsupervised anomaly detection methods for detecting malicious activities in real-world network traffic data. The main focus is on identifying zero-day attacks without relying on labeled data during the training phase.

## Objective
The objective of this study is to compare multiple unsupervised anomaly detection methods and evaluate their ability to detect anomalous behavior in network traffic under realistic conditions.

## Models Used
- One-Class SVM
- Isolation Forest
- Autoencoder
- Deep SVDD

## Dataset
The dataset used in this project is based on real-world network traffic collected from an operational environment. Due to confidentiality and privacy considerations, the dataset cannot be shared publicly.

## Method
The models were trained using only normal instances in order to learn the structure of normal network behavior. After training, anomaly scores were generated and converted into binary predictions using threshold-based decision rules.

## Final Results
| Model | Precision | Recall | F1-score |
|------|----------|--------|----------|
| Isolation Forest | 0.42 | 0.14 | 0.21 |
| One-Class SVM | 0.22 | 0.07 | 0.11 |
| Autoencoder (p90) | 0.20 | 0.07 | 0.10 |
| Deep SVDD | 0.07 | 0.02 | 0.03 |

Isolation Forest achieved the best overall performance in this study.

## Repository Structure
- `notebooks/` → Jupyter notebooks
- `results/` → result tables and figures
- `data/` → dataset description only
- `thesis/` → thesis-related files

## Notes
This repository does not include the raw dataset because of confidentiality restrictions.
