# Predictive-modelling-of-house-prices
This project would help to develop a robust machine learning model that can predict house prices based on various features of the houses and solve the problem mentioned earlier.
## Methodology

### Data Collection
The dataset used for this project is titled "Housing Sales: Factors Influencing Sale Prices" from Kaggle. It includes 18 features and 2,413 observations, detailing property attributes such as lot size, building type, house style, and sale prices. This data was ideal for analyzing real estate market trends and developing predictive models.

### Data Cleaning
1. **Typographical Error Correction:** Verified and corrected categorical and numerical features to ensure data integrity.
2. **Numerical Feature Validation:** Checked for unusual characters in numerical features, confirming data cleanliness.
3. **Handling "Year Built":** Chose not to convert "Year Built" to datetime, considering it more meaningful as an integer.
4. **Outlier Analysis:** Identified and handled 561 outliers, creating two datasets: one with outliers (`df`) and one without (`df2_without_outliers`) to compare model performance.

### Exploratory Data Analysis (EDA)
1. **Non-Graphical and Graphical Univariate Analysis:** Explored frequency distributions, statistical summaries, histograms, and boxplots.
2. **Non-Graphical and Graphical Multivariate Analysis:** Investigated relationships between features and the target variable, using correlation analysis, groupby, ANOVA, pairplots, and heatmaps.
3. **Key Outcome:** Gained insights into feature distributions and their impact on the target variable, informing feature selection for modeling.

### Feature Engineering and Selection
New features, such as house age and decade built, were created to enhance model performance. Features were selected based on their effect on the target variable, resulting in three datasets for machine learning:
1. `training_ml_df`: Training set with outliers.
2. `test_ml_df`: Test set with outliers.
3. `df2_without_outliers_ml`: Dataset without outliers.

### Machine Learning
Three models were trained and tested on the datasets, both with and without outliers:
1. **Linear Regression:** Chosen for its simplicity, interpretability, and efficiency.
2. **Random Forest Regressor:** Selected for handling non-linearity, providing feature importance, and robustness.
3. **XGBoost Regressor:** Preferred for its high performance, ability to handle large datasets, and feature engineering capabilities.

All models were evaluated using Root Mean Square Error (RMSE), Mean Squared Error (MSE), and R² scores. Visual evaluations included scatter plots and bar charts to assess model performance.


## Conclusion
The project successfully developed and evaluated multiple machine learning models for predicting house prices, offering a robust tool for stakeholders in the real estate market. The final model, selected based on evaluation metrics, provides accurate and reliable price predictions, helping to better understand the factors influencing property values.

The XGBoost Regressor emerged as the best performer in our analysis, particularly when trained on the dataset without outliers. This model demonstrated significantly lower errors, as indicated by the Mean Squared Error (MSE) and Root Mean Squared Error (RMSE), and exhibited superior explanatory power with a higher R-squared (R²) value.

The impact of outliers on model performance was substantial. Generally, removing outliers led to improved performance across all models. However, the most notable enhancement was observed in the XGBoost model, highlighting its sensitivity to outliers and its ability to benefit greatly from their removal.
In terms of model robustness, both the Random Forest and XGBoost models showed greater resilience to outliers compared to Linear Regression. Despite this, all models experienced performance gains when outliers were removed, underscoring the importance of outlier management in achieving accurate predictions.
