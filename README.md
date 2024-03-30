# Credit Risk Model

## Approach

Start with a logistic regression model as a baseline performance since it is easier to explain and interpret. Than we will use more decision tree related models like xgboost often resulting in better model performance.

Special columns (from Kaggle):

case_id - This is the unique identifier for each credit case. You'll need this ID to join relevant tables to the base table.

date_decision - This refers to the date when a decision was made regarding the approval of the loan.

WEEK_NUM - This is the week number used for aggregation. In the test sample, WEEK_NUM continues sequentially from the last training value of WEEK_NUM.

MONTH - This column represents the month and is intended for aggregation purposes.

target - This is the target value, determined after a certain period based on whether or not the client defaulted on the specific credit case (loan).

num_group1 - This is an indexing column used for the historical records of case_id in both depth=1 and depth=2 tables.

num_group2 - This is the second indexing column for depth=2 tables' historical records of case_id. The order of num_group1 and num_group2 is important and will be clarified in feature definitions.