# Red Wine Quality Prediction Using Classification Modelling and Machine Learning
### Data Understanding

My analysis will use Red Wine Quality Data Set, available on the UCI machine learning repository (https://archive.ics.uci.edu/ml/datasets/wine+quality). It contains the red wine samples from the north of Portugal to model red wine quality based on physicochemical tests. The dataset contains a total of 12 variables, which were recorded for 1,599 observations. This data will allow us to create different classification models to determine how different independent variables help predict our dependent variable, quality.The variables are as follows:
1. Alcohol: Amount of alcohol(ethanol) present
2. Volatile acidity: high acetic acid in wine which have an unwelcoming vinegar taste
3. Sulphates: a wine additive that is generally used to save and cover the wines from bacteria 
4. Citric Acid: Used in wines that are naturally lacking in acid. It helps bring out the fruity flavour of the wine
5. Total Sulphur Dioxide:  gives a pungent smell
6. Density: thickness of the wine
7. Chlorides: Generally referred to as salt in the wine
8. Fixed acidity: are non-volatile acids like tartaric or malic acids
9. pH: the level of acidity in the wines.
10. Free Sulphur Dioxide: it prevents microbial growth and the oxidation of wine
11. Residual sugar: the amount of sugar remaining after the fermentation process
12. Quality – the score ranges between 3-8.


### Data Preparation

I explored the dataset to identify any missing or duplicate values. The data had 240 duplicated rows, so we removed those values.  Then, I analysed each column’s statistical summary to detect the outliers. I removed the outliers from the data by capping them using the z score method i.e. z = Data*mean +/- 3*std. I also ran a correlation analysis of the independent variables against the dependent variable, quality. This analysis showed a list of variables that had the highest correlations with quality and I dropped those who had high correlation i.e. >60%. 
I set an arbitrary cut-off for the dependent variable (wine quality) at e.g. 6 or higher getting classified as 'good/1' and the remainder as 'not good/0' to make it a classification problem.


### Modelling

Based on the EDA and correlation analysis, various classification models were used. We evaluated our model using the following metrics: Accuracy, Precision, Recall and ROC Score. We split the data randomly into training and testing data where we used the training data to train the models and testing data to test the model’s performance.
Model One: Decision Tree
“Decision tree uses a tree like structure to solve a problem in which each node represents an attribute, each link represents a decision rule and each leaf node represents an outcome.”

Model Two: Random Forest
“Random Forest is an ensemble bagging (bootstrap + aggregation) algorithm that works as a large collection of decision trees and merges them to obtain a more stable and accurate prediction through cross-validation.”

Model Three: Support Vector Machine
“SVM is a supervised ML algorithm which is used for classification problems. It uses a technique called kernel trick to transfigure non-linear low dimension space to a higher dimension space to get linear classification/separator.”
