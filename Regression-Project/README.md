# What Makes Food Delicious: Studying the Relationship Between Ingredient Levels and Popularity of a Recipe

### Abstract

The goal of this project was to determine the possible contribution of a recipe's nutritional ingredients to its popularity using data from recipe bank website, allrecipes.com. A few linear regression models were built using the data obtained by web-scraping from the website. The results suggest that the linear models can explain a small degree of the variability that can be observed in the ratings of the recipes. It is possible that the bulk of variability in the ratings can still be explained using non linear models. But even using a linear model shows that a few of the ingredients can stand out as main contributors to the popularity of a recipe.

### Design

Python web-scraping package, Beautiful Soup, was used to extract close to 1800 rows of data from allrecipes.com.
300 irregular entries were discarded before the start of the analysis. 1496 rows were used for the main regression analysis. Outliers were removed by using the reported calories as the criteria (<100 or >1000) as calories have been shown to have a high correlation with the amount of the ingredients. Then the remaining dataset was split into 80/20 train vs. holdout using scikit learn model selection module. A handful of engineered features were added to the dataset based on their contribution to an initial fitted ordinary least squares (OLS) model to the training data, bringing the number of the features to a total of 30.

### Tools

scikit learn modules, KFold, cross_val_score, GridSearchCV, LinearRegression, Lasso, Ridge and ElasticNet were used in order to prepare the data, fit different types of linear regression models and finding the optimized value for hyper-parameters. The data were divided into five groups and using scikit-learn cross validation package and then OLS, least absolute shrinkage and selection operator (LASSO), Ridge and Elastic Net regression models were fitted to the validation data and the mean scored across the five validation sets were calculated.

### Results

Ridge regression was chosen as the final model on the basis of having the largest average R^2 (0.067 + 0.043) across the validation groups (with optimum alpha) and also on the basis of a substantial optimum alpha value that was calculated. In order to further minimize overfitting, the alpha was increased to 1 (R^2 = 0.059 + 0.032). A limited linear relationship was observed among the final 17 selected features and the target. After selecting the optimum model via cross-validation, the model trained and scored on the whole training data set (R2 = 0.082, MAE = 0.155). Finally, the models were trained on all the data and scored on the hold-out test group (R2 = 0.059, MAE = 0.162). Protein, Cholesterol and Fat were determined as the most influential features.

It is possible that the relationship between the nutrients and the rating follows a non-linear pattern, and therefore non-linear models (decision trees, random forest, etc.) would be better tools in order to investigate this relationship. 
