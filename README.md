# Credit Card Fraud Detection

## Table of Contents
- [Project Objective](#project-objective)
- [Dataset Description](#dataset-description)
- [Project Workflow](#project-workflow)
- [ETL Framework](#etl-framework)
- [Model Building and Predictions](#model-building-and-predictions)
- [Results](#results)
- [Future Scope](#future-scope)

---

## Project Objective
The goal of this project is to detect fraudulent credit card transactions using machine learning models on a highly imbalanced dataset. By leveraging anomaly detection techniques, the project aims to:
- Identify fraudulent transactions with high precision and recall.
- Minimize false positives and false negatives for improved fraud prevention.
- Provide actionable insights for financial institutions to enhance security measures.

---

## Dataset Description
The dataset consists of anonymized credit card transaction data with the following key features:
- **Time**: The time of the transaction.
- **Amount**: The transaction amount in USD.
- **Features (V1 to V28)**: Anonymized features representing transaction details.
- **Class**: The target variable indicating whether a transaction is fraudulent (1) or legitimate (0).

**Dataset Details**:
- **Rows**: 284,807 transactions
- **Fraudulent Transactions**: ~0.172% of total data
- **Legitimate Transactions**: ~99.828% of total data

---

## Project Workflow
1. **Data Preprocessing**:
   - Handled missing values and normalized transaction amounts.
   - Addressed data imbalance by focusing on anomaly detection techniques instead of traditional classification.

2. **Exploratory Data Analysis (EDA)**:
   - Visualized class distributions to understand the data imbalance.
   - Analyzed relationships between transaction time, amount, and fraud likelihood.
   - Generated heatmaps to explore correlations between features.

3. **Model Building**:
   - Implemented three anomaly detection models:
     - Isolation Forest
     - Local Outlier Factor (LOF)
     - One-Class SVM
   - Evaluated models using precision, recall, F1-score, and accuracy metrics.

4. **Model Evaluation**:
   - Compared model performance and identified the best-performing algorithm.
   - Focused on reducing false positives and false negatives for practical use cases.

---

## ETL Framework
The project uses the following components for the pipeline:
- **CSV File**: Contains anonymized credit card transaction data.
- **Python (Pandas, NumPy)**: For data extraction, cleaning, and preprocessing.
- **Scikit-learn**: For implementing anomaly detection models.
- **Matplotlib & Seaborn**: For data visualization and insights.

---

## Model Building and Predictions
1. **Isolation Forest**:
   - Identified anomalies by isolating observations using random splits.
   - Effective for detecting rare fraud cases in a large dataset.

2. **Local Outlier Factor (LOF)**:
   - Measured local density deviations to flag transactions significantly different from neighbors.

3. **One-Class SVM**:
   - Created a decision boundary for normal transactions and flagged outliers as fraudulent.

**Key Performance Metrics**:
- **Precision**: 90%
- **Recall**: 88%
- **F1-Score**: 89%

---

## Results
- Detected fraudulent transactions with **90% precision** and **88% recall**, reducing the risk of false positives and negatives.
- Identified over **200 fraudulent transactions** out of a dataset with significant class imbalance.
- Insights revealed fraudulent transactions often involved unusual amounts and occurred at off-peak times.

---

## Future Scope
1. **Real-Time Detection**: Integrating the model into live transaction systems for immediate fraud prevention.
2. **Deep Learning**: Experimenting with recurrent neural networks (RNNs) to capture temporal dependencies in transaction sequences.
3. **Blockchain Integration**: Enhancing fraud detection with secure, decentralized transaction verification.
4. **Explainable AI**: Developing models that provide interpretable outputs to aid decision-making by financial analysts.
