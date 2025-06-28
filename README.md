
 Real Estate Price Prediction in Saudi Arabia
This project predicts price per square meter of real estate properties in Saudi Arabia using various machine learning models. It includes data preprocessing, model training, hyperparameter tuning.

📊 Dataset Overview
The dataset includes:

City & Region in Arabic (mapped to English)

Property Type (Residential, Commercial, Agricultural)

Price, Area, Price per sqm

Date of transaction (Gregorian & Hijri)

 Data Preprocessing
 Renamed columns from Arabic to English

 Mapped regions and cities from Arabic to English

 Cleaned area and price fields

 Filtered outliers:

Area between 50 sqm and 2000 sqm

Price between 50,000 SAR and 5,000,000 SAR

 Created price_per_sqm and log_price_per_sqm

 Models Trained
Model	R² Score
Ridge Regression	0.5381
Random Forest	0.6181
XGBoost	0.6374
LightGBM	0.6378
CatBoost	0.6170
MLPRegressor	0.3501

XGBoost and LightGBM performed best.

 Hyperparameter Tuning
 GridSearchCV for XGBoost

 RandomizedSearchCV

 Optuna (best result: R² = 0.63695)

Best XGBoost params:
{
  "n_estimators": 208,
  "max_depth": 8,
  "learning_rate": 0.0635
}
 Final Model
Model	MAE (SAR/sqm)	R² Score
XGBoost	808.17	0.4469
Ensemble	808.78	0.4470

Models saved as .joblib files.


 Future Work

Build  dashboard

Include satellite or building age features


