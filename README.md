# Kickstarter Project Success Prediction

This project aims to predict the success or failure of **Kickstarter crowdfunding projects** using machine learning. It leverages **PySpark**, a powerful distributed computing framework, for large-scale data processing and applies two machine learning models: **Logistic Regression** and **Random Forest**.

## Project Overview

Crowdfunding platforms like **Kickstarter** allow creators to bring their ideas to life by securing funding from backers. Predicting the success or failure of these projects can offer valuable insights to both creators and backers. This project explores how machine learning, specifically using **PySpark**, can help make these predictions based on a variety of campaign features.

## Dataset

The dataset used in this project is from Kaggle, containing information about Kickstarter projects, such as:

- **Funding goal**
- **Pledged amount**
- **Backers**
- **Project duration**
- **Category** of the project
- **Country** of origin
- **State** (successful, failed, etc.)

This dataset provides detailed campaign data for over 370,000 Kickstarter projects and serves as the foundation for predicting project success.

## Methodology

### 1. Data Preprocessing:
- Cleaned and transformed raw data, ensuring proper data types for each feature.
- Handled missing data and outliers to improve model performance.

### 2. Feature Engineering:
- Extracted key features like **completion percentage** and **days allotted**.
- Created new features to better represent the dataset for the models.

### 3. Model Development:
Two models were implemented and evaluated:
- **Logistic Regression**: A simple baseline model for binary classification (success vs. failure).
- **Random Forest**: A more complex model capable of handling non-linear relationships between features.

### 4. Model Evaluation:
- Used **ROC AUC** and **accuracy** metrics to evaluate model performance.
- Applied **cross-validation** and **regularization** to combat overfitting and ensure generalizability.

## Results

- **Logistic Regression**: 
  - Initial ROC AUC: 0.9999
  - After 3-fold cross-validation, ROC AUC: 0.9344
  - After 5-fold cross-validation, ROC AUC: 0.9999
  - Regularization did not result in significant improvements.

- **Random Forest**:
  - ROC AUC: 0.99997
  - Accuracy: 0.99998

The **Random Forest** model outperformed the Logistic Regression model, demonstrating a better ability to distinguish between successful and failed projects.

## Key Insights
- **Overfitting**: Both models performed exceptionally well, but there was evidence of overfitting. The models were highly tuned to the training data, suggesting that the features may be overly simplistic or not varied enough.
- **Feature Importance**: Despite high accuracy, further analysis indicated that the dataset might lack sufficient complexity to make meaningful predictions. More informative features or a more diverse dataset could improve results.

## Installation & Setup

To run this project locally:

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/Kickstarter-Project-Success-Prediction.git
