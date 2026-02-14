# Rusty Bargain Used Car Price Prediction Project

### Problem Context:
Development of a machine learning system for Rusty Bargain used car service to predict market values of vehicles based on historical data including technical specifications, trim levels, and prices, enabling rapid price estimation for customers.

### Objective:
Build regression models to determine car market values focusing on three key criteria: prediction quality, prediction speed, and training time optimization.

Technical Competencies Used:
Exploratory Data Analysis (EDA):
- Investigation of 354,369 car records with 16 features
- Data quality assessment identifying outliers (Power values up to 20,000 HP)
- Missing value analysis across categorical variables
- Statistical analysis of price, power, and mileage distributions

Data Preprocessing:
- Outlier treatment (Power values >1500 replaced with median)
- Date conversion (DateCrawled, DateCreated, LastSeen to year format)
- Missing value imputation with 'Unknown' for categorical variables
- One-hot encoding optimization (applied only to categorical columns to reduce dimensionality from 874 to 317 columns)

Machine Learning Model Development:
- Linear Regression: Baseline model with analytical solution
- Random Forest Regressor: Hyperparameter optimization (max_depth, n_estimators)
- LightGBM: Advanced gradient boosting with parameter tuning (num_leaves, num_rounds)
- XGBoost: Gradient boosting with regularization parameters
- CatBoost: Automated categorical feature handling with iterations optimization

Model Optimization:
- Systematic hyperparameter tuning across all models
- Performance comparison using RMSE, MSE, and R² metrics
- Training time analysis for production deployment considerations

### Main Libraries:
- pandas: Data manipulation and preprocessing
- numpy: Numerical operations and array handling
- scikit-learn: Linear Regression, Random Forest, evaluation metrics
- lightgbm: Advanced gradient boosting algorithm
- xgboost: Extreme gradient boosting implementation
- catboost: Categorical boosting with automated feature handling

### Final Results:
Successful development of high-performance car price prediction system:

Model Performance Comparison:
- Linear Regression: RMSE = 3,032.83, R² = 0.55, Training time = 9.23s
- Random Forest: RMSE = 1,800.61, R² = 0.84, Training time = 36.1s
- LightGBM: RMSE = 1,691.67, Training time = 17.3s
- XGBoost: RMSE = 1,898.16, Training time = 2min 30s
- CatBoost: RMSE = 1,754.32, R² = 0.85, Training time = 17.1s

Best Model Selection:
- LightGBM identified as optimal solution
- Lowest RMSE: 1,691.67 with excellent prediction accuracy
- Fast training time: 17.3 seconds for production deployment
- Balanced performance: Superior accuracy with computational efficiency

Business Impact:
- Enables rapid car price estimation for customer applications
- Supports automated valuation with 84%+ accuracy
- Provides scalable solution for high-volume price predictions
- Facilitates competitive pricing strategies in used car market
