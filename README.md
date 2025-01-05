## Predicting-Heart-Disease

## Introduction
Cardiovascular diseases (CVDs) are the leading cause of death globally, claiming 17.9 million lives annually (WHO).
This project aims to develop a predictive model using patient health attributes to assess the likelihood of heart disease.
A K-Nearest Neighbors (k-NN) classifier is implemented to identify high-risk individuals based on historical data.
## Exploratory Data Analysis (EDA)
## Dataset Overview:
Attributes include Age, Sex, ChestPainType, Cholesterol, RestingBP, ExerciseAngina, MaxHR, and HeartDisease (target).
Numerical and categorical variables were explored to understand data distribution and correlations.
## Key Insights:
Strong correlations with HeartDisease:
Oldpeak (ST depression)
MaxHR (Maximum heart rate achieved)
ExerciseAngina_Y (Exercise-induced angina)
ST_Slope_Flat and ST_Slope_Up (Slope of ST segment during exercise).
Cholesterol showed weak correlation with heart disease, contrary to common assumptions.
## Preprocessing
## Feature Scaling:
MinMaxScaler was used to normalize features to a range of [0, 1].
Feature Selection:
Selected features based on EDA and correlation analysis:
Oldpeak
Sex_M (Male)
ExerciseAngina_Y
ST_Slope_Flat
ST_Slope_Up
## Train-Test Split:
Dataset split into training (85%) and testing (15%) sets using a random state of 417 for reproducibility.

## Modeling
## Baseline Model:
Built a k-NN model with k=3 and evaluated performance using individual features.
## Hyperparameter Tuning:
GridSearchCV was employed to find optimal hyperparameters:
Search space:
Number of neighbors (k): 1–20.
Distance metrics: minkowski (Euclidean distance) and manhattan (City block distance).
## Best Parameters:
k: Optimal value identified via cross-validation.
Distance metric: Metric with highest validation accuracy.
Tuning improved model performance significantly by balancing bias and variance.
## Evaluation:
## Test Set Results:
Predictions made using the tuned k-NN model on scaled test data.
## Metrics:
Accuracy: [Reported value in percentage].
Confusion matrix and classification reports were generated to assess performance on positive and negative cases.

## Conclusions
The k-NN model, optimized through hyperparameter tuning, proved effective for predicting heart disease risk.
## Key takeaways:
Early identification of high-risk features like Oldpeak and ExerciseAngina_Y can assist in proactive healthcare interventions.
Hyperparameter tuning demonstrated the importance of optimizing k and distance metrics for best results.
