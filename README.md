# Predicting Credit Risk

## Background

LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.

We will be using this data to create machine learning models to classify the risk level of given loans. Specifically, we will be comparing the Logistic Regression model and Random Forest Classifier.

<hr>

### Dataset used

We will be using an entire year's worth of data (2019) to predict the credit risk of loans from the first quarter of the next year (2020).

The datasets used have been undersampled to give an even number of high risk and low risk loans. In the original dataset, only 2.2% of loans are categorized as high risk.

<hr>

## Preprocessing

### Prediction - Logistic Regression vs. Random Forest (unscaled)
The dataset we are using is highly categorical and non-linear. 
Linear relationships are best used with logistic regression.
Datasets with non-linear relationships operate best with random forest for a balance between precision and overfitting.
The prediction would be that in this case, the random forest model will be more accurate compared to a logistic regression model.

### Result - Logistic Regression vs. Random Forest (unscaled)
The random forest model yielded a score of 0.64 compared to the logistic regression model score of 0.51.
The result was in line with the initial prediction of a random forest being more accurate in this particular dataset for the non-linear relationships.

<hr>

## Revisit the Preprocessing: Scale the data

### Prediction - Logistic Regression vs. Random Forest (scaled)
Random forest models do not require the data to be scaled and so will not see much of a change from the data being scaled.
Logistic regression models will see an improved score from the scaling of the data.

### Result - Logistic Regression vs. Random Forest (scaled)
The random forest model yielded the same test score result as with the unscaled dataset.
The logistic regression model shows a test score improvement of 0.25.
The results are in line with the initial prediction that scaling has a significant impact on logistic regression models, with little to no impact on random forest models.
With an unscaled dataset, the random forest was resulting in a higher test score compared to logistic regression.
However, after scaling, logistic regression yielded a higher result than random forest, showing that a properly scaled data on a simpler model could be more effective than complex decision tree models like random forests.