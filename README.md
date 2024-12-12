# 2020-US-Election-Vote-Share-Prediction

### Overview

This project analyzes the county-wise vote share from the 2020 United States presidential election using a dataset containing detailed county demographics, racial composition, income statistics, and occupational distributions. The project aims to predict the Democratic vote share percentage using machine learning models and gain insights into the factors influencing election outcomes.

### Objectives

- Predict the Democratic vote share percentage at the county level using machine learning models.
- Analyze the relationships between demographic, economic, and occupational factors and voting patterns.
- Provide visual insights into voting trends and demographic distributions.

### Dataset

The dataset contains the following columns:

- County: The county name.
- State: The state where the county is located.
- Population: Various population statistics (total, race, education level).
- Voting Data: The number of votes for the Democratic, Republican, and other parties.
- Vote Share: The percentage of votes for each party.

### Features

Election Data:
- 2020 Democrat vote raw and %
- 2020 Republican vote raw and %
- 2020 other vote raw and %

Demographics:
- Racial composition (e.g., Hispanic, White, Black, Asian percentages)
- Population size and density

Economic Factors:
- Median and mean income
- Income inequality (Gini Index)

Educational Attainment:
- Levels from "less than 9th grade" to "graduate or professional degree"

Occupational Distribution:
- Percentages of the population engaged in different job categories (e.g., management, sales, construction)

### Data Preprocessing Steps

Missing Values:
- Missing values were imputed using mean imputation for numerical columns to fill gaps in the dataset.

Handling Commas in Numeric Data:
- Columns with commas (such as 'Median income (dollars)' and 'Total Population') were cleaned, removing commas and converting to numeric data types.

 Outlier Detection and Capping:
 - Extreme outliers in the 'Median income (dollars)' column were capped to improve model stability.

 Feature Engineering:
 - New features were created to calculate vote shares for each party (Democratic, Republican, and Other).
 - A difference between the Democrat and Republican vote shares was also calculated.

 Feature Scaling:
 - Numeric columns were normalized using MinMax Scaling to bring all features to a common scale.

 One-Hot Encoding:
 - The 'state' column was one-hot encoded to create binary variables for each state.

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

Evaluation Metrics
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- R-squared (R²)

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
