# Predicting Airline Customer Satisfaction 

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Imports and Packages](#imports-and-packages)
- [Data exploration data cleaning and model preparation](#Data-exploration-data-cleaning-and-model-preparation)
- [Model Building](#model-building)
- [Visualizations for model assessment](#visualizations-for-model-assessment)
- [Results and Considerations](#results-and-considerations)
- [Recommendations](#recommendations)
- [References](#references)


### Project Overview

This data analysis project aims to build a logistic regression model to predict customer service satisfaction for an airline company, it will also examine the impact/effect of inflight entertainment on customer satisfaction.
The model uses previous customer feedback data to train the model so that it can predict future customer satisfaction,
thereby helping improve customer service and satisfaction and ultimately customer retention and improved revenue generation and overall brand growth.

### Data Sources

The data for this activity includes survey responses from 129,880 airline customers. It includes data points such as class, flight distance, and in-flight entertainment, among others.

### Tools Used

  - Jupyter notebook [Download here](https://jupyter.org)
 
### Imports and Packages
The imports packages included:
1.	Pandas 
2.	Numpy 
3.	Matplotlib
4.	Train_test_split 
5.	LogisticRegression
6.	Sklearn.metrics, and OneHotEncoder 
7.	ProfileReport
The above imports and packages were used to generate a quick report, preprocess, do EDA, build, visualize, and evaluate the model
### Data exploration data cleaning and model preparation
#### Prepare the data
After loading the dataset, I prepared the data to be suitable for a logistic regression model. The steps included:
1. Exploring the data
2. Checking for and handling missing values and duplicates
3. Renaming columns appropriately
4. Encoding the data; The columns that were in object format were encoded using categorical encoding for the variables with inherent order and OneHotEncoder for the other variables without an order in their components.
5. Checking and handling outliers
6. Scaling variables that had significantly higher scales compared to other variables
### Visualizations from Data Exploration
1.	Boxplot of variables with suspected outliers
2.	Correlation heatmap of the variables
### Model building
#### The following steps were undertaken to build logistic regression(One and multiple features) and Naïve Bayes  models;
1.	Isolated the dependent and independent variables (y and X variables respectively)
2.	Split the data into training and testing sets, using the train_test_split method of sklearn
3.	Instantiated a logistic regression model.
4.	Then fit the model to the training dataset
5.	Predicted customer satisfaction (y) given inflight entertainment(X)
6.	Predicted customer satisfaction given inflight entertainment and other independent variables
7.	Considered the assumptions of the various models.  
### Visualizations for model assessment 
1.	#### Correlation heatmap

  	![Correlation heatmap of features](https://github.com/mena88/Airline_Customer_Satisfaction_Predictor/assets/97759151/ff21d383-e50d-4446-b2fe-72da7611e374)
  	The correlation heatmap above was used to visualize the correlation coefficient of the variables
  	
3.	#### Logistic regression plot

  	![Regresion plot of satisfaction vs inflight entertaiment](https://github.com/mena88/Airline_Customer_Satisfaction_Predictor/assets/97759151/4d31b206-b981-4ab9-80e3-09404e73f4dc)

  	The logistis regression plot above demonstrates a sigmoid curve, characteristic of logistic regression. The plot represents a monotonic relationship between 
    satisfaction and inflight entertainment, as inflight entertainment rating increased so did the probability of the customers being satisfied.


4.	#### Confusion matrix diagram

  	![Confusion matrix daigram](https://github.com/mena88/Airline_Customer_Satisfaction_Predictor/assets/97759151/ff95eeb7-37aa-4153-898e-cb36f80bc4cc)

   From our diagram of the total test set, our model had a true positve prediction of 17423 and true negative prediction of 13714 The value of the false positve 
   prediction 
   was 3925 while the false neagtive prediction was 3785
   From our diagram, our model did well with identifying a significant amount of the customers who were satisfied and not satisfied.
   The number of customers that were wrongly classified were not also too high, it made slightly more type 1 errors than type 2 errors.

   
### Model Evaluation
#### The following steps were taken
1. Obtain parameter estimates (coefficients and intercepts)
2. Print out models Accuracy, Precision, Recall, F1 Score and ROC_AUC score
3. Plot Confusion matrix diagram
3. Derive insight from the values in 1 and 2 above

### Results and Considerations 
1. Our model did well over all in predicting outcomes from the text set.
2. From our analysis, the odds ratio (Exponentiated Coefficient) is approximately 2.711. This means that for each one-unit increase in Inflight_entertainment, the odds of a passenger being satisfied are 2.711 times higher or a 171% increase in the odds of being satisfied, holding all other variables constant. This suggests a strong positive relationship between Inflight_entertainment and passenger satisfaction. Thus, as the quality or availability of Inflight_entertainment increases, passengers are significantly more likely to be satisfied
3. With an intercept of -3.19355406, and an odds_ratio ofs 0.04, the adsence of inflight entertainment or it's low rating, will also translate to a low likelihood of customers being satisffied, with the chance of being satisfied in this insance being 4% 4%
4. Our model's errors, both type 1 and 2 were similar and not too high

### Recommendations 
**Our recommendations to stakeholders would be to:**
1. Not compromise on inflight entertainment
2. Consider constantly improving content variety and quality; This may involve, frequent update, offering content in multiple languages, expanding content library and providing varying video and audio quality.
3. Ensure the systems are interactive and can be personalized
4. Ensure easy connectivity and accessibility
5. Get customer feedbacks and implement them
6. Consider investing in building more advanced models that could yield better results

### References
1. Google Advanced Data Analytics Course Resources
2. Google
3. StackOverflow
4. StackUp
5. ChatGPT
