# Capstone - Optimizing Fundraising Memberships 


## Contact 
If you want to contact me you can reach me at contactbethford@gmail.com

  
## Files
* EDA_NewFeatures_ClassificationScore.ipynb - Initial Python exploratory data analysis and new features
* README.md


## Data
Data was taken from a competition proposal run by APRA American Prospect Research Association. Apra is “Apra is committed to serving, representing and advancing the professionals and practices that enable the philanthropic success of institutions that rely on fundraising to achieve their missions” Who We Are (aprahome.org) 



**Modeling**
- KMeans model to create personae clusters to use for marketing
- Regression model with Grid Search and cross validation to identify target of top donors


**Overall Findings**
- Optimal Elbow reached all the way to 20 different clusters. To make the clusters more usable for the business, I may consider creating new fields upon which to cluster

![Picture of elbow curve at 20.](/images/Elbow.png)



## Recommendations
- Create a score and new fields to be more descriptive and not so many correlated fields.