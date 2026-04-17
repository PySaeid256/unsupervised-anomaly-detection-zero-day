# unsupervised-anomaly-detection-zero-day
# A Comparative Analysis of Unsupervised Anomaly Detection Methods for Zero-Day Attack Detection in Real-World Network Traffic

## Overview
This project investigates the effectiveness of unsupervised anomaly detection methods for detecting malicious activities in real-world network traffic data, with a focus on identifying zero-day attacks.

Traditional intrusion detection systems rely on labeled data and known attack signatures, making them ineffective against unknown threats. This study explores unsupervised approaches that learn normal behavior and detect deviations without requiring labeled data during training.

---

## Objective
The objective of this study is to compare multiple unsupervised anomaly detection methods and evaluate their performance in detecting anomalies under realistic, noisy, real-world conditions.

---

## Key Contribution
- Comparative analysis of four anomaly detection models  
- Evaluation on real-world network traffic data  
- Analysis of model performance under noisy conditions  
- Insight: model performance depends more on data than model complexity  

---

## Models Used
- One-Class SVM (boundary-based)
- Isolation Forest (tree-based)
- Autoencoder (reconstruction-based)
- Deep SVDD (deep learning-based)

---

## Dataset
The dataset consists of real-world network traffic collected from an operational environment.

- Fully labeled dataset  
- Labels used only for evaluation  
- Not used during training to preserve unsupervised learning  

Due to privacy and confidentiality constraints, the dataset cannot be publicly shared.

---

## Methodology
The workflow consists of the following steps:

1. Data preprocessing (feature selection and normalization)  
2. Training models on normal data only  
3. Generating anomaly scores  
4. Applying threshold-based classification  
5. Evaluating results using precision, recall, and F1-score  

Thresholds (85%, 90%, 95%) were tested, with the 90th percentile providing the best balance.

---

## Results

| Model              | Precision | Recall | F1-score |
|-------------------|----------|--------|----------|
| **Isolation Forest**  | **0.42** | **0.14** | **0.21** |
| One-Class SVM     | 0.22     | 0.07   | 0.11     |
| Autoencoder       | 0.20     | 0.07   | 0.10     |
| Deep SVDD         | 0.07     | 0.02   | 0.03     |

Isolation Forest achieved the best performance due to its robustness and scalability in handling noisy real-world data.

---

## Key Insights
- Real-world data is significantly more complex than benchmark datasets  
- Model complexity does not guarantee better performance  
- Simpler models can outperform deep learning models in noisy environments  

---

## Practical Implications
This approach can be applied in real-time intrusion detection systems, especially using scalable models like Isolation Forest.

---

## Limitations
- Performance depends on dataset characteristics  
- Threshold selection impacts results  
- Deep models require careful tuning  

---

## Future Work
- Evaluate on multiple datasets  
- Explore adaptive thresholding  
- Develop hybrid anomaly detection models  

---

## Repository Structure
- `notebooks/` → Jupyter notebooks  
- `results/` → evaluation results  
- `data/` → dataset description only  
- `thesis/` → thesis files  
y restrictions.
