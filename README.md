# credit-risk-classification

## Overview of the Analysis

In this analysis, the goal was to develop a machine learning model to predict loan risk, specifically to classify loans as either high-risk (`1`) or healthy (`0`). This analysis was aimed at helping financial institutions assess loan applicants' risk of default based on a variety of features in the provided dataset. By accurately predicting loan risk, financial institutions can better manage lending practices and minimize losses from defaults.

The dataset consisted of financial information related to loan applicants, including various attributes used to assess loan risk. The target variable, `loan_status`, indicated whether a loan was high-risk (`1`) or healthy (`0`).

The stages of the machine learning process for this analysis included:
1. **Data Preprocessing**: Separating the data into features (`X`) and labels (`y`), then splitting the data into training and testing sets.
2. **Model Selection**: Logistic Regression was chosen as the primary classification algorithm.
3. **Model Training**: The Logistic Regression model was trained on the training data.
4. **Model Evaluation**: The model was evaluated using a confusion matrix and a classification report to understand its precision, recall, and F1-scores for both loan statuses.

## Results

### Logistic Regression Model:
- **Accuracy**: 99% – The model is highly accurate, correctly predicting the loan status for 99% of the test data.
- **Precision**: 
  - **Healthy loan (`0`)**: 1.00 – When the model predicts a loan as healthy, it is 100% accurate.
  - **High-risk loan (`1`)**: 0.86 – When the model predicts a loan as high-risk, it is correct 86% of the time.
- **Recall**:
  - **Healthy loan (`0`)**: 0.99 – The model successfully identifies 99% of all actual healthy loans.
  - **High-risk loan (`1`)**: 0.94 – The model successfully identifies 94% of all actual high-risk loans.
- **F1-Score**:
  - **Healthy loan (`0`)**: 1.00
  - **High-risk loan (`1`)**: 0.90

## Summary

The Logistic Regression model performed exceptionally well overall, particularly in predicting healthy loans. It achieved a perfect precision of 1.00 for healthy loans and a recall of 0.99, meaning nearly all healthy loans were correctly identified. For high-risk loans, the model also performed well, with a precision of 0.86 and a recall of 0.94.

Given the nature of this problem, it may be more important to minimize false negatives (i.e., correctly identifying high-risk loans), which this model handles reasonably well, with a recall of 0.94 for high-risk loans. However, the precision of 0.86 for high-risk loans suggests there may still be some false positives, meaning a few healthy loans are being classified as high-risk.

### Recommendation:
- **Logistic Regression** performs best and should be recommended for this task because it provides excellent accuracy, precision, and recall across both healthy and high-risk loans. The high recall for high-risk loans suggests the model effectively identifies most high-risk applicants, which is crucial for minimizing potential defaults.
- The performance of this model depends on the business objective. If it is more important to identify high-risk loans (to avoid defaults), the recall for high-risk loans would be the key metric to focus on, and the model performs well with a recall of 0.94.

If further improvements are needed to minimize false positives for high-risk loans, additional techniques such as hyperparameter tuning or experimenting with other algorithms (e.g., Random Forest, Gradient Boosting) may be considered.

## Code Source
- Learning Assistant
- GitHub location: https://github.com/jeffjunohkim/credit-risk-classification.git
