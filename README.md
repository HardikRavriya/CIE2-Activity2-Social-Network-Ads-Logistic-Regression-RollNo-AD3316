# CIE2-Activity2-Social-Network-Ads-Logistic-Regression-RollNo.-AD2316
Binary classification using Logistic Regression to predict customer purchasing behaviour based on age and estimated salary. CIE-2 Activity 2 – Regression and Classification Algorithms (Unit II).

# Social Network Ads Purchase Prediction Using Logistic Regression

## CIE-2 Activity 2: Binary Classification Activity

**Subject:** Regression and Classification Algorithms (RCA)  
**Unit:** Unit II – Classification and Logistic Regression  
**Roll Number:** AD3316

## 1. Project Overview

This project implements a Logistic Regression model to predict whether a customer will purchase a product advertised on social media based on age and estimated salary.

The objective is to help the marketing team identify potential customers and improve advertising efficiency.

## 2. Dataset

- **Dataset Name:** Social Network Ads
- **Source:** Kaggle
- **File Format:** CSV
- **Total Records:** 400
- **Total Columns:** 5

[Dataset Source – Social Network Ads](https://www.kaggle.com/datasets/akram24/social-network-ads)

### Dataset Description

| Column | Description |
|---|---|
| User ID | Unique customer identifier |
| Gender | Gender of the customer |
| Age | Age of the customer |
| EstimatedSalary | Estimated salary of the customer |
| Purchased | Purchase status (0 or 1) |

### Input Features

- Age
- EstimatedSalary

### Target Variable

- Purchased
  - 0: Not Purchased
  - 1: Purchased

User ID is excluded because it is an identifier. Gender is excluded to keep the model simple and avoid directly using gender in advertising decisions.

## 3. Technologies and Libraries Used

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## 4. Methodology

1. Import required libraries.
2. Load and inspect the dataset.
3. Check missing values and duplicate records.
4. Perform exploratory data analysis.
5. Select input features and target variable.
6. Perform stratified train-test splitting (80:20).
7. Visualise the sigmoid function.
8. Apply feature scaling using StandardScaler.
9. Train the Logistic Regression model.
10. Generate predicted classes and probabilities.
11. Evaluate model performance using classification metrics.
12. Compare the model with a majority-class baseline.
13. Analyse different decision thresholds.
14. Compare training and testing performance.
15. Visualise the decision boundary.
16. Predict purchasing behaviour for a new customer.

## 5. Model Evaluation Results

| Evaluation Metric | Score |
|---|---:|
| Accuracy | 0.8375 |
| Precision | 0.8636 |
| Recall | 0.6552 |
| Specificity | 0.9412 |
| F1-score | 0.7451 |
| ROC-AUC | 0.9053 |

### Confusion Matrix

| Actual / Predicted | Not Purchased | Purchased |
|---|---:|---:|
| Not Purchased | 48 | 3 |
| Purchased | 10 | 19 |

### Baseline Comparison

| Model | Accuracy |
|---|---:|
| Majority-Class Baseline | 63.75% |
| Logistic Regression | 83.75% |

The Logistic Regression model improves accuracy by 20 percentage points compared to the majority-class baseline.

## 6. Decision Threshold Comparison

| Threshold | Predicted Positive | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|---:|
| 0.3 | 38 | 0.7875 | 0.6579 | 0.8621 | 0.7463 |
| 0.5 | 22 | 0.8375 | 0.8636 | 0.6552 | 0.7451 |
| 0.7 | 14 | 0.7875 | 0.9286 | 0.4483 | 0.6047 |

A threshold of 0.5 is recommended for this activity because it provides good overall accuracy and precision. Higher thresholds reduce false positives but may miss potential customers. The recommended threshold should be confirmed using validation data before real-world deployment.

## 7. Visualisations

- Class Distribution
- Age Distribution
- Estimated Salary Distribution
- Age vs Estimated Salary
- Sigmoid Function
- Confusion Matrix
- ROC Curve
- Logistic Regression Decision Boundary

## 8. New Customer Prediction

| Feature | Value |
|---|---:|
| Age | 35 |
| EstimatedSalary | 60000 |
| Predicted Class | 0 |
| Purchase Probability | 12.47% |

The model predicts that the customer is unlikely to purchase the product.

## 9. Conclusion

The Logistic Regression model achieved a testing accuracy of 83.75% and a ROC-AUC score of 0.9053. It performed better than the majority-class baseline and demonstrated its ability to classify customers based on age and estimated salary.

The model can support marketing decisions by identifying potential customers and reducing unnecessary targeting.

However, purchasing behaviour may also depend on other factors, such as customer interests, product price and advertising quality. The prediction is a probability-based estimate and not a guaranteed outcome.

## 10. How to Run the Project

1. Download or clone this repository.
2. Install the required Python libraries.
3. Place `Social_Network_Ads.csv` in the same directory as the notebook.
4. Open `Social_Network_Ads_Logistic_Regression.ipynb` in Jupyter Notebook or Google Colab.
5. Run all cells sequentially.

## 11. References

- [Kaggle – Social Network Ads Dataset](https://www.kaggle.com/datasets/akram24/social-network-ads)

## 12. Faculty GitHub Reference

[https://github.com/complexiota](https://github.com/complexiota)
