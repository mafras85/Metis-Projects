# Identifying the flake!

### A classification model to identify the potential cancelling customers for Marriott International

### Abstract

The purpose of this project was to build a classification model in order to better identify the hotel bookings with higher cancellation risk based on a series of given variables. This model will be used by Marriott International to ultimately reduce the rate of booking cancellations by allocating marketing resources to or imposing stricter terms on the customers with higher probability of cancellation. The final model built in this phase of the project is using the Random Forest algorithm. This algorithm also produced a list of the most relevant features that can be used by the marketing and administrative department of Marriott International for devising future strategies.

### Data

A combined dataset from two hotels will be used in this project. Both hotels are located in Portugal. The dataset contains 31 original variables describing 119390 observations. Each observation represents a hotel booking. The dataset includes bookings due to arrive between the 1st of July 2015 and the 31st of August 2017, including bookings that effectively arrived (0 class) and bookings that were canceled (1 class). The data has been provided to the public by Antonio N. et al in the February 2019 issue of Data in Brief journal (https://doi.org/10.1016/j.dib.2018.11.126).

### Methodology

The entire dataset was splitted into 80/20 train vs. holdout. The train set was further splitted 75/25 into train and validation sets. The validation set was used for diagnostic purposes during the modeling phase. The train set was splitted into 5 cross-validation sets and diagnostic scores were recorded as the average across all 5 groups. Predictions on the holdout were limited to the very end, so this split was only used and scores seen just once.

K Nearest Neighbor (KNN), Logistic Regression (LR), Decision Tree (DT), Random Forest (RF) and XGBoost (XGB) classifiers were fitted and evaluated on the data. An ensemble voting classifier comprising all five models was also evaluated. Model selection was performed primarily based on the ROC AUC score and plot. The optimal threshold for the selected model was further tuned based on the Precision-Recall curve.

### Results

Random Forest model was selected as the model with best overall performance based on AUC score and ROC curve:

![ROC](https://user-images.githubusercontent.com/84594280/142649031-bb7ea613-38bc-4882-83b3-a4e49bcf7875.png)

RF and XGB were almost identical in the overall performance, but the RF were selected over XGB at this phase of the project as the primary working model. XGB needs extensive tuning of the hyperparameters to reach peak performance which was not feasible in the initial phase.

Feature importances list created by the RF algorithm was also extracted:

![download](https://user-images.githubusercontent.com/84594280/142649295-28af98e7-5683-47b7-9f0f-59474daabbe6.png)

The first 5 features belong to three categories of Average Daily Rate (ADR), Reservation Lead Time and Deposit Type.

The selected RF model was further tuned to achieve the optimal balance between precision and recall rates. The Precision-Recall curve was used to determine the optimal threshold of 0.3775:

![P R](https://user-images.githubusercontent.com/84594280/142649406-70ab9996-0bcd-4bbb-8a7f-e832aa1680ec.png)

After updating the model with this threshold the following scores were recorded on the validation set and finally on the hold-out test set:

__Validation Scores__:

__Accuracy__: 0.818<br>
__Precision__: 0.759<br>
__Recall__: 0.753<br>
__F1__: 0.756<br>
__AUC__: 0.890<br>


__Hold-Out Scores__:

__Accuracy__: 0.824<br>
__Precision__: 0.756<br>
__Recall__: 0.787<br>
__F1__: 0.772<br>
__AUC__: 0.900<br>

The current model can be further refined and improved in the future phases.




