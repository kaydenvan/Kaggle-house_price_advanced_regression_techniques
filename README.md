# Kaggle Competition 
This repository contains the code for a Kaggle competition, [House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques). <br><br>

### First submission
With the quick start, XGBoost is used with basic null value handling and data cleansing. The score is 0.14469 ranked 48%. 

### Second submission
Data cleansing (i.e. fill missing fields) has been done based on the data description provided by Kaggle. Same XGBoost configuration has been used. The score is 0.15039 which is lower than the first submission. It is because extra columns are created to handle null fields. This brings extra difficulties on the ensemble method. 

### Third submission
NuSVR has been used with hyperparmeters tuning using optuna framework. It is a good machine learning algorithm in high dimension space, which is in this case, with more than 200+ features created. However, the score drops to 0.20218 which is unexpected initially. <br>
**Learning**: Since I blindly transfer all the columns using one hot encoding, which creates huge amounts of highly correlated features. This brings huge impact of the model result. The VIF between columns are high.

### Fourth submission 
At the second submission, I failed to do the data cleansing properly and create significant amount of highly correlated features. This submission choose some columns with LabelEncoding and some one-hot encoding. The score jumps back to 0.18595, although worse than the first submission, shows it is on the right direction.

### Fifth submission
Turning the model back to XGBoost and hyperparameters tuning. The score is 0.13943 ranked 41.5%.
