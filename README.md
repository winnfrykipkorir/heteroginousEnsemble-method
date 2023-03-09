# heteroginousEnsemble-method
Two datasets, churn modelling.csv and Insurance.csv, are the focus of a machine learning operation on random forest employing heterogeneous ensemble.
Pandas, RandomForestClassifier, VotingClassifier, DecisionTreeClassifier, LogisticRegression, and Numpy are among the libraries that have been submitted. 
First, the dataset is loaded and examined for missing values; in this instance, neither dataset has any missing values. In this scenario, CustomerId in the churn 
and children in the insurance columns were removed from the dataset as they were unneeded for the analysis of the data. Under the 0.2 test fraction, data are 
divided into training and test sets. A base classifier, rf1 = RandomForestClassifier(n estimators = 50, random state = 42), is used to produce a heterogenous 
ensemble random forest classifier. DecisionTreeClassifier with maximum depth of 5 and random state of 42. constructing a heterogeneous regression model using 
lr = LogisticRegression(random state = 42)..A heterogeneous ensemble classifier is then created using the formula hetero rf = VotingClassifier(estimators=[('rf1', rf1)
, ('dt', dt), ('lr', lr)], voting = 'hard'). The models are tested for accuracy, precision, recall, and f1 score by making predictions using the test set.
Greater accuracy values show that the model performs well on the dataset, whereas lower accuracy values show that the ensemble performs poorly. While insurance 
produced average values, the churn model produced a variety of results that were all very high, indicating a successful ensemble.
