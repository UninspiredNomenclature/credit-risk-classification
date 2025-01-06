# credit-risk-classification

# Module 20 Report

## Overview of the Analysis
This analysis attempts to determine the feasibility of using a linear regression model in determining credit risk from a variety of financial data to determine whether a borrower represents a high or low credit risk. Data for this analysis includes: loan amounts, interest rates, borrower income, debt-to-income ratio, the number of accounts a borrower has, negative marks on a credit report, total debt amount, and loan status.

This data was primarily used to predict a 'loan status' variable, divided into two categories: 0 (low risk) and 1 (high risk). A value count analysis of the target variable showed a significant class imbalance, with low-risk loans (0) being the dominant class compared to high-risk loans (1).

This process included data preprocessing - inspecting the data and accounting for missing values or inconsistancies, while categorical features were encoded using one-hot encoding and numerical features were standarized with a StandardScaler. The data was split into training and testing sets, with 75% of the data allocated for training and 25% for testing. A Logistic Regression was chosen as the primary algorithm due to its simplicity and interpretability for binary classification tasks, using a linear decision boundary to classify data points into low-risk or high-risk categories. The performance of the model was evaluated using a variety of metrics, including precision, recall, F1-score, and accuracy.

## Results
The performance of the logistic regression model was evaluated using accuracy, precision, recall, and F1-score metrics. Below is a summary of the results:

Machine Learning Model: Logistic Regression
* Accuracy: 99%. The model achieved a high accuracy, indicating that it correctly classified 99% of the total data points in the testing set.
* Precision: Class 0 (Low Risk): 1.00. Class 1 (High Risk): 0.85 The model achieved perfect precision for the low-risk category, meaning all instances predicted as low risk were indeed low risk. For the high-risk category, 85% of the predicted high-risk loans were correctly classified, reflecting room for improvement in identifying high-risk loans with precision.
* Recall: Class 0 (Low Risk): 0.99. Class 1 (High Risk): 0.95. The model successfully identified 99% of the actual low-risk loans, indicating excellent sensitivity for this category. The recall for high-risk loans was lower, with 95% of actual high-risk loans being identified. While strong, this highlights that 5% of high-risk loans were misclassified as low risk.
* F1-Score: Class 0 (Low Risk): 1.00. Class 1 (High Risk): 0.89. The harmonic mean of precision and recall for low-risk loans is perfect, signifying strong and balanced performance. The F1-score for high-risk loans is slightly lower due to the trade-off between precision and recall but remains robust.

## Summary
The model demonstrated exceptional performance in predicting low-risk loans, with near-perfect precision, recall, and F1-scores. For high-risk loans, the model achieved strong recall and reasonable precision, though the precision score indicates that some false positives were present in the predictions. Overall, the weighted average F1-score (0.99) and accuracy (99%) underscore the model's effectiveness in handling the imbalanced dataset while maintaining high classification quality for both categories. By leveraging these metrics, the model provides actionable insights for predicting credit risk, with potential for further optimization to enhance precision for high-risk classifications.

Further analysis should:
* Balance the Dataset: Oversampling the minority class (high-risk) or undersampling the majority class (low-risk) to address the class imbalance.
* Focus on High-Risk Cases: Adjust the model threshold to increase sensitivity for high-risk predictions, even if it slightly reduces precision.
* Model Selection: Consider using ensemble methods like Random Forest or Gradient Boosting to improve high-risk predictions.

## Conclusion
The model shows excellent performance for classifying credit risk, particularly for low-risk cases. Future iterations should prioritize improving predictions for high-risk cases to enhance the model’s utility in real-world financial decision-making. By addressing class imbalance and tuning the model, further improvements can be achieved.


Resources: For this assignment, personal class notes, tutoring sessions, starter code, course-supplied dataset, and ChatGPT were used in writing the code and analysis.