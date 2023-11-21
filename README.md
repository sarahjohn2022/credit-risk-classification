# credit-risk-classification

Purpose of the Analysis:
The purpose of this analysis is to develop and evaluate machine learning models for predicting credit risk in a peer-to-peer lending context. The goal is to assist in assessing the creditworthiness of borrowers, thereby informing lending decisions to mitigate the risk of default.

Financial Information and Prediction Target:
The dataset used in this analysis contains historical lending activity from a peer-to-peer lending services company. The primary focus is on predicting the likelihood of loans being healthy (0: low risk) or high-risk (1: high risk) based on various financial features.

Variable Information:
The target variable (loan_status):
  0: Healthy loans
  1: High-risk loans

Stages of the Machine Learning Process
1. Data Preparation:
   - Data was loaded from a CSV file and split into training and testing sets.
   - Labels and features were separated, and the imbalance in the target variable was addressed through resampling.
2. Model Training:
   - Logistic Regression models were trained on both the original and resampled training data.
3. Model Evaluation:
   - The performance of each model was evaluated using accuracy, balanced accuracy, confusion matrix, and classification report metrics.
  
Machine Learning Models and Scores:
1. Original Data Model
      Logistic Regression Model:
        - Balanced Accuracy: 0.9521
        - Precision (Class 0): 1.00
        - Recall (Class 0): 1.00
        - Precision (Class 1): 0.86
        - Recall (Class 1): 0.91
2. Resampled Data Model
      Logistic Regression Model (with RandomOverSampler):
        - Balanced Accuracy: 0.9942
        - Precision (Class 0): 1.00
        - Recall (Class 0): 0.99
        - Precision (Class 1): 0.85
        - Recall (Class 1): 0.99

Summary and Recommendation:
Both models perform well, but the resampled data model outperforms the original data model across all metrics. The resampled model achieved higher balanced accuracy and improved precision and recall for the minority class (high-risk loans).

Recommendation:
Considering the better performance of the resampled model, it is recommended for deployment in assessing credit risk in peer-to-peer lending scenarios.

Considerations:
The choice of the best-performing model will depend on the specific goals of the lending company. If avoiding false positives (misclassifying healthy   loans as high-risk) is crucial, the resampled model may be preferred. Regular monitoring and updates to the model are advised to ensure continued relevance and effectiveness in the evolving lending landscape.
