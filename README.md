

## Comparing Classifiers Notebook

### Overview

This notebook focuses on a practical application of comparing the performance of several classifiers, including:
- K Nearest Neighbor (KNN)
- Logistic Regression (LogReg)
- Decision Trees (DT)
- Support Vector Machines (SVM)
- Naive Bayes (NB)

The data used is related to marketing bank products over the telephone and is sourced from the UCI Machine Learning repository. The dataset contains results from multiple marketing campaigns conducted by a Portuguese banking institution.

### Contents

1. **Understanding the Data**  
   - Dive deep into the data by reading the information provided in the UCI repository.
   - Understand the context and details of the marketing campaigns.

2. **Data Loading and Exploration**  
   - Read the dataset `bank-additional-full.csv` using pandas.
   - Understand the features, including their data types and potential missing values.

3. **Model Comparison**  
   - Train models with their default values and compare their performances.
   - Utilize GridSearchCV for hyperparameter tuning and observe the changes in model performance.
   
4. **Hyperparameters**  
   - Detailed list of hyperparameters used for tuning each classifier.

### Results

#### Performance with Default Parameters

| Model   | Train Time (sec) | Train Accuracy | Test Accuracy |
|---------|------------------|----------------|---------------|
| LogReg  | 0.091            | 0.799          | 0.814         |
| KNN     | 0.020            | 0.817          | 0.768         |
| DT      | 0.052            | 0.900          | 0.657         |
| SVM     | 6.358            | 0.802          | 0.814         |
| NB      | 0.027            | 0.330          | 0.322         |

#### Performance with Hyperparameter Tuning (GridSearchCV)

| Model   | Train Time (sec) | Train Accuracy | Test Accuracy | Best Estimator |
|---------|------------------|----------------|---------------|----------------|
| LogReg  | 2.965            | 0.799          | 0.814         | {'LogReg__C': 1, 'LogReg__solver': 'newton-cg'} |
| KNN     | 2.801            | 0.830          | 0.735         | {'KNN__metric': 'euclidean', ...} |
| DT      | 0.288            | 0.810          | 0.797         | {'DT__max_depth': 10, 'DT__max_features': 'sqrt'} |
| SVM     | 15.545           | 0.721          | 0.726         | {'SVM__C': 1, 'SVM__kernel': 'sigmoid'} |

---

