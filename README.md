# Churn Analysis Project

## Overview
This project focuses on analyzing customer churn and building predictive models to identify potential churners. It includes a dataset, modeling scripts, and visual documentation.

## Files in the Repository

### 1. Dataset
- **`churn-bigml.csv`**: The dataset used for training and evaluating churn prediction models. It contains features related to customer behavior and demographics.

### 2. Notebook
- **`KDD_Models.ipynb`**: A Jupyter Notebook implementing machine learning models for churn prediction. It includes:
  - Data preprocessing steps
  - Exploratory data analysis (EDA)
  - Model training and evaluation
  - Performance metrics and results

### 3. Visual Documentation
- **`Screenshot 2024-12-08 at 3.43.25 PM.png`**: A visualization or screenshot related to the project. This could be an important result or UI component.

## Data Analysis and Insights
- **Initial Dataset Imbalance**: The raw dataset showed a significant imbalance in the target variable `Churn`. SMOTE was applied to handle this and create a balanced training set.
- **Feature Engineering**: Categorical variables like `State`, `International plan`, and `Voice mail plan` were one-hot encoded to prepare the data for machine learning models.
- **Scaling**: Features were scaled using StandardScaler to ensure models with distance-based algorithms (e.g., SVM, KNN) perform optimally.

## Models and Results
The following machine learning models were trained and evaluated. GridSearchCV was used for hyperparameter tuning where applicable:

| Model                     | Accuracy | Precision | Recall | F1-Score |
|---------------------------|----------|-----------|--------|----------|
| Logistic Regression       | 89%      | 0.88      | 0.89   | 0.88     |
| Random Forest             | 92%      | 0.91      | 0.92   | 0.91     |
| SVM                       | 90%      | 0.89      | 0.90   | 0.89     |
| KNN                       | 88%      | 0.87      | 0.88   | 0.87     |
| Naive Bayes               | 84%      | 0.83      | 0.84   | 0.83     |
| Decision Tree             | 85%      | 0.84      | 0.85   | 0.84     |
| Gradient Boosting         | 91%      | 0.90      | 0.91   | 0.90     |
| Artificial Neural Network | 93%      | 0.92      | 0.93   | 0.92     |
| CART                      | 85%      | 0.84      | 0.85   | 0.84     |
| C5.0                      | 86%      | 0.85      | 0.86   | 0.85     |
| Random Forest (Tuned)     | 94%      | 0.93      | 0.94   | 0.93     |
| XGBoost (Tuned)           | 95%      | 0.94      | 0.95   | 0.94     |

### Key Takeaways
- **Best Model:** The tuned XGBoost classifier achieved the highest accuracy of 95%, with an F1-score of 0.94, making it the most effective model for this dataset.
- **Feature Importance:** Random Forest and XGBoost provided insights into the most important features contributing to churn prediction.

## How to Use

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Open the Jupyter Notebook to explore and execute the code:
   ```bash
   jupyter notebook KDD_Models.ipynb
   ```

3. Ensure all dependencies are installed:
   ```bash
   pip install -r requirements.txt
   ```

4. Use the dataset `churn-bigml.csv` to train or test models.

## Requirements
- Python 3.8+
- Jupyter Notebook
- Libraries:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib
  - seaborn
  - imbalanced-learn
  - xgboost

## Results
The project demonstrates the effectiveness of machine learning models in predicting customer churn. For detailed results and metrics, refer to `KDD_Models.ipynb`.

## Acknowledgments
This project leverages open-source tools and datasets to analyze and predict customer churn. Special thanks to the creators of the dataset and tools used.

