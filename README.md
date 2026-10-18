# A Comparative Study of Resampling and Cost-Sensitive Learning for Imbalanced Credit Card Fraud Detection

## Overview

Credit card fraud detection is a challenging machine learning problem because fraudulent transactions represent only a small proportion of all transactions. This severe class imbalance can cause traditional classification models to favor legitimate transactions while failing to identify fraudulent activities.

This project investigates the performance of resampling techniques and cost-sensitive learning for imbalanced credit card fraud detection. It compares multiple machine learning classifiers under different class-imbalance handling strategies.

## Research Objectives

- Investigate the impact of class imbalance on credit card fraud detection.
- Compare resampling techniques for improving fraud detection performance.
- Evaluate cost-sensitive learning using class weights.
- Compare the performance of different machine learning classifiers.
- Identify suitable approaches for balancing fraud detection and false-positive reduction.

## Dataset

The project uses the European Credit Card Fraud Detection dataset available through Kaggle.

- Total transactions: 284,807
- Fraudulent transactions: 492
- Legitimate transactions: 284,315
- Fraud proportion: approximately 0.172%

The dataset contains anonymized transaction features, transaction amounts, and a binary class label identifying fraudulent transactions.

The raw dataset is not included in this repository. Users should obtain it from the original dataset source and follow its applicable terms.

## Machine Learning Models

The following classifiers are investigated:

- Logistic Regression
- Decision Tree
- Random Forest

## Class-Imbalance Handling Techniques

The experimental comparison includes:

1. Baseline learning without additional imbalance handling
2. Random Oversampling
3. Random Undersampling
4. Synthetic Minority Over-sampling Technique (SMOTE)
5. Cost-sensitive learning using class weights

## Methodology

The research workflow consists of:

1. Loading and inspecting the dataset.
2. Preparing the features and target variable.
3. Splitting the data into stratified training and testing sets.
4. Applying preprocessing where required.
5. Applying resampling techniques to the training data only.
6. Training the selected classifiers under the experimental configurations.
7. Evaluating predictions on the held-out test set.
8. Comparing results and discussing the implications.

Resampling is performed only on the training data to avoid information leakage into the test set.

## Evaluation Metrics

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion matrix

Particular attention is given to recall, precision, and F1-score because accuracy alone can be misleading when fraudulent transactions are rare.

## Repository Structure

```text
credit-card-fraud-detection/
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
├── data/
├── notebooks/
├── src/
├── results/
├── docs/
└── references/
```

The final structure may differ depending on the implementation files included in the repository.

## Installation and Usage

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/credit-card-fraud-detection.git
cd credit-card-fraud-detection
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Prepare the dataset

Download the dataset from its original source and place the required CSV file in the location specified by the project configuration or notebook.

### 5. Run the experiments

Follow the instructions for the notebooks or Python scripts included in the repository. The exact commands will be documented after the implementation files are finalized.

## Results

Experimental results, performance comparison tables, and visualizations will be documented here after verification against the actual model outputs.

No performance claims should be interpreted as established until the corresponding experiments have been executed and evaluated.

## Research Scope and Limitations

This project is an experimental comparison using a publicly available, anonymized dataset. Results may depend on the train-test split, preprocessing choices, model parameters, sampling strategies, and decision thresholds.

Performance on this dataset does not guarantee equivalent performance in a real-world payment system.

## References

- European Credit Card Fraud Detection dataset, available through Kaggle.
- Chawla, N. V., et al. (2002). SMOTE: Synthetic Minority Over-sampling Technique. *Journal of Artificial Intelligence Research*, 16, 321–357. https://doi.org/10.1613/jair.953

## Author

**YOUR NAME**

GitHub: https://github.com/YOUR-USERNAME

## Disclaimer

This project is intended for academic research and educational purposes. It is not a production-ready fraud detection system.
