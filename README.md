# XGBoost-Email-Spam-Classifcation
Machine learning model for determining whether or not an email is spam based on the frequency of different words used in the email.
An XGBoost model was implemented to classify whether or not an email was spam based on training data with 30 words that and associated frequencies within each email, and a classification of whether or not this email was spam. The model was originally trained on a set of 1500 emails. KNN imputation was performed in order to habdle missing data represented as -1 in the data sets, and then a model was trained using a 5 fold cross validation, and cross validated feature selection in order to optimize our results without over or under fitting based on our training data. We gathered accuracy scores by using parts of the data that are unseen during the training of our model in order to replicate implementing our data on unseen data. 
When evaluating our final model we used the metrics of area under the ROC curve(AUC), and True Positive Rate(TPR) at a False Positive Rate(FPR) of 0.01. Based on many runs of our model looking at the data with different shuffles, and a full data set of 3000 different emails we achieved the following results:
Mean AUC: .891
STD Dev. AUC: .006
Mean TPR at FPR = 0.01: .423
STD Dev. TPR at FPR = 0.01: .038
