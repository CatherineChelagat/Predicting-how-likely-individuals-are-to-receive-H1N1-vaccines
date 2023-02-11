# Predicting-how-likely-individuals-are-to-receive-H1N1-vaccines
## Overview
This project aims to build a model that predicts individuals' response to vaccines based on how they reacted to the H1N1 vaccine in 2010. It will use the several feature variables provided to establish the connection between them and the target variable H1N1 vaccine. The dataset used for this project was ontained from [DrivenData](https://www.drivendata.org/competitions/66/flu-shot-learning/page/210/) and contains information on individual's characteristics ranging from level of concern to behaviour in their homes and large gatherings.
The project covers the following sections:
Business Understanding
Problem Statement
Objectives
Metrics of Success
Data Understanding
Data Preparation
Exploratory Data Analysis
Feature Engineering
Modeling
Feature Selection
Hyperparameter Tuning
Conclusion
Recommendation for Future Steps
## Business Understanding
The public health organization is interested in finding the response of individuals to the H1N1 vaccine in 2010, if a majority took it or not. With the cropping up of global pandemics like COVID-19, public health has become very critical and a priority to the government and health sector. For this reason, they saw it fit to study vaccines, and specifically, whether individuals get them or not. Having been approached with this, we look to build a classification model that will establish whether indivuals took the h1n1 vaccine and the factors that were correlated to them and predict individual's possible reaction to a case like this in the future. This will help the stakeholders to establish a feasible way to approach this issue in future.

We apply machine learning for this project because it will give the stakeholders a view of trends in individuals' behaviors in relation to their response to vaccines, as well as supports the development of new vaccines if need be.
### Problem Statement
Vaccination has become a key public health measure that is used to fight and in most cases curb infectious diseases. Vaccines provide immunization for individuals and having a community participate in the process can further decrease the spread of diseases as a result of the concept of "herd immunity."

The idea is to come up with a classification model that will predict (almost) accurately whether individuals were immunized with H1N1 vacciness and from this determine the next course of action depending on whether people are open or not getting the h1n1 vaccine.
### Objectives
Identify which factors affect individuals' response to vaccines

Accurately predict the general response of individuals to a new vaccine

Build a classification model that accurately predicts the response of individuals to new vaccines and provides actionable insights on how to reduce the spread of contagious infections.
### Metrics of Success
The final model will be considered a success if it has an accuracy and f1 score of not less 75%. The goal is to make as accurate as possible predictions, that is why the choice of success metrics is the accuracy score and f1 score.
## Data Understanding
### Data Source
The data used for the project was retrieved from [DrivenData](https://www.drivendata.org/competitions/66/flu-shot-learning/page/210/)
### Data Description
The dataframe contains 26707 observations and 35 features. The data on the training features (the input variables that the model will use to predict the probability that people received H1N1 flu vaccines and seasonal flu vaccines) contains 35 feature columns in total, each a response to a survey question.
## Data Preparation
The data underwent cleaning and preprocessing processes that would ensure it was in the right form for modeling. This was done dealing with missing values by dropping and filling in. The duplicates were also dropped and categorical data was encoded using label encoding. In EDA trends in the distrinution and correlation of the features and the target was established.
## Modeling
In this section, four models were built. The first was the base model; a simple logistic regression model that was fitted on the training set before any feature selection was done. Fitting this model to the test data resulted in a very weak f1 score of 43%, and regardless of the contrasting higher accuracy score, the model was considered a poor performing model. In an attempt to improve our results, feature selection was performed and the most important features used to fit the second model which was KNN. This, however, proved to be performing even worse than the previous one with an f1 score of 36%. For the third model, we built a decision tree that resulted in an f1 score of 36%, still a poor performance. Following the same kind of results after building three models, there was need to do more to improve the outcome. It was at this point that hyperparameter pruning was carried out on the decision tree model and an improvement in the f1 score was seen at 78%.
## Evaluation
The final model had an accuracy score of 80% and f1 score of 78%. Both surpassed previously set success metrics of an accuracy score and f1 score of 75%.
## Recommendations and Future Steps
* The public health sector should carry out more research on how people responded to other vaccines because while this model may provide important insight, it may not be as conclusive as a weighted outcome of several different vaccine types.
* Surveys like the one that led to getting the dataset used in this project are not very effective since they are done on phone. Individuals answer more truthfully in person, because of lack of this, the dataset ended up with a lot missing values.
* Seeing as to how the model was performing poorly at first continously, in the future, the data preprocessing processes need to be improved.
* From evaluating the distribution of H1N1 vaccine, it was established that only around 20% of the individuals had taken the vaccine. The public health organization in charge should look deeper into the reasons behind people not wanting to take the vaccine. It could be that they are not concerned enough, or do not have enough knowledge because it was established during EDA that with increase in levels of concern and knowledge about the vaccine by individuals, the higher the chances were of them taking the vaccine.
