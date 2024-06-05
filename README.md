# CreditCardFraud
Credit Card Fraud Detection System Using Machine Learning

Detect Fraudulent Credit Card transactions using different Machine Learning models and compare performances

In this notebook, I explore various Machine Learning models to detect fraudulent use of credit cards by comparing each model performance and results. The best performance is achieved using SMOTE technique.

The unique point in this analysis is that : 
    
    This approach can be transferred to other detection analysis in alternatrive domains. The feature extraction process remains similar and can be replicated on many other detection issues.

###  Problem Statement

In this project we want to identify fraudulent transactions with Credit Cards. Our objective is to build a Fraud detection system using ML techniques. In the past, such systems were rule-base but ML offers powerful new ways.

The project uses a dataset of 300,000 fully anonymized transactions. Each transation is labelled either fraudulent or not fraudulent. Note that prevalence of fraudulent transactions is very low in the dataset. Less than 0.1% of the card transactions are fraudulent. This means that a system predicting each transaction to be normal can reach an accuracy of over 99.9% despite not detecting any fraudulent transaction, therefore, creating a need to necessitate adjustment techniques.

The project compares the results of different techniques :

    Machine learning techniques:
        Random Forest
        Decision Trees
    Deep Learning techniques:
        Neural network using fully connected layers.

Performance of the neural network is compared for different optimization approaches:

    plain binary cross-entropy loss minimization
    minimization using weights to compensate for the class imbalance
    Under-sampling of the non-fraudulent class to match the fraudulent class
    Over-sampling of the fraudulent class to match the non-fraudulent one by implementing SMOTE technique. The SMOTE method allows to generate a new vector using 2 existing datapoints. For additional details on this approach, you can read this detailed post SMOTE for Imbalanced Classification with Python


Results

The best results are achieved by over-sampling the under-represented class using SMOTE (synthetic minority oversampling technique). With this approach, the model is able to detect 100% of all fraudulent transactions in the unseen test set. This fully satisfies the primary objective to detect the vast majority of abnormal transactions. Please note that the technique and model used are simple to implement simple, easy to use and can be updated in real-time.

In addition, the number of false positive remains acceptable. This means a lot less verification work (on legitimate transactions) for the fraud departement compare dto some other approaches which failed on this aspect.

Confusion matrix achieved using SMOTE over-sampling and a simple dense neural network.

Comparison of key performance indicators between the tested approaches.

