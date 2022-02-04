# model_based_drift_detection
Implementation of a model based drift detection technique

The idea is to remove the Y labels from the training data set and label half of the training data as zero and the other half as one.
A machine learning model is fit on the modified data set and the test data is evaluated and their probabilities of prediction are taken.
If the probability of prediction is between .4 and 6, we consider that the model cannot differentiate between the two data points and that there is no significant drift in the incoming data. If this is not the case, we will infer that there is drift.
