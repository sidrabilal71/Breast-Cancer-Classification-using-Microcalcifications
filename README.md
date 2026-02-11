# Breast Cancer Classification using Microcalcifications

This project focuses on the classification of microcalcifications (MCs) in breast cancer data, distinguishing between benign and malignant cases. Using a dataset of 150 features extracted from mammography images, we implement and evaluate machine learning models at both the microcalcification and patient levels.

## Project Overview

Microcalcifications are tiny calcium deposits that can be an early sign of breast cancer. This project uses predictive modeling to assist in the diagnosis process by analyzing radiomic features.

### Key Features

* **Feature Set**: 150 features extracted from mammography images (shape, first-order statistics, and wavelet-based texture features).
* **Evaluation Levels**:
* **MC Level**: Individual microcalcification classification.
* **Patient Level**: Aggregated prediction for the patient.


* **Robust Validation**: Utilizes 5-fold patient-wise cross-validation (**GroupKFold**) to prevent data leakage and ensure the model generalizes to new patients.

## Models Implemented

The following algorithms were trained and compared with and without hyperparameter tuning:

* **Logistic Regression**
* **Random Forest**
* **K-Nearest Neighbors (KNN)**

## Workflow

1. **Data Loading**: Importing feature data from Excel sources.
2. **Exploratory Data Analysis (EDA)**:
* Analyzing label distribution (Benign vs. Malignant).
* Visualizing patient-wise data distribution.
* Statistical analysis of features (Elongation, Kurtosis, etc.).


3. **Data Preprocessing**: Handling feature separation and patient grouping.
4. **Model Training**: Implementing cross-validation pipelines.
5. **Evaluation**: Performance reporting using Accuracy and F1-score.

## Dataset Structure

The dataset includes:

* `Patient ID`: Used for group-wise splitting.
* `Label`: 0 for Benign, 1 for Malignant.
* `Features`: 150 columns of radiomic data (e.g., `original_shape_Elongation`, `wavelet-LHL_glrlm_RunVariance`).

## Installation & Usage

### Prerequisites

* Python 3.x
* Pandas
* Matplotlib
* Scikit-learn

### Running the Project

The project is provided as a Jupyter Notebook (`Breast_Cancer_Classification.ipynb`).

1. Clone the repository.
2. Ensure your dataset (`Reduced Features for TAI project.xlsx`) is in the project directory.
3. Run the notebook cells sequentially to reproduce the analysis.

## Results Summary

The models provide comparative insights into the diagnostic power of various machine learning approaches, highlighting the effectiveness of ensemble methods (Random Forest) vs. linear methods (Logistic Regression) for this specific medical dataset.

---

**Author**: Sidra Bilal
