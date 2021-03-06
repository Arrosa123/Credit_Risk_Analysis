# Credit_Risk_Analysis
## Overview of the analysis:

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we need to employ different techniques to train and evaluate models with unbalanced classes. We use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. 
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

## Results: 

### Naive Random Oversampling

The Naive Random Oversampling method used RandomOverSampler to resample the data. The logistic regression model was trained and the following image and information shows the resulting balanced accuracy score, confusion matrix, and imbalance classification report.
Accroding to the following image;
- The balanced accuracy score for this model is around 64.5%. This is good score, but not excellent. 
- The precision scores for this model are very skewed toward the low-risk loans, but none of the high risk loans were predict.
- The recall scores for this model show that the model is better at identifying positive low-risk loans (0.68) and decent at positively identifying high-risk loans (0.61).


![2022-04-29 (1)](https://user-images.githubusercontent.com/96403349/165952718-a12aa51b-450e-4aae-9fc9-612842fd1e93.png)

### SMOTE Oversampling

This method used SMOTE to resample the data and enlarge the minority class of training data to use in a logistic regression model. The logistic regression model was trained and the following image and information shows the resulting balanced accuracy score, confusion matrix, and imbalance classification report.
Accroding to the following image;
- The balanced accuracy score for this model is around 64.5%. This is good score, but not excellent. 
- The precision scores for this model are very skewed toward the low-risk loans, but none of the high risk loans were predict.
- The recall scores for this model show that the model is better at identifying positive low-risk loans (0.63) and decent at positively identifying high-risk loans (0.64).

![2022-04-29 (2)](https://user-images.githubusercontent.com/96403349/165957183-6116c32a-d72e-4726-9797-dfebc4d27af6.png)

### Undersampling

This method used Cluster Centroidsthe to resample data and enlarge the minority class of training data to use in a logistic regression model. The logistic regression model was trained and the following image and information shows the resulting balanced accuracy score, confusion matrix, and imbalance classification report.
Accroding to the following image;
- The balanced accuracy score for this model is around 63.8%. This is good score, but not excellent. 
- The precision scores for this model are very skewed toward the low-risk loans and low-risk were correctly predicted, but none of the high risk loans were predict.
- The recall scores for this model show that the model is better at identifying positive low-risk loans (0.45) and decent at positively identifying high-risk loans (0.61). While the high-risk recall is much better than low-risk recall.

![2022-04-29 (3)](https://user-images.githubusercontent.com/96403349/165958310-22a1b8af-3ca1-44e0-9fd6-f907845032ba.png)


### Combination (Over and Under) Sampling

This method used SMOTEENN to remove outliers and resample the data to use in a logistic regression model. The logistic regression model was trained and the following image and information shows the resulting balanced accuracy score, confusion matrix, and imbalance classification report.
Accroding to the following image;
- The balanced accuracy score for this model is around 53%. 
- The precision scores for this model are very skewed toward the low-risk loans and low-risk were correctly predicted, but none of the high risk loans were predict.
- The recall scores for this model show that the model is better at identifying positive low-risk loans (0.70) and decent at positively identifying high-risk loans (0.57). While the high-risk recall is much better than low-risk recall.

![2022-04-29 (4)](https://user-images.githubusercontent.com/96403349/165959140-1a7df3fb-2404-4fca-a2d5-71ffbd1a66c8.png)

### Balanced Random Forest Classifier

The Balanced Random Forest Classifier used to find 100 estimators to to classify the testing data. The logistic regression model was trained and the following image and information shows the resulting balanced accuracy score, confusion matrix, and imbalance classification report.
Accroding to the below image;

-  the following image and information shows the resulting balanced accuracy score, confusion matrix, and imbalance classification report.
Accroding to the below image;This shows that the classifier is good at predicting true positives for low-risk loans.


![2022-04-30](https://user-images.githubusercontent.com/96403349/166133515-a18769d2-444e-4a01-bd04-a4ca234c3f7e.png)

### Easy Ensemble AdaBoost Classifier

The Easy Ensemble AdaBoost Classifier was used to train and evaluate models to classify the testing data. the following image and information shows the resulting balanced accuracy score, confusion matrix, and imbalance classification report.
Accroding to the below image;

- The balanced accuracy score for this model is around 92.6%. 
- The precision scores for this model are very skewed toward the low-risk loans and low-risk were correctly predicted, but some of the high risk loans were predict.
- The recall scores for this model show that the model is better at identifying positive low-risk loans (0.94) and decent at positively identifying high-risk loans (0.91)which shows the high rate of true postive. 

![2022-04-30 (1)](https://user-images.githubusercontent.com/96403349/166133665-508ce760-6b1a-4d86-a3af-3ab2815bcc49.png)

## Suumary:

For all machine learning models, utilize that EasyEnsembleClassifier is the most effective and provides a highest Score for all Risk loans. The best predictive models had a fair mix of recall and precision accuracy. I would recommend one of the 2 ensemble models because they have high accuracy scores than other 4 models. And the Easy Ensemble AdaBoost Classifier has the balanced of precision and recall accuracy scores and this specific model to be used to assess credit risk in this example and also in the future. 


