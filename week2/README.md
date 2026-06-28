# week2_Tesla-ML-Pipeline
# Tesla End-to-End ML Pipeline

This project implements an end-to-end Machine Learning pipeline using Tesla deliveries and production dataset data from 2015–2025.

The main objective of the project is to predict `Estimated_Deliveries` using production, pricing, battery, and regional features while understanding delivery trends through data analysis and visualization.

---

## Dataset

Dataset Source:  
https://www.kaggle.com/datasets/nalisha/tesla-ea-deliveries-and-production-data20152025

---

## Project Workflow

The following ML workflow was implemented in this project:

- Data Loading
- Dataset Inspection
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Correlation Analysis
- Feature Encoding
- Train-Test Split
- Feature Scaling
- Linear Regression Model
- Random Forest Regressor
- Hyperparameter Tuning
- Trend Analysis and Forecasting Insights
- Model Evaluation

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Models Used

### Linear Regression
Used as the baseline regression model for predicting `Estimated_Deliveries`.

### Random Forest Regressor
Used for advanced regression modeling and performance comparison.

---

## Evaluation Metrics

The following regression metrics were used:

- MAE (Mean Absolute Error)
- MSE (Mean Squared Error)
- RMSE (Root Mean Squared Error)
- R² Score

---

## Results

- Linear Regression achieved the best overall performance on this dataset.
- Strong relationships were observed between `Production_Units` and `Estimated_Deliveries`.
- Trend analysis showed fluctuations in Tesla deliveries over different years.

---

## Conclusion

This project helped in understanding the complete machine learning workflow from preprocessing and visualization to model training, evaluation, and trend analysis.

The project also demonstrated how regression models can be used to predict delivery-related business metrics using historical production and sales data.

---

## Author

Pavika Yadav
B.Tech CSE (Data Science)
Amity University
