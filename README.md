# Credit_Risk_Analysis
##	Overview of the analysis: 
1.	**Purpose:** An analysis of a supplied dataset was requested to evaluate the performance of six models for use in assessing credit risk. 
2.	**Discussion:** Two oversampling algorithms, naïve random oversampling, and synthetic minority oversampling technique (SMOTE), were evaluated along with one under sampling technique (Cluster Centroid algorithm) as well as a combination (over and under) sampling technique called SMOTEEN (that is, SMOTE mentioned previously combined with Edited Nearest Neighbor (ENN)).  Additionally, two ensemble learning algorithms were compared, a balanced random forest classifier and an “easy ensemble classifier” (an ensemble of AdaBoost (Adaptive Boosting) learners trained on different balanced bootstrap samples). (Note: a “bootstrap sample” is a smaller sample that is taken or “bootstrapped” from a larger sample.)
3.	**Scoring Methods:** Since the dataset by its nature was quite unbalanced (significantly more good credit scores than bad, a “balanced accuracy score” was calculated. Next, the “confusion matrix” was displayed.  Finally, a performance evaluation metric called a classification report was employed. Some of the metrics included in the report are precision (pre) or the ratio of true positives to the sum of true positives and false positives, recall (rec) or the ratio of true positives to the sum of true positives and false negatives, F1 score which is the harmonic mean of precision and recall, and support (sup) which is just the number of actual occurrences of each class in the dataset.   Because the dataset was imbalanced, the imbalanced classification technique was used.  (Note: In the report, three other metrics are included: specificity (spe) which is also known as the “true negative rate”, geometric mean (geo), and index balanced accuracy (iba).  A more detailed explanation of index imbalanced accuracy (as well as some of the other metrics mentioned here) can be found at: https://dev.to/amananandrai/performance-measures-for-imbalanced-classes-2ojj
Note that while all the results are shown, only the balanced accuracy, precision, and recall scores will be discussed in the "Results" section. 	
##	Results: 
1.	Naïve Random Oversampling:  For the imblearn RandomOverSampler technique, the results are shown below:
 -	![Naïve Random Oversampling Results](images/Naive_Random_Oversampling_results.png)
 -	As can be seen above, the Naïve Random Oversampling technique had a balanced accuracy score of 0.69. It's precision (as well as the other three smapling techniques) was 1.00 for the low risk class (which represented the overwhelming majority of the data in the dataset) and 0.01 for the high risk class (which represented less than 1% of the instances in the dataset).  The recall was 0.77 for the high risk class and 0.60 for the low risk class.  The implication here is that 40% of the low risk candidates would be inaccurately tagged as high risk candidates.
2.	SMOTE:  For the imblearn SMOTE technique, the results are shown below:
 -	![SMOTE Oversampling Results](images/SMOTE_Oversampling_results.png)
 -	
3.	Cluster Centroid Algorithm:  For the imblearn ClusterCentroids technique, the results are shown below:
 -	![Cluster Centroid Undersampling Results](images/ClusterCentroid_Undersampling_results.png)
 -	
4.	SMOTEEN:   For the imblearn SMOTEENN technique, the results are shown below:
 -	![SMOTEEN Combination Over and Under Sampling Results](images/SMOTEEN_Combination_Over_and_Under_Sampling_results.png)
 -	
5.	Balanced Random Forest Classifier:   For the imblearn BalancedRandomForestClassifier technique, the results are shown below:
 -	![Balanced Random Forest Classifier Results](images/Balanced_Random_Forest_Classifier_results.png)
 -	
6.	Easy Ensemble Classifier:  For the imblearn EasyEnsembleClassifier technique, the results are shown below:
 -	![Easy Ensemble AdaBoost Classifier Results](images/Easy_Ensemble_AdaBoost_Classifier_results.png)
 -	
##	Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any.  If you do not recommend any of the models, justify your reasoning. 
