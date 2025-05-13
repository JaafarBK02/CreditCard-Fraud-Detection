## Credit Card Fraud Detection - Machine Learning Project

During this project, I trained and compared several classification models to detect fraudulent credit card transactions using a 2023 Kaggle dataset.

## Project Overview

- **Goal**: Predict whether a credit card transaction is fraudulent.
- **Models Used**: Logistic Regression, Random Forest, XGBoost.
- **Dataset Source**: [Credit Card Fraud Detection-Kaggle]([https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud])

---

## Files

- `fraud_detection.ipynb` — main notebook with preprocessing, training, and evaluation
- `README.md` — this file
- `Presentation.pdf` - Google slide that I used to present my project to my class.
- `Fraud Detection Project Report.pdf` - Full report of the project.

---
##  Dataset Details (from Kaggle)

- **Transactions**:  284,807 transactions
- **Classes**: 0 = Non-fraudulent, 1 = Fraudulent
- **Features**: 30 features (anonymized features (V1 to V28), ` Time`, and `Amount`)
- **Unbalanced**: only 492 frauds, whic represent 0.172% of all transactions.

---

## Model Used 

I started with Logistic Regression because it is a simple and interpretable model that serves as a good baseline to evaluate performance. Then, I selected Random Forest, which is a tree-based ensemble model known for its robustness to noise and irrelevant features, which is useful here because the dataset has 28 anonymized features (V1–V28) that may contain hidden or less meaningful information. Random Forest is also efficient on large tabular datasets like this. Next, I used XGBoost, a gradient boosting model that typically outperforms Random Forest in terms of accuracy and efficiency on structured data. XGBoost handles imbalances, irrelevant features, and nonlinear patterns effectively, making it a top performer for many classification tasks. 


--
## Metrics used 

To properly evaluate our models on this highly imbalanced fraud detection dataset, I employed specialized metrics that focus on the minority class rather than relying on misleading measures like overall accuracy. The F1-score served as our primary metric because it balances both precision (ensuring most flagged transactions are truly fraudulent) and recall (capturing as many actual fraud cases as possible). We complemented this with detailed confusion matrix analysis to examine the exact distribution of false negatives (dangerous missed fraud cases) versus false positives (costly false alarms). 

For XGBoost, our best-performing model, this revealed an excellent 80% recall rate, detecting 113 of 142 fraud cases, while maintaining 82% precision. This comprehensive evaluation approach ensured we didn't just create a model that appeared accurate by always predicting "non-fraud," but one that actually identified real fraudulent transactions with meaningful reliability, striking the optimal balance between catching fraud and minimizing business disruption from false positives. The model's strong 0.81 F1-score demonstrated its superior ability to handle this imbalance compared to alternatives like logistic regression (7% recall) or random forest (~50% recall).

By using a combination of these metrics, I was able to gain a more comprehensive understanding of each model's performance. While all models performed well in terms of accuracy, the F1 score provided additional insights into how well the models handled fraud cases, with XGBoost achieving the highest balance between precision and recall.


---

Thank you for checking out this project! Feel free to explore the notebook to see each model's performance and evaluation.

