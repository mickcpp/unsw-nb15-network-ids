# Network Intrusion Detection with Machine Learning on UNSW-NB15

---

## Badges

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
[![Colab - EDA](https://img.shields.io/badge/Colab-EDA-F9AB00?logo=googlecolab)](https://github.com/mickcpp/unsw-nb15-network-ids/blob/main/notebook/01_eda_unsw_nb15.ipynb)
[![Colab - Pre-processing](https://img.shields.io/badge/Colab-Preprocessing-F9AB00?logo=googlecolab)](https://github.com/mickcpp/unsw-nb15-network-ids/blob/main/notebook/02_preprocessing.ipynb)
[![Colab - Modeling](https://img.shields.io/badge/Colab-modeling-F9AB00?logo=googlecolab)](https://github.com/mickcpp/unsw-nb15-network-ids/blob/main/notebook/03_modeling.ipynb)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Research-brightgreen)
![Maintained](https://img.shields.io/badge/Maintained-Yes-success)
![Project](https://img.shields.io/badge/Academic-Project-purple)
![Reproducibility](https://img.shields.io/badge/Reproducibility-Available-green)

---

## Project Overview

This repository implements a complete Machine Learning pipeline for Network Intrusion Detection Systems (NIDS), applied to the UNSW-NB15 dataset. The project covers supervised classification (binary intrusion detection using algorithms such as Logistic Regression, Linear SVM, Random Forest, Extra Trees and XGBoost) as well as unsupervised learning through K-Means clustering, aimed at exploring latent structures in network traffic. All experiments follow a rigorous methodology encompassing data preprocessing, feature engineering, hyperparameter optimization via stratified k-fold cross-validation, and multi-metric evaluation, with an emphasis on reproducibility and avoidance of data leakage.

---
## Repository Structure

```text
main/
├── notebooks/
│   └── *.ipynb
└── results/
    ├── *.csv
    └── *.png
```


### notebooks/

Contains all Google Colab notebooks (`.ipynb`) implementing the complete experimental pipeline, including data loading, preprocessing, exploratory data analysis (EDA), feature engineering, supervised Machine Learning experiments, unsupervised K-Means experiments, model evaluation and result generation. The notebooks are designed to be executed sequentially within the Google Colab environment.

### results/

Contains every artifact produced during the experiments. This includes CSV files with quantitative results (metrics and evaluation tables) and PNG figures generated during EDA, model evaluation, confusion matrices, ROC curves, Precision-Recall curves, feature importance visualizations, and clustering visualizations (PCA projections). This directory stores only outputs produced during execution of the notebooks and is not manually populated.

---

## Experimental Workflow

1. **Dataset loading** — Import of the UNSW-NB15 dataset (training and test partitions).
   ↓
2. **Data preprocessing** — Removal of duplicate records, handling of redundant features, encoding of categorical variables, and treatment of skewed numerical features to prevent data leakage.
   ↓
3. **Exploratory Data Analysis** — Statistical analysis of feature distributions, target variable balance, and outlier detection.
   ↓
4. **Feature Engineering** — Transformation and selection of features, including log transformations and importance-based dimensionality reduction.
   ↓
5. **Supervised Learning** — Training and hyperparameter optimization of classifiers (Logistic Regression, Linear SVM, Random Forest, Extra Trees, XGBoost) via GridSearch with stratified cross-validation.
   ↓
6. **Unsupervised Learning (K-Means)** — Clustering of network traffic to explore latent structures independent of labels.
   ↓
7. **Model Evaluation** — Assessment using Accuracy, Precision, Recall, F1-score, ROC-AUC and PR-AUC, along with confusion matrix analysis.
   ↓
8. **Result Export** — Generation and storage of CSV metric tables and PNG visualizations inside `results/`.

---

## Repository Contents

| Directory | Description | Content | Purpose |
|---|---|---|---|
| `notebooks/` | Experimental pipeline notebooks | `.ipynb` files covering loading, preprocessing, EDA, feature engineering, supervised and unsupervised experiments, evaluation | Implement and document the full ML workflow, executable in Google Colab |
| `results/` | Experiment outputs | `.csv` metric reports; `.png` figures (EDA plots, confusion matrices, ROC/PR curves, feature importance, PCA projections) | Store all artifacts generated during notebook execution |

---

## Results

The `results/` directory contains quantitative outputs (CSV files) summarizing evaluation metrics such as Accuracy, Precision, Recall, F1-score, ROC-AUC and PR-AUC for the supervised classifiers, as well as internal and external clustering metrics for the K-Means experiments. Generated figures include exploratory data analysis plots, confusion matrices, ROC and Precision-Recall curves, feature importance charts, and PCA-based clustering visualizations. All files are produced automatically by the notebooks during execution.

---

## Running the Project

- Open the desired notebook from `notebooks/` in Google Colab.
- Execute the notebook cells sequentially, following the order of the experimental workflow.
- All generated outputs (CSV reports and PNG figures) are automatically saved inside the `results/` directory.

---

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Google Colab | Notebook execution environment |
| Jupyter Notebook | Interactive development and documentation |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical computations |
| Scikit-Learn | Machine learning models and evaluation utilities |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| XGBoost | Gradient boosting classifier |

---

## Reproducibility

All experiments are reproducible through the notebooks contained in `notebooks/`, which represent the complete experimental workflow from data loading to result generation. Every artifact produced by the experiments, including metric tables and figures, is stored inside `results/`, ensuring that outcomes can be independently verified and reviewed.

---


## Citation

If you use this repository in your research, please cite it as follows:

```bibtex
@misc{nids_unsw_nb15,
  author       = {Marco Renella, Roberto Giuseppe Scarpa)},
  title        = {Progettazione Metodologica di una Pipeline di Machine Learning per Sistemi di Rilevamento Intrusioni basata sul Dataset UNSW-NB15},
  year         = {2026},
  howpublished = {GitHub repository},
  url          = {Repository URL}
}
```

---

## Contact

For questions or collaboration inquiries, please contact the repository maintainer(s) via the contact details provided on their GitHub profile.
