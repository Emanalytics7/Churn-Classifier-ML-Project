

# PowerCo Churn Prediction

## **Overview**

This repository contains the code for PowerCo's customer churn prediction project. As a major gas and electricity utility, PowerCo is facing challenges with customer retention in the competitive energy market. The primary goal is to understand and address customer churn, with a focus on evaluating the hypothesis that price sensitivity is a significant driver.

## **Key Objectives**

- Analyze customer data, churn data, and historical pricing data.
- Define and calculate price sensitivity.
- Engineer features and prepare the data for analysis.
- Build and test binary classification models (Random Forest Classifier).
- Evaluate model performance based on complexity, explainability, and accuracy.
- Extrapolate the impact of price sensitivity on customer churn.
  
## **Hypothesis**
`Price Sensitivity is the primary influencer of customer churn.` The analysis aims to quantify the extent to which price sensitivity contributes to customer attrition.

## Analysis
![image](https://github.com/user-attachments/assets/7640e7e4-6e11-4390-a7b1-9e0f0712cb0f)


## Results

- **Churners in Test Set**: About 10% of the rows are churners (churn = 1).

- **True Negatives**: We have 3284 out of 3286 true negatives. This means that out of all the negative cases (churn = 0), we predicted 3284 as negative. This is great!

- **False Negatives**: Here, we predicted a client not to churn (churn = 0) when in fact they did churn (churn = 1). The number is quite high at 349. We want to reduce false negatives to as close to 0 as possible, so this will need to be addressed when improving the model.

- **False Positives**: We predicted a client to churn when they actually didn't churn. There are only 2 such cases, which is great!

- **True Positives**: We correctly identified 17 out of 366 clients who churned in the test dataset. This is very poor.

- **Accuracy Score**: The accuracy score is high, but this can be misleading. Precision and recall are much more informative in this case.

- **Precision Score**: The precision score is 0.89, which is not bad.

- **Recall Score**: The recall score shows that the classifier has a very poor ability to identify positive samples (clients who churn). This is the main area of concern for improving the model.

### Conclusion

Overall, we’re able to very accurately identify clients who do not churn, but we struggle with predicting clients who actually do churn. A high percentage of clients are being identified as not churning when they should be. This suggests that the current set of features is not discriminative enough to clearly distinguish between churners and non-churners.
