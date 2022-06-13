# Predicting Bike Rentals: Project Overview
- Implemented and compared three models to predict number of bike rentals in a given hour: Linear Regressor, Decision Tree Regressor, and Random Forest Regressor
- With 14 numeric features and simple holdout validation, determined that Random Forest Regressor was the best model with lowest root mean squared error (~45 bikes)

## Code and Resources Used
**Python Version:** 3.7
**Packages:** pandas, sklearn, numpy, matplotlib, seaborn
**Dataset:** http://archive.ics.uci.edu/ml/datasets/Bike+Sharing+Dataset

## Data Overview
For each listing, we get 17 columns detailing information about the number of bikes rented in a given hour on a given day. Our target variable is "cnt", the number of bikes rented in the given hour.
![image](https://user-images.githubusercontent.com/97380323/173437182-69087cd1-a781-4fbc-b331-ee7c92939705.png)

## Feature Selection and Engineering
I dropped the columns "casual" and "registered", since "cnt" is the sum of these rental categories and this distinction is not relevant to our project.
I computed the pearson correlation coefficient between variables in order to see which features may be relevant to a regressor.
![image](https://user-images.githubusercontent.com/97380323/173436619-dfd18e78-e244-40ca-9026-44ef382a80a0.png)

For this project, we included all features, even those with low correlation values, since they could be useful for our non-linear regressors.

## Comparing Model Performance
![image](https://user-images.githubusercontent.com/97380323/173436801-565a814f-d40c-45d5-992f-ed1b2675fde9.png)
Based on RMSE, the Random Forest Regressor model had the best performance, with a RMSE value of 45 bikes.

