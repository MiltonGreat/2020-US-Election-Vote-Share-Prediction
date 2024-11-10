# 2020-US-Election-Vote-Share-Prediction

### Overview

This project focuses on the cleaning and preprocessing of the US Election 2020 dataset using Pandas in Python. The primary goal is to prepare the data for further analysis or modeling by addressing issues like missing values, outliers, feature selection, and model evaluation. We use multiple models like Linear Regression and Random Forest Regressor to predict the vote share for the Democratic Party in each county.

### Dataset

The dataset contains the following columns:

- County: The county name.
- State: The state where the county is located.
- Population: Various population statistics (total, race, education level).
- Voting Data: The number of votes for the Democratic, Republican, and other parties.
- Vote Share: The percentage of votes for each party.

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

### Model Training and Evaluation

- Linear Regression: The Linear Regression model was trained to predict the Democrat's vote share, evaluated using metrics like Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared.

- Random Forest Regressor: The Random Forest Regressor was used to model the vote share, and cross-validation was applied to assess its generalizability. Feature selection was performed using Recursive Feature Elimination (RFE).

- Evaluation: Both models were evaluated and compared based on their predictive performance. The Random Forest model performed slightly better, with an R-squared of 0.99995.

### Issues and Areas for Improvement

- Overfitting: The models (especially Linear Regression) showed perfect R-squared values, suggesting potential overfitting. This issue can be mitigated with regularization techniques or by using simpler models.

- Feature Selection: The feature engineering and selection process can be further improved. Exploring correlations between features and using Principal Component Analysis (PCA) or Variance Inflation Factor (VIF) can help reduce multicollinearity.

- Missing Value Handling: While missing values were imputed using the mean strategy, exploring other imputation methods (such as median imputation or using a more sophisticated model) might improve results.

### Source

https://www.kaggle.com/datasets/essarabi/ultimate-us-election-dataset
