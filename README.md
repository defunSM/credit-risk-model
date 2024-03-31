# Credit Risk Model

# 1. Data

This dataset is taken from Kaggle and contains contains financial information in order to determine the target feature which is if a person will default on their loan.


# 2. Method

The goal is to first explore the dataset to figure out which features of the dataset can be used for training the model.

1. Using logistical regression as a baseline classifier.
2. Use a tree based model to optimize the accuracy of the model.

# 3. Cleaning

1. Many of the features have NaNs in the dataset and thus remove any NaNs in the dataset.

2. Pick out the highest correlated features to the target feature for the model.

3. Heatmap to represent the correlations of the columns that most correlate to the target feature.


# 4. EDA

There is many features for this dataset. Therefore one approach I took is to narrow down the features is to take numerical ones and then find any features that have > 0.01 to the target feature. This narrows it down to just two features.


Special columns:

case_id - This is the unique identifier for each credit case. You'll need this ID to join relevant tables to the base table.

date_decision - This refers to the date when a decision was made regarding the approval of the loan.

WEEK_NUM - This is the week number used for aggregation. In the test sample, WEEK_NUM continues sequentially from the last training value of WEEK_NUM.

MONTH - This column represents the month and is intended for aggregation purposes.

target - This is the target value, determined after a certain period based on whether or not the client defaulted on the specific credit case (loan).

num_group1 - This is an indexing column used for the historical records of case_id in both depth=1 and depth=2 tables.

num_group2 - This is the second indexing column for depth=2 tables' historical records of case_id. The order of num_group1 and num_group2 is important and will be clarified in feature definitions.

