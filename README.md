# Telco Customer Churn Prediction

A machine learning project focused on analyzing and predicting customer churn in the telecommunications industry.

The project explores customer behavior, preprocesses the dataset, trains multiple machine learning models, and evaluates their ability to predict whether a customer is likely to churn.

## Project Overview

Customer churn refers to customers discontinuing their services. Predicting churn can help telecommunications companies identify customers who may be at risk and support data-driven customer retention strategies.

This project uses a dataset containing **7,043 telecom customers and 21 features** and treats churn prediction as a **binary classification problem** (`Yes` / `No`).

The analysis includes:

- Exploratory data analysis
- Data preprocessing
- Categorical variable encoding
- Feature scaling
- Correlation analysis
- Stratified train-test splitting
- Machine learning model development
- Model performance evaluation
- Confusion matrices
- ROC curves and ROC-AUC analysis
- Customer churn prediction

## Dataset

The dataset contains information about telecommunications customers, including demographic, service, contract, and billing-related attributes.

### Dataset Details

- **Customers:** 7,043
- **Features:** 21
- **Target:** Churn
- **Problem Type:** Binary Classification
- **Quantitative Features:** `MonthlyCharges`, `TotalCharges`, `tenure`
- **Categorical Features:** `gender`, `InternetService`, `Contract`, `PaymentMethod`, and others

The dataset contains an imbalanced target distribution:

| Churn Status | Percentage |
|--------------|------------|
| No Churn | 73.46% |
| Churn | 26.54% |

## Data Preprocessing

Several preprocessing steps were performed before model training.

### Missing Values

The `TotalCharges` feature contained missing values. Since only a small number of records were affected, those rows were removed.

### Categorical Encoding

Categorical variables were converted into numerical representations using **Label Encoding**.

### Feature Scaling

**StandardScaler** was applied to normalize the feature values before training the models.

### Train-Test Split

The dataset was divided using an **80/20 stratified split**:

- Training set: **5,634 samples**
- Testing set: **1,409 samples**

Stratification was used to maintain the churn distribution across the training and testing datasets.

## Machine Learning Models

Three machine learning classification models were developed and evaluated:

1. **K-Nearest Neighbors (KNN)**
2. **Decision Tree**
3. **Neural Network**

## Model Performance

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| KNN | 74.84% | 74.88% | 74.84% | 74.86% | **77.08%** |
| Decision Tree | 71.07% | 71.95% | 71.07% | 71.47% | 64.52% |
| Neural Network | **76.33%** | 74.76% | **76.33%** | **75.16%** | 76.87% |

The **Neural Network achieved the highest accuracy and F1-score**, while **KNN achieved the highest ROC-AUC score**.

## Key Findings

- The dataset contains a noticeable class imbalance, with churn representing 26.54% of customers.
- `TotalCharges` and `tenure` showed a strong positive correlation.
- `MonthlyCharges` and `TotalCharges` showed a moderate positive correlation.
- The Neural Network achieved the highest accuracy at **76.33%**.
- KNN achieved the highest ROC-AUC at **77.08%**.
- The Decision Tree produced the lowest ROC-AUC among the evaluated models.

## Technologies Used

- **Python**
- **Jupyter Notebook**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**

## Project Structure

```text
telco-customer-churn/
│
├── README.md
│
├── notebooks/
│   └── telco_customer_churn_analysis.ipynb
│
├── data/
│   └── telco_customer_churn.csv
│
└── report/
    └── telco_customer_churn_report.pdf
```

## Notebook

The Jupyter Notebook contains the complete implementation, including:

- Dataset loading and inspection
- Data preprocessing
- Exploratory analysis
- Feature transformation
- Model training
- Predictions
- Performance metrics
- Confusion matrices
- ROC curves
- Model comparison

## Future Improvements

Potential improvements identified for the project include:

- Feature engineering to create more informative predictors
- Hyperparameter tuning
- Ensemble learning methods
- Addressing class imbalance using techniques such as SMOTE or class weights
- Incorporating additional customer-related features
- Regular model retraining and performance monitoring
- Developing an automated alert system for high-risk customers

## Project Report

A detailed report describing the methodology, preprocessing, model development, evaluation, and conclusions is included in the `report/` directory.

## Project Contributors

- Nafisa Nahar Aka
- Tahsin Alam Sayed

---

**Telco Customer Churn Prediction | Machine Learning Project**
