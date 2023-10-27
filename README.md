## Project Objective
The objective of this project is to develop a machine learning model that predicts whether a customer who has already taken out health insurance with the company might also be interested in taking out insurance on their vehicle.

## Exploratory Data Analysis
In the exploratory data analysis phase, the following steps were taken:
- Numerical and categorical variables were analyzed individually.
- Each variable was visually represented to better understand its characteristics and distribution.
- A correlation analysis was conducted for numerical variables using Pearson correlation.
- For categorical variables, the Chi-square test was employed, followed by transforming the obtained p-values using Cramer's V to quantify the strength of the association between variables.
- Variance Inflation Factor was calculated to assess multicollinearity among numerical variables.

## Preprocessing
Further analysis of numerical variables was carried out to examine distribution qualities and identify outliers. Appropriate transformations were applied, including the removal of outliers.

## Pipeline Building
Following the exploratory analysis and outlier handling, the dataset was split into training and testing sets. Due to the class imbalance in the response variable, oversampling was performed outside the pipeline.

For the final preprocessing of the dataset, two pipelines were created: one for handling numeric variables and one for categorical variables.

## Models
Given the highly unbalanced nature of the dataset, the focus was on models suitable for such situations, including:
- XGBoost algorithm
- Balanced Random Forest Classifier
- Logistic regression as a baseline model to assess the impact of class imbalance.
  
Complex ensemble models are often effective in these scenarios. Therefore, the XGBoost was used for the final training.

Each model underwent a randomized search for hyperparameter tuning.

Finally, predictions were made on a test dataset that the model had not seen during training.
