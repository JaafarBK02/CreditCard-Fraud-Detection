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
- **Features**: 30 features (anonymized features (V1 to V28), `id`, and `Amount`)
- **Balanced**: 50% fraud, 50% non-fraud

---

## Model Used 

Since the dataset contains 568,630 transactions, it is considered large, which means we can use more complex and powerful models that benefit from larger amounts of data. I started with Logistic Regression because it is a simple and interpretable model that serves as a good baseline to evaluate performance. Then, I selected Random Forest, which is a tree-based ensemble model known for its robustness to noise and irrelevant features, which is useful here because the dataset has 30 anonymized features (V1–V28) that may contain hidden or less meaningful information. Random Forest is also efficient on large tabular datasets like this. Next, I used XGBoost, a gradient boosting model that typically outperforms Random Forest in terms of accuracy and efficiency on structured data. XGBoost handles imbalances, irrelevant features, and nonlinear patterns effectively, making it a top performer for many classification tasks. Although the dataset is balanced (50% fraud, 50% non-fraud), I still wanted to use XGBoost because of its overall strong performance and flexibility with large feature sets. These three models give me a strong mix of simplicity, interpretability, and high performance to compare and evaluate.

--

## Model Comparison

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

