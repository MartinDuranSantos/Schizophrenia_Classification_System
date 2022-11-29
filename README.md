# Schizophrenia_Classification_System
Classification basics of EEG signals of people with schizophrenia, via Logistic Regression (LR) and Stochastic Gradient Descent (SGD)

The files "ERPdata.csv" and "demographic.csv" can be downloaded from https://www.kaggle.com/datasets/broach/button-tone-sz

Original source: 
Ford, J. M., Palzes, V. A., Roach, B. J., & Mathalon, D. H. (2014). Did I do that? Abnormal predictive processes in schizophrenia when button pressing to deliver a tone. Schizophrenia bulletin, 40(4), 804–812. https://doi.org/10.1093/schbul/sbt072

Run full program to execute Logistic Regression (LR) algorithm.

To change to Stochastic Gradient Descent classifier, change in [6]:

-------------------------------------------------------------------------------------------------------------------------------------------
#clf_lr = SGDClassifier(max_iter=1000, tol=1e-3, random_state=42)
#clf_lr.fit(X_train, Y_train==1)
clf_lr = LogisticRegression(random_state=0, solver='lbfgs',multi_class='multinomial',max_iter=200).fit(X_train, Y_train==1)
-------------------------------------------------------------------------------------------------------------------------------------------

For this:

-------------------------------------------------------------------------------------------------------------------------------------------
clf_lr = SGDClassifier(max_iter=1000, tol=1e-3, random_state=42)
clf_lr.fit(X_train, Y_train==1)
#clf_lr = LogisticRegression(random_state=0, solver='lbfgs',multi_class='multinomial',max_iter=200).fit(X_train, Y_train==1)
-------------------------------------------------------------------------------------------------------------------------------------------

