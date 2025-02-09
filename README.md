# Breast-Cancer-Detection
This repository focus on Breast cancer detection using different ML models. In total 7 models are used and RandomizedSearchCV for Hyper Parameter Tuning. The Dataset has been used which is available at UCI.

# Model Performance Comparison

This repository contains a comparison of multiple machine learning models trained on the Breast Cancer Wisconsin dataset. The models were evaluated using k-fold cross-validation and hyperparameter tuning to select the best-performing model.

## Overview
Seven models were trained and evaluated:

1. **SVM (Support Vector Machine)**
2. **Random Forest**
3. **Logistic Regression**
4. **XGBoost**
5. **LightGBM**
6. **CatBoost**
7. **Neural Network (MLP)**

The best model was selected based on validation accuracy and generalization performance on the test dataset.

## Results Summary
| Model                 | Best Validation Accuracy | Test Accuracy |
|-----------------------|--------------------------|---------------|
| **SVM**              | 97.58%                  | **98.25%**    |
| **Random Forest**     | 96.26%                  | 95.61%        |
| **Logistic Regression** | **98.24%**             | **97.37%**    |
| **XGBoost**           | 97.14%                  | 95.61%        |
| **LightGBM**          | 96.92%                  | 95.61%        |
| **CatBoost**          | 97.36%                  | 95.61%        |
| **Neural Network (MLP)** | 98.02%                | 96.49%        |

### Best Model: Logistic Regression
- Logistic Regression was chosen as the best model with a validation accuracy of **98.24%** and a test accuracy of **97.37%**.
- SVM had the highest test accuracy (**98.25%**), but Logistic Regression had a higher validation accuracy, ensuring better generalization.

## Visualizations
Below are the visualizations of the model performances:

### 1. Model Accuracy Trends (Line Plot)
![Model Accuracy Trends](Model%20Accuracy%20Trends%20(Line%20Plot).png)

### 2. Accuracy Distribution (Box Plot)
![Accuracy Distribution](Accuracy%20Distribution%20(Box%20Plot).png)

### 3. Validation vs Test Accuracy (Scatter Plot)
![Validation vs Test Accuracy](Model%20Performance%20(Scatter%20Plot).png)

### 4. Validation vs Test Accuracy (Bar Chart)
![Validation vs Test Accuracy](Validation%20vs%20Test%20Accuracy%20(Bar%20Chart).png)

## Methodology
1. **Dataset:** The Breast Cancer Wisconsin dataset was loaded using `sklearn.datasets`.
2. **Preprocessing:**
   - The data was split into 80% training and 20% testing.
   - Features were scaled using `StandardScaler` for models like Logistic Regression and SVM.
3. **Model Training:**
   - Each model was tuned using `RandomizedSearchCV` with 5-fold cross-validation.
   - The best hyperparameters were selected for each model.
4. **Evaluation:**
   - Validation accuracy was computed during cross-validation.
   - Test accuracy was computed on the unseen test dataset.

## Conclusion
Logistic Regression proved to be the best-performing model due to its high validation accuracy and generalization performance. SVM was a close contender with the highest test accuracy.

## Repository Contents
- Python scripts for training and evaluating models.
- Saved charts for model comparison.
- This README file for project documentation.

## Usage
1. Clone this repository.
2. Run the Python scripts to reproduce the results.
3. View the charts to understand model performance.
