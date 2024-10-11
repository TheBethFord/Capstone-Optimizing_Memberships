# Capstone - Optimizing Fundraising Memberships 


## Contact 
If you want to contact me you can reach me at contactbethford@gmail.com

  
## Overview
* Analysis and Modeling designed to optimize fundraising operations, especially as total gifts decline yearly. ![Picture of gifts by year.](/images/GiftsByYear.png) 

So we are looking to understand the following questions:

1. Who Donors Are, create personaes for marketing using K Means Cluster
2. How to Identify Top Donors, using Logistic Regression
3. How to Assign the Right Solicitor to Make Donors Successful, using a RandomForestClassifier


## Files
* EDA_NewFeatures_ClassificationScore.ipynb - Initial Python exploratory data analysis and new features
* Fundraising_Operations_Optimization.ipynb - Final file with clusters, regression and classifications
* README.md


## Data
Data was taken from a competition proposal run by APRA American Prospect Research Association. Apra is “Apra is committed to serving, representing and advancing the professionals and practices that enable the philanthropic success of institutions that rely on fundraising to achieve their missions” Who We Are (aprahome.org) 


## Data Exploration and Feature Engineering
One file was created, joining the three seperate files. Fundraising data was then aggregated by infidual in order to see totals and means of financial activities. Additonal columsn like year and month.  Trending data was added by looking to see who increased their gift YoY. A success factor was added calculated by adding both flags to see if they were a top donor as well as trending up.  This factor was appended to solicitors in order to make the target classification variables of successful solicitors.

## Modeling
- KMeans model to create personae clusters to use for marketing ![Picture of elbow curve at 19.](/images/Elbow.png)
- Regression model with Grid Search and cross validation to identify target of top donors
- Classification models (Logistic Regression, RandomForestClassifier, SVM, KNN). After running through four models, RandomForestClassifier came out as the strongest model.  In order to optimize that model, I ran a gridsearch of 243 fits to find the best parameters, resulting in a maximum depth of 30 with 200 trees being built by n_estimators=200.  The mean CV score of these tree was 43% ![Picture of random forest.](/images/RandomForest.png)


## Overall Findings and Recommendations
- Optimal Elbow reached all the way to 20 different clusters. To make the clusters more usable for the business, I may consider creating new fields upon which to cluster in order to try and decrease the total personaes more usable for marketing. 
- Look for additonal data sets that included demographic and psycographic information to humanize the personaes.
- I do not think that the Logistic Regression drove enough insight nor did it produce a very high F1 score.  Due to this, I would use heurisic measurements to identify top donors and it is also easier to explain to clients when you identify giving above the mean.
- Use the best model from the RandomForestClassifer to predict when new donors come into the database, is there a preferred solicitor to optimize their giving. 
- The strongest predictions came with Lurleen Gownge, Kipp Anespie, Brnba Donaghy, Reggie Egginson and Rodd Hanretty
- Overall the features that were most important to successful placement were monetary features, however the assigmnet units of DXO and the Law School were the most omportant categorical features.