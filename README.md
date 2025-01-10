# 2020-US-Election-Vote-Share-Prediction

### Overview

This project analyzes the United States 2020 presidential election data using machine learning techniques to understand voting patterns and demographic relationships. The analysis includes data preprocessing, feature engineering, model training, and visualization of various electoral trends.

### Objectives

- Predict the Democratic vote share percentage at the county level using machine learning models.
- Analyze the relationships between demographic, economic, and occupational factors and voting patterns.
- Provide visual insights into voting trends and demographic distributions.

### Dataset

The dataset contains the following columns:

- Vote counts and percentages for Democratic, Republican, and other parties
- Demographic information
- Economic indicators
- Educational statistics
- Occupational data
- Geographic data

### Feature Engineering

- Vote share calculations
- Total votes computation
- Party percentage calculations
- Vote share difference analysis

### Data Preprocessing Steps

- Missing value handling
- Outlier detection and capping
- Feature scaling and normalization
- PCA dimensionality reduction

### Data Visualization

This project includes various visualizations to explore and explain the data:

- Boxplots: Vote share by state for Democratic and Republican candidates.
- Scatter Plots: Actual vs. Predicted vote shares for each model.
- Heatmaps: Correlations between county demographics, economic factors, and voting outcomes.
- Histograms: Distribution of vote percentages across counties.
        
### Model Training and Evaluation

Models Implemented
- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regressor

### Model Performance

The Random Forest model achieved an average cross-validation R² score of 0.9577.

### Performance Summary

- Linear Regression and Ridge Regression performed exceptionally well with an R² score of ~0.995, indicating very high predictive power.
- Lasso Regression struggled with higher errors due to regularization.
- Random Forest Regressor showed robust performance with an R² score of ~0.954 on the test set and ~0.9434 on cross-validation.

### Key Insights

- Income and Education: Counties with higher median income and advanced educational attainment showed stronger Democratic support.
- Racial Composition: Counties with higher percentages of NH-White population leaned Republican, while counties with diverse racial compositions showed more Democratic support.
- Occupational Distribution: Areas with a higher proportion of management and arts occupations tended to favor Democrats.

### Source

https://www.kaggle.com/datasets/essarabi/ultimate-us-election-dataset
