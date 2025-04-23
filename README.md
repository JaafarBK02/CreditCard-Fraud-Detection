## Credit Card Fraud Detection - Machine Learning Project

During this project, I trained and compared several classification models to detect fraudulent credit card transactions using a 2023 Kaggle dataset. The dataset was already clean and balanced, allowing me to focus on building and evaluating models.

## Project Overview

- **Goal**: Predict whether a credit card transaction is fraudulent.
- **Models Used**: Logistic Regression, Random Forest, XGBoost.
- **Dataset Source**: [Credit Card Fraud Detection Dataset 2023 - Kaggle](https://www.kaggle.com/datasets/nelgiriyewithana/credit-card-fraud-detection-dataset-2023)

---

## What I Did

I started by loading and exploring the dataset, confirming there were no missing values or duplicates. Since the dataset was already balanced, I skipped resampling techniques like SMOTE.

Then, I split the dataset into training and testing sets (80/20 split). I trained three models: Logistic Regression, Random Forest, and XGBoost. After training, I evaluated each model's performance using accuracy, precision, recall, F1-score, and a confusion matrix.

Random Forest performed the best with almost perfect accuracy, followed closely by XGBoost. Logistic Regression also achieved strong performance.

---

## Files

- `fraud_detection.ipynb` — main notebook with preprocessing, training, and evaluation
- `README.md` — this file

---
##  Dataset Details (from Kaggle)

- **Transactions**: 568,630
- **Classes**: 0 = Non-fraudulent, 1 = Fraudulent
- **Features**: 30 anonymized features (V1 to V28), `Time`, and `Amount`
- **Balanced**: 50% fraud, 50% non-fraud

---

## Model Comparison

All models showed high accuracy due to the clean and balanced nature of the dataset : 
- Logistic Regression : 96.43%
-  Random Forest : 99.99%
-   GBoost : 99.97%  

## Visualizations

### Class Distribution
A countplot was created to confirm that the dataset was balanced:
![Fraud vs Non-Fraud](fraud_distribution.png)

### Model Accuracy Comparison 
![Confusion Matrix](model_accuracy_comparison.png)


### Confusion Matrix
Each model's confusion matrix was plotted to evaluate performance on false positives and false negatives.

![Confusion Matrix](confusion_matrix.png)
![Confusion Matrix](confusion_matrix2.png)
![Confusion Matrix](confusion_matrix3.png)

---

Thank you for checking out this project! Feel free to explore the notebook to see each model's performance and evaluation.

