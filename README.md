# dsc-3-final-project-online-ds-pt-112618

# Module 3 Final Project - Car Insurance Cold Calling Campaign


## Overview

The aim of this task is to predict for 1000 customers whether they will buy car insurance or not.

For this project, machine learning models will be employed.  Machine learning works on the development of computer programs that can access data and use it to automatically learn and improve from experience.  (i.e. – it’s a technique that uses statistics to help machines learn from past data). 
Specifically, supervised machine learning will be used in this project.  Supervised machine learning is a method that enables the machine to classify and predict objects, problems or situations based on labeled data.  With this type of model, your data is labeled, direct feedback is given, and the machine predicts the output.  

## Problem Statement

The client would like to know the most important factor that determines cold calling success.  So we’ll use predictive models (i.e. – Machine Learning techniques) to see which factor(s) are successful.

## Data Source Overview

Contains consumer information from a company conducting cold calling.  The dataset contains general info (i.e. – age, education, job, etc.) and cold calling info (i.e. – communication, last contact, previous contact attempts, etc.). 

The dataset was obtained from Kaggle: https://www.kaggle.com/kondla/carinsurance.

## Scrubbing the Data

The data was in fairly great shape, so not much was done in terms of scrubbing. It consisted of a few rows and columns, and there were some columns with null values within the dataset that were fairly easy to fix.

## Exploratory Data Analysis

I created some bar plots with error bars with certain features on the x-axis and Car Insurance along with y-axis.  The graphs showed me some interesting trends like potential customers with advanced degrees are likely to purchase car insurance, and single people are also likely to buy insurance.  Also, those who are students, retired and unemployed purchased the most insurance.  Lastly, car insurance sells appear to peak in March, Sept, Oct, and Dec.  

<img src='https://github.com/Sugaboo/dsc-3-final-project-online-ds-pt-112618/blob/master/mod3graph1.png'>

<img src='https://github.com/Sugaboo/dsc-3-final-project-online-ds-pt-112618/blob/master/mod3graph2.png'>

## Predictive Modeling

Since I was focusing on classification for my predictive modeling, I choose to run the following: K-Nearest Neighbors (kNN), Logistic Regression, Support Vector Machine (SVM), Decision Tree and Random Forest.  These models are examples of Supervised machine learning.  

With each predictive model, confusion matrices would be needed.  Confusion matrices are helpful because they assess the accuracy of each model used.  Basically, they’re a summary of prediction results on your classification problem.  

<img src='https://github.com/Sugaboo/dsc-3-final-project-online-ds-pt-112618/blob/master/mod3graph3.png'>

I’m interested in the percentage of the true positive and true negative values / the total count.  So that would be the values in the darkest blue squares (346+288 / 800 = 0.79).  If you multiply 0.79 x 100, this would generate 79%.  So, my confusion matrix for this model shows an accuracy of 79%.  For the models, my confusion matrices accuracy were:

* 	K-Nearest Neighbors (kNN): 73%
* 	Logistic Regression: 80%
* 	SVM: 80%
* 	Decision Tree: 81%
* 	Random Forest: 84%

<img src='https://github.com/Sugaboo/dsc-3-final-project-online-ds-pt-112618/blob/master/Mod3_Random%20Forest%20CM.png'>

Overall, Random Forest was the most accurate model and yielded the highest percentage of accuracy.  Additionally, I wanted to know which features in this data set were the most important.  This would help with the cold calling efforts as it would most likely drive the most sales.  I used the ExtraTreesClassifer in Sklearn and generated the following graph of the top 5 features: 

<img src='https://github.com/Sugaboo/dsc-3-final-project-online-ds-pt-112618/blob/master/mod3graph4.png'>

The graph above showed that the Call Time (i.e. – time on the phone with potential customers) was the top feature in this data set.  Last Contact Day also showed that potential customers who were contacted regularly seemed more likely to purchase car insurance.

## Conclusions

* Based on the predictive modeling, Random Forest had the highest percentage of 84%, and a cross validation score of 84%. 

* Interestingly, Call Time had the most effect on customers who were cold called. Last Contact Day also showed would be more likely to purchase car insurance.

* Potential customers with tertiary (advanced) educations are more likely to purchase insurance.

* Single people are more likely to purchase insurance.

* Students, retired and unemployed people are purchasing the most car insurance polices.

* Many people buy insurance in March, September, October and December.

## Future Work

* Try other methods of machine learning (i.e. - Unsupervised or possibly Reinforecement).

* Analyze the dataset using other Supervised machine learning models.

* Explore any Deep Learning or AI methodology to the dataset.
