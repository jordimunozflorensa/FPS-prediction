# FPS Prediction Using Machine Learning

This repository contains the implementation and documentation for a machine learning project aimed at predicting the Frames Per Second (FPS) in modern games based on the hardware specifications of the system. This project was developed as part of an academic requirement and is structured into two key files:

1. **`practica_final.ipynb`**: The Jupyter Notebook that contains the implementation of data preprocessing, model training, evaluation, and results analysis.
2. **`Informe.pdf`**: A comprehensive report detailing the methodology, experiments, and results.

## Project Overview

The goal of this project is to create a robust machine learning pipeline capable of predicting FPS using a dataset of modern gaming benchmarks. This approach allows users to estimate FPS for various hardware setups without performing actual tests, saving time and resources.

### Objectives

- Identify and analyze a real-world regression problem.
- Explore and preprocess the dataset to prepare it for machine learning.
- Experiment with linear and non-linear machine learning models.
- Evaluate and interpret the models using appropriate metrics.
- Justify the chosen final model based on performance and interpretability.

## Dataset

The dataset, sourced from Kaggle, includes:
- **24624 samples** with real benchmark data.
- **43 features**, including hardware specifications (CPU, GPU, etc.) and game settings.
- FPS values as the target variable.

The dataset combines numerical and categorical data, requiring extensive preprocessing, including:
- Handling missing, anomalous, and redundant values.
- Encoding categorical variables (binary, one-hot, and target encoding).
- Splitting into training, validation, and testing sets.

## Methodology

1. **Data Preprocessing**:
   - Addressed missing and anomalous values.
   - Eliminated irrelevant and redundant features using statistical measures like correlation and Variance Inflation Factor (VIF).
   - Created multiple preprocessed datasets for model experimentation.

2. **Modeling**:
   - Linear models: Linear Regression, Ridge, Lasso.
   - Non-linear models: Support Vector Machines (SVM), Random Forest, Multi-Layer Perceptron (MLP), and Gradient Boosting.
   - Ensemble methods: Voting and Stacking.

3. **Evaluation**:
   - Used metrics such as R², Mean Squared Error (MSE), and Mean Absolute Error (MAE).
   - Conducted model interpretability analysis using feature importance and residual analysis.

## Results

The Stacking ensemble model (SVM with RBF kernel, MLP, and XGBoost) was the best performer, achieving:
- **R²: 0.99992**
- **MSE: 0.228**
- **MAE: 0.350 FPS**

This model demonstrates high accuracy with minimal error, generalizing well across test data.

## Files

- **`practica_final.ipynb`**: Implementation of the machine learning pipeline, including:
  - Preprocessing steps.
  - Model training and hyperparameter optimization.
  - Evaluation and visualization of results.

- **`Informe.pdf`**: Detailed documentation of the project, including:
  - Background and objectives.
  - Data exploration and preprocessing methodology.
  - Comparative results of different models.
  - Justification of the final model and future improvements.

## How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo-name.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook `practica_final.ipynb` and run the cells sequentially.
4. Refer to `Informe.pdf` for in-depth explanations and insights.

## References

- Kaggle dataset: [FPS Benchmark Dataset](https://www.kaggle.com/datasets/ulrikthygepedersen/fps-benchmark)
- Key libraries used:
  - Scikit-learn
  - XGBoost
  - Matplotlib
  - Pandas
