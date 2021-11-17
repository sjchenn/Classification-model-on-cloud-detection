# STA521_PRO2


This project features a CVmaster function, which compute k-fold cross-validation for algorithms used in this project. It takes a character string `classifiers`,`features`,`labels`,`nfold`, and additional hyperparameters that can be tuned in some of the models as input.
Classifier is a character string which specify the type of algorithm.\
`knn`: K-nearest neighbors\
`xgboost`: XGBoosting\
`lda`: Linear discriminant analysis\
`logistic`: Logistic Regression

Features is a matrix training data for the model, but should not include the true labels

Labels is a vector of factors which is the true labels for training data

nfold is a positive number specifying the number of cross-validation set to be created, with default value 5.

The other inputs are used for hyperparameter tuning, and they are set with default value. If some of the hyperparameter are not used for a specific model, no input is needed.

`KNN`:\
k is a real number specifying number of nearest neighbor to use in KNN, with default value 5

`XGBoosting`:


max_depth is a real number specifying maximum depth for trees in XGBoost,with default value 4

min_child is a real number specifying minimum weights a child needs to be before splitting trees in XGBoost,with default value 1

niter is a real number specifying number of runs for XGBoost

seed is a real number specifying random seed used, which keeps results of cross-validation reproducible. The default value is 521.

In addition to CVmaster, we provide separate cross-validation function for XGBoost and KNN which requires tuning on hyperparameters. If future users need to tune on hyperparameters not included in CVmaster, it is easier to make changes to individual cross-validation functions. 


