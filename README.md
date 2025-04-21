# ml_regression_trentrueckert

## Links
Notebook: https://github.com/trentrueckert/ml_regression_trentrueckert/blob/main/regression_trentrueckert.ipynb
Peer review: https://github.com/trentrueckert/ml_regression_trentrueckert/blob/main/peer_review.md

## Preliminary Project Setup

### Step 1 - Initial Setup
1. Click "New Repository"
* Generate name with no spaces
* Add a "README.md"

2. Clone Repository to machine via VS Code
* Create folder in "C:\Projects"

3. Install requirements.txt
4. Setup .gitignore file

### Step 2 - Create Project Virtual Environment

```
py -m venv .venv
.venv\Scripts\Activate
py -m pip install --upgrade pip 
py -m pip install -r requirements.txt
```

### Step 3 - Git add, commit, and push

```
git add .
git commit -m "Commit Example"
git push -u origin main
```

## Overview
In this notebook, I will analyze the Medical Costs Dataset to predict insurance charges by preparing/exploring the data, cleaning the data/handling missing values, performing feature engineering, and training machine learning models based on different selected features. More specifically, I will be using various regression models to provide insights on which features most impact insurances charges. My focus will be on the features: age, BMI, and smoker.

## Section 1. Import and Inspect the Data
* 1.1 Load the dataset and display the first 10 rows
* 1.2 Check for missing values and display summary statistics
* Reflection 1: What do you notice about the dataset? Are there any data issues?

## Section 2. Data Exploration and Preparation
* 2.1 Explore data patterns and distributions
  * Create histograms, boxplots, and count plots for categorical variables (as applicable).
  * Identify patterns, outliers, and anomalies in feature distributions.
  * Check for class imbalance in the target variable (as applicable).
* 2.2 Handle missing values and clean data
  * Impute or drop missing values (as applicable).
  * Remove or transform outliers (as applicable).
  * Convert categorical data to numerical format using encoding (as applicable).
* 2.3 Feature selection and engineering
  * Create new features (as applicable).
  * Transform or combine existing features to improve model performance (as applicable).
  * Scale or normalize data (as applicable).
* Reflection 2: What patterns or anomalies do you see? Do any features stand out? What preprocessing steps were necessary to clean and improve the data? Did you create or modify any features to improve performance?

## Section 3. Feature Selection and Justification
* 3.1 Choose features and target
  * Select two or more input features (numerical for regression, numerical and/or categorical for classification)
  * Select a target variable (as applicable)
    * Regression: Continuous target variable (e.g., price, temperature).
    * Classification: Categorical target variable (e.g., gender, species).
    * Clustering: No target variable.
    * Justify your selection with reasoning.
* 3.2 Define X and y
  * Assign input features to X
  * Assign target variable to y (as applicable)
* Reflection 3: Why did you choose these features? How might they impact predictions or accuracy?
  
## Section 4. Train a Model (Linear Regression)
* 4.1 Split the data into training and test sets using train_test_split
* 4.2 Train model using Scikit-Learn model.fit() method
* 4.3 Evalulate performance, for example:
  * Regression: R^2, MAE, RMSE (RMSE has been recently updated)
  * Classification: Accuracy, Precision, Recall, F1-score, Confusion Matrix
  * Clustering: Inertia, Silhouette Score
* Reflection 4: How well did the model perform? Any surprises in the results?

## Section 5. Improve the Model or Try Alternates (Implement Pipelines)
* 5.1 Implement Pipeline 1: Imputer → StandardScaler → Linear Regression
* 5.2 Implement Pipeline 2: Imputer → Polynomial Features (degree=3) → StandardScaler → Linear Regression
* 5.3 Compare performance of all models across the same performance metrics
* Reflection 5: Which models performed better? How does scaling impact results?

## Section 6. Final Thoughts & Insights
* 6.1 Summarize findings
* 6.2 Discuss challenges faced
* 6.3 If you had more time, what would you try next?
* Reflection 6: What did you learn from this project?