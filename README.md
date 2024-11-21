# Overview of the Analysis

Developing a model to accurately evaluate borrower creditworthiness is essential for peer-to-peer lending services. Such a model helps lenders assess lending risks, set appropriate interest rates, and make informed loan approval decisions. By analyzing historical borrower data and financial metrics, lenders can predict the likelihood of default and improve decision-making. This project utilizes a dataset containing historical lending activity from a peer-to-peer lending service to build a model for assessing borrower creditworthiness.

## Data Attributes (77,536 data entries)

- **loan_size**: The borrowed amount.
- **interest_rate**: The loan's interest percentage.
- **borrower_income**: The borrower's annual income.
- **debt_to_income**: Ratio of total debt payments to gross income.
- **num_of_accounts**: Number of credit accounts held by the borrower.
- **derogatory_marks**: Negative credit report entries, such as late payments or bankruptcies.
- **total_debt**: Total debt owed by the borrower.
- **loan_status**: Loan outcome, categorized as "healthy" (low risk) or "high risk."

## Machine Learning Process

1. **Data Loading and Exploration**  
2. **Data Split**: Dividing data into training and testing sets.  
3. **Model Training**: Training the logistic regression model.  
4. **Model Fitting**: Adjusting model parameters for optimal performance.  
5. **Testing**: Evaluating the model on unseen data.  
6. **Performance Evaluation**: Measuring accuracy, precision, and recall.  

## Results

### Confusion Matrix Analysis
- **Healthy Loans (Low Risk)**: Correctly predicted 18,663 out of 18,765.  
- **High-Risk Loans**: Correctly predicted 563 out of 619.

### Classification Report
| Loan Type      | Precision | Recall | F1-Score | Support |
|----------------|-----------|--------|----------|---------|
| Healthy Loan   | 1.00      | 0.99   | 1.00     | 18,765  |
| High-Risk Loan | 0.85      | 0.91   | 0.88     | 619     |
| **Overall**    | **Accuracy: 99%**, Macro Avg: 0.94, Weighted Avg: 0.99 |

### Summary of Metrics
- **Healthy Loans**: Nearly perfect precision (100%) and recall (99%).  
- **High-Risk Loans**: Lower precision (85%) and recall (91%).  
- Overall accuracy is 99%, with a minor misclassification rate for healthy loans.

### Observations
- The imbalance in the dataset (more healthy loans than high-risk loans) causes the model to prioritize the majority class.
- High accuracy for healthy loans but reduced performance for high-risk loans.

## Recommendations
To improve model performance for high-risk loans:
- Apply oversampling techniques to balance the dataset.
- Emphasize accurate identification of high-risk loans to mitigate credit risks and inform lending strategies.
