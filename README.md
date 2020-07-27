# Machine Learning Challenge

## Build and evaluate several machine learning models to assess credit risk using LendingClub, a peer-to-peer lending services company<br>

Credit risk is an inherently unbalanced classification problem, as the number of good loans easily outnumber the number of risky loans. Therefore, I needed to employ different techniques to train and evaluate models with unbalanced classes. I used imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. The goal is to evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

link to dataset: https://github.com/mydogmandy/Machine_Learning_Challenge/blob/master/Resources/LoanStats_2019Q1.csv

Below are the six different models used, the balanced accuracy scores, precision, recall, and f1 scores.
Recall (sensitivity) = Percentage of true positives predicted correctly<br>
Precision = Accuracy of positives predicted correctly<br>
f1 (harmonic mean) = Weighted average of the Precision & Recall

In all the models tested, 100% of the low-risk loans were correctly identified, but out of the six tested, the Easy Ensemble AdaBoost Classifier performed the best.<br>
The balanced accuracy score is 0.93, showing the highest percentage of low-risk & high-risk predicted correctly.<br>
The overall recall of 0.92 & 0.94 reflects this as well, as this measures true positives.<br>
Although the high-risk precision is 0.09, it is due to the the reluctance of the model to commit to high-risk due to the features tested.  With further tweaking of the features tested, this model can be improved.


* #### Balanced Random Forest Classifier<br>
  Balanced Accuracy Score:  0.7885466545953005<br>
  High-Risk:  Precision = 0.03 / Recall = 0.70 / f1 = 0.06<br>
  Low_Risk:  Precision = 1.00 / Recall = 0.87 / f1 = 0.93<br>

* #### Easy Ensemble AdaBoost Classifier<br>
  Balanced Accuracy Score:  0.9316600714093861<br>
  High-Risk:  Precision = 0.09 / Recall = 0.92 / f1 = 0.16<br>
  Low_Risk:  Precision = 1.00 / Recall = 0.94 / f1 = 0.97<br>

* #### Naive Random Oversampling<br>
  Balanced Accuracy Score:  0.6742571941946299<br>
  High-Risk:  Precision = 0.01 / Recall = 0.74 / f1 = 0.02<br>
  Low_Risk:  Precision = 1.00 / Recall = 0.61 / f1 = 0.75<br>

* #### SMOTE Oversampling<br>
  Balanced Accuracy Score:  0.6623356588465208<br>
  High-Risk:  Precision = 0.01 / Recall = 0.63 / f1 = 0.02<br>
  Low_Risk:  Precision = 1.00 / Recall = 0.69 / f1 = 0.82<br>

* #### ClusterCentroids Resampler<br>
  Balanced Accuracy Score:  0.547120874973372<br>
  High-Risk:  Precision = 0.01 / Recall = 0.68 / f1 = 0.01<br>
  Low_Risk:  Precision = 1.00 / Recall = 0.41 / f1 = 0.58<br>

* #### Combination (Over and Under) SMOTEENN Sampling<br>
  Balanced Accuracy Score:  0.6447701423556762<br>
  High-Risk:  Precision = 0.01 / Recall = 0.72 / f1 = 0.02<br>
  Low_Risk:  Precision = 1.00 / Recall = 0.57 / f1 = 0.72<br>

