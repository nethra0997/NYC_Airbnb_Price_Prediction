# NYC_Airbnb_Price_Prediction

## Overview
This project aims to predict the prices of Airbnb listings in New York City using various data mining and machine learning techniques. By analyzing key features and parameters that influence the costs of listings, we aim to build a robust predictive model that can accurately forecast Airbnb prices.

## Objective
The primary objective of this project is to identify the features that most significantly impact Airbnb listing prices in NYC and to improve the prediction accuracy of the model through data analysis, feature selection, and machine learning.

## Data Source
The dataset used in this project is publicly available on the [Inside Airbnb website](http://insideairbnb.com/new-york-city). 
We combined data from three files: `listings.csv`, `neighborhood.csv`, and `reviews.csv`.

## Data Description
The final dataset consists of 25,740 rows and 75 columns, including numerical values, categorical data, and date columns. The key features include room type, review scores, number of bedrooms, and location details.

## Data Exploration and Cleaning
1. **Data Cleaning Steps:**
   - Dropped redundant columns such as URLs.
   - Removed rows with more than 35% missing values.
   - Handled outliers in the target variable by dropping extreme values.
   - Imputed missing values using the median of the column.

2. **Visualizations:**
   - **Correlation Heatmap:** Shows the correlation between variables.
   - **Scatter Plot:** Represents clusters of neighborhoods hosting listings.
   - **Review Score Distribution Plot:** Illustrates the distribution of review scores.
   - **Distribution of Significant Feature Variables:** Provides insights into bedroom counts, guest accommodations, and bed numbers.
   - **Stacked Bar Chart:** Represents room types grouped by neighborhood.
   - **Box Plot for Availability:** Displays availability outliers for different neighborhoods.
   - **Location Map:** Shows top 15 places with the highest ratings.

## Data Mining Tasks and Models
1. **Dimension Reduction and Variable Selection:**
   - Dropped highly correlated columns.
   - Performed ANOVA tests to identify significant features.
   - Applied label encoding for categorical variables.

2. **Model Exploration:**
   - Tested several models including Linear Regression, Lasso, Ridge, SVR, RandomForestRegressor, DecisionTreeRegressor, and XGBRegressor.

3. **Model Performance Evaluation:**
   - Evaluated models using RMSE, R-squared, MAE, and MSE metrics.
   - Implemented k-fold cross-validation to estimate model performance.

4. **Final Model Selection:**
   - Chose RandomForestRegressor as the final model due to its superior performance and lower complexity.

## Key Findings
- **Feature Importance:** Room type, review scores, and number of bedrooms were among the most significant factors affecting prices.
- **Model Performance:** RandomForestRegressor and XGBRegressor showed the best performance, with RandomForestRegressor being selected for its simplicity.

## Hyperparameter Tuning
- Optimized hyperparameters for the RandomForestRegressor to further improve performance.
- Achieved an R-squared of approximately 83%, normalized RMSE of 0.079, MAE of 27.6, and MSE of 1543.

## Conclusion
This project successfully built a predictive model for Airbnb prices in NYC, with RandomForestRegressor emerging as the best-performing model. The extensive data cleaning, feature selection, and model evaluation processes ensured robust predictions and valuable insights into the factors influencing Airbnb listing prices.

## Tech Stack
- **Programming Language:** Python
- **Libraries and Frameworks:**
  - **Pandas:** Data manipulation and analysis
  - **NumPy:** Numerical computing
  - **Scikit-Learn:** Machine learning models and evaluation
  - **XGBoost:** Gradient boosting framework
  - **Matplotlib and Seaborn:** Data visualization
  - **Statsmodels:** Statistical modeling
- **Tools:**
  - **Jupyter Notebook:** Development environment
  - **Git:** Version control
  - **Excel:** Initial data exploration
