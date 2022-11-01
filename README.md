<h1> Advanced-Regression-House-Price-Prediction </h1> 

##Brief description of the project:

- A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. 
The data is provided in the CSV file below.

The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

#The company wants to know:

Which variables are significant in predicting the price of a house, and

How well those variables describe the price of a house.

Also, determine the optimal value of lambda for ridge and lasso regression.


## General Information

- You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. 
They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.


Data Definitions: https://cdn.upgrad.com/UpGrad/temp/87f67e28-c47e-4725-ae3c-111142c7eaba/data_description.txt

Dataset: https://ml-course3-upgrad.s3.amazonaws.com/Assignment_+Advanced+Regression/train.csv

### EDA Analysis:
- Analyzed data with different visualization plots.
- There are few outliers and they are removed.
- There are few missing values and filled those missing values with appropriate choice( zero or mean or median or 'None').
 From the correlation plot, one can observe that a lot of corrleated features are in the data set, I followed RFE and regularization method to remove correlated features and selected the final set of best predictor variables.

##Model Building and Evaluation Conclusion:

- Both Ridge and Lasso regressions performed similar on this dataset, However I would like to take Lasso as the best performed model because of fewer predictor variables.

- Ridge Regression Performance:
  - Ridge Number of non-zero Coefficients 50
  - MSE Train 0.0011340223199113653
  - RMSE Train 0.03367524788195872
  - MAE Score Train 0.023621151194653998
  - R2 Score Train 0.9037419157664696 

  - MSE Test 0.0011608495220026408
  - RMSE Test 0.03407124186176137
  - MAE Score Test 0.02477157200853807
  - R2 Score Test 0.8979619290976839 

- Lasso Regression Performance:
  - Lasso Number of non-zero Coefficients 30
  - MSE Train 0.001154427841141163
  - RMSE Train 0.03397687215064334
  - MAE Score Train 0.0237527385178099
  - R2 Score Train 0.9020098542833054 

  - MSE Test 0.0011809747032773916
  - RMSE Test 0.03436531250079638
  - MAE Score Test 0.025035683883856817
  - R2 Score Test 0.8961929361016818 
 
- As you can see with the help of 30 predictor variables Lasso regression can achieve same results as Ridge regression.

- Top five features from Ridge regression are ,GrLivArea,OverallQual_10,1stFlrSF,2ndFlrSF,BsmtFinSF1
- The Optimum Lamda Value(regularization parameter) for Ridge regression is 2

- Top five features from Lasso regression are ,GrLivArea,OverallQual_10,OverallQual_9,TotalBsmtSF,YearBuilt
- The Optimum Lamda Value(regularization parameter) for Lasso regression is 0.0001

- All assumptions of Multiple Linear Regression are met( Homoscedasticity, error terms are normal distributed, error terms are independent of each other, linear relationship between predictor variables and Target variable)

- Most Dominent Features:
    - GrLivArea: Above grade (ground) living area square feet
    - OverallQual: Rates the overall material and finish of the house
       - 10	Very Excellent
       - 9	Excellent
    - TotalBsmtSF: Total square feet of basement area
    - YearBuilt: Original construction date
	
## Technologies Used
- pandas - version 1.2.4
- numpy - version 1.20.1
- seaborn - version 0.11.1
- matplotlib - version 3.3.4
- scikit-learn - version 1.0.2
- statsmodels - version 0.13.2

## Acknowledgements
Give credit here.
- This project was inspired by Upgrad(IIITB) Advanced-Regression-House-Price-prediction.

## Contact
Created by [@yalagamsrinivas] - feel free to contact us!

