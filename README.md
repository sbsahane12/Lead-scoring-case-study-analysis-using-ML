# [Project  10:Lead scoring case study analysis using ML](https://github.com/sbsahane12/Lead-scoring-case-study-analysis-using-ML.git) 
## Problem Statement  
### Background  - Business Understanding   
- Building Logistic regression model & assigning Lead Scores to the prospective candidates of X Education
## Problem description
- X Education is an online Education company which has Lead database, some of which got converted & some didn‘t
- The typical lead conversion rate is 30% which is expected to be maximized to atleast 80%
- Target is to identify the ‘Hot Leads' which have a high conversion rate.
- The 'Hot Leads’ to be identified by cutoff Lead Scores Lead scores to be assigned to each candidates based on probabilities calculated by Logistic regression model

This project requires Python 3.6 and the following libraries installed:
- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [seaborn](https://seaborn.pydata.org/)
## Data Preparation  
- Data Inspection and Missing value treatment
- Dummy variable creation
- Logistic regression modelling
- Model Accuracy Check
- Model fit on testdata
- Conclusion
- Recommendations\

## Data Inspection and Missing value treatment
- Columns containing >70% missing data were dropped.
- ‘City’ column had ~40% missing values & was dropped
- In absence of any visible correlation with Activity & Profile, these columns were dropped too
- *Asymmetric Index columns were checked for any possible relation to impute missing values Other columns with possible imputations were handled appropriately

- Unique value columns : 
- Columns with only one type of unique values were dropped in absence of variability

- Imputation :
- High missing value containing columns were imputed with suitable values

## Model Building : 
- 15 Features were selected using RFE.
- Six Logistic regression models were built iteratively
- Final model was selected based on:
- p-values <0.05 for all variables, indicatingsignificance 2.VIF< 5, indicating absence of multicollinearity
- Model performancemeasures
- High values of Accuracy, Sensitivity & Specificity indicate good predictive powers of model.
- Low False positive rate indicates model’s ability to
- predict positive values accurately.
- ![image](https://user-images.githubusercontent.com/106218600/217209211-427e9944-a59d-4b3a-897a-ef0fc888c20e.png)

## Recommendations

🠜Toget more customers, XEducation must keep the lead score lower, starting at ‘0’. But to achieve target conversion of greater than 80%, it should keep the cut off at 30.
🠜Thus, in the model, data frame changed for cut off Lead Score to gauge the Conversion percentages w.r.t. actual converted.
🠜Lowering the lead score cut off reduces conversion %, but it increases
number of actual converted.
🠜Based on the man power availability with XEducation, it may decide to give weightage to conversion %oractual numbers.
