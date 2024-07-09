# Prediction-of-Product-Sales
- Author: Alaa Zagha
## Project Overview:
Sales prediction for food items sold at various stores. The goal of this is to help the retailer understand the properties of products and outlets that play crucial roles in increasing sales.
## Data
- Download the data using this link: [download the data] (https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/)).
## Methods
- Business understaniding , then data cleaning to make it ready for ML, by fixing the inconsistent values there were inconsistent values in Item_Fat_Content feature, also finding the approach of imputing the missing values
- feature inspection to know which feature can help to predict the target
- preprocessing for modeling
- modeling
- evaluation
## Results
### Heatmap of Correlation to understand the relations between the features
![download](https://github.com/alaazagha/Prediction-of-Product-Sales/assets/170015439/79b397e4-6e46-4656-a385-e36829db10bd)

- there's a good positive correlation between Item_MRP and Outlet_sales, the higher the price of product higher sales
### Item_Itdentifier
![Identifier](https://github.com/alaazagha/Prediction-of-Product-Sales/assets/170015439/4ae9e971-8820-4814-a5f7-074feaca80b7)

- This feature will be excluded for high cardinality
### Outlet_Type
![outlettype](https://github.com/alaazagha/Prediction-of-Product-Sales/assets/170015439/ac4a9268-b422-4f63-b2ab-ad7e14a910d3)

- This is a good feature to predict the target
### MRP 
- ![mrp](https://github.com/alaazagha/Prediction-of-Product-Sales/assets/170015439/0861e8d7-a5b4-446b-a26a-834cb313c544)
- This shows the distribution of MRP 
- ![mrpvssales](https://github.com/alaazagha/Prediction-of-Product-Sales/assets/170015439/2b3904c3-21e9-49ba-902f-e10546fe4494)
- This shows how good the relation between the target and MRP
## Modeling
3 models were tried to predict the sales, Linear Regression,Default RandomForest and Tuned RandomForest
### Tuned RandomForest Result
![Tuned RandomForest](https://github.com/alaazagha/Prediction-of-Product-Sales/assets/170015439/a3d5ea3f-7a79-46ab-95f0-5d84e6311cc8)

- The model is doing better than the default hyperparameters, less overfit than the default and the linear regression model, also has the lowest error rate which is 34%, The MAE and RMSE means that if the prediction value is compared with the real value this would be the difference between them so there will be a 1064 USD difference betweeen the prediction value of sales and the real value of sales if using the RMSE to evaluate if choosing the MAE it will be 742 USD
