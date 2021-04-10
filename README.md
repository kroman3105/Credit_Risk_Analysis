# Credit_Risk_Analysis

## Overview
We saught out to build machine learning models to predict credit card risk.  As this is an unbalanced classification problem, we used several different techniques to undersample and oversample as well as a combinatorial approach.  Finally, BalancedRandomForestClassifier and EasyEnsembleClassifier models were used to predict credit risk

## Results
- Naive Random Oversampling returned a balanced acurracy score of 0.65, an avg precision score of 0.99 and an avg recall score of 0.57
- SMOTE Oversampling returned a balanced acurracy score of 0.66, an avg precision score of 0.99 and an avg recall score of 0.68
- Cluster Centroids Undersampling returned a balanced acurracy score of 0.54, an avg precision score of 0.99 and an avg recall score of 0.40
- SMOTEENN Combination approach returned a balanced acurracy score of 0.65, an avg precision score of 0.99 and an avg recall score of 0.58
- Balanced Random Forest Classifier returned a balanced acurracy score of 0.79, an avg precision score of 0.99 and an avg recall score of 0.87
- Easy Ensemble AdaBoost Classifier returned a balanced acurracy score of 0.93, an avg precision score of 0.99 and an avg recall score of 0.94

## Conclusion
In reviewing the models, the Easy Ensemble AdaBoost Classifier performed the best of the six models in terms of the balanced accuracy score, avg precision score and avg recall score.  The Cluster Centroids model performed the worst, and is probably not the right model for this analysis.  Based on these findings, I would recommend the use of the Easy Ensemble AdaBoost Classifier model for predicting credit risk.  Along witht he high balanced accuracy score, a big reason for this model is the precision score at identifying low credit risks.  If the model tells you that an individual has a low credit risk and therefore worthy of extending credit, you want that conclusion to be very precise and not result in a lot of False Postives where you extend credit to inidivuals who turn out to be high risk.  For purposes of analyzing credit risk, you're willing to live with the lower precision score on identifying high risk clients.  You're willing to turn away those customers who were predicted as High Risk that ended up being Low Risk if that means you'll avoid offering credit to those customers who truly are High Risk.
