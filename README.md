# data-leakage
an example of data leakage
In this example, I have used make_classification to generate random data with 1000 samples and 20 features, with 15 informative
features and 5 redundant features. I then split the data into training and testing tests with a 70/30 split. After that,
I fit the MinMaxScalers separately on the training and testing sets and then trained an SVM on both with the appropriate scaled features.
By comparing the accuracies, you should see that the accuracy with the scaler fit separately on X_train and X_test should be higher than the
accuracy with the scaler fit on all of X. This is because fitting th e scaler on all of X can potentially introduce data leakage from the
testing set into the training set, which can lead to overfitting and reduced accuracy on new, unseen data.
