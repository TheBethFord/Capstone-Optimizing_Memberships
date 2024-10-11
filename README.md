# Capstone - Optimizing Fundraising Memberships 


## Contact 
If you want to contact me you can reach me at contactbethford@gmail.com

  
## Overview
* Analysis and Modeling designed to optimize fundraising operations, especially as total gifts are celining each year. ![Picture of gifts by year.](/images/GiftsByYear.png)
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


## Modeling
- KMeans model to create personae clusters to use for marketing ![Picture of elbow curve at 19.](/images/Elbow.png)
- Regression model with Grid Search and cross validation to identify target of top donors
- Classification models (Logistic Regression, RandomForestClassifier, SVM, KNN). After running through four models, RandomForestClassifier came out as the strongest model.  In order to optimize that model, I ran a gridsearch of 243 fits to find the best parameters, resulting in a maximum depth of 30 with 200 trees being built by n_estimators=200.  The mean CV score of these tree was 43%


## Overall Findings
- Optimal Elbow reached all the way to 20 different clusters. To make the clusters more usable for the business, I may consider creating new fields upon which to cluster in order to try and decrease the total personaes.





## Recommendations
- Create a score and new fields to be more descriptive and not so many correlated fields.