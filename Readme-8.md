**“The Best Prediction of Sales” Project**

**Author**: Samah Iriqat

**Overview**
The Best Prediction of Sales Project is a project for predicting the best model for the coming years 2024 and above, which will be chosen from different models and scenarios about specific outlet sales in 4 supermarkets and stores depending on adata collected for a time series (1985-2009) for specific features appearing in the data frame.

Our stakeholders are: Owners of supermarkets.

Their primary goal is: Increase the outlt sales for specific itm whih wer sales in supermarkets.

They plan to:Build the best model to predict the maximum sales and determining the which features affect outlt sales.

What do they need/expect? Actionable insights/recommendations for which modifications they can make to increase the outlt sales.

### Business problem:

The problem with this project is to determine which features affect outlet sales and what is the best model to predict the outlet sales.

### Data:
This data was gathered from these supermarkets, about specific items that the supermarkets and stores sales. It covers two main topics: 
Items (identifier, wight, fat content, visibility, MPR).
Outlet (identifier, establishment year, size, location type) which will be used to predict outlet sales.

There are 8523 record for 11 features as sows in the table below for the outlet sales and some fatures:

**“The Best Prediction of Sales” Project**

**Author**: Samah Iriqat

**Overview**
The Best Prediction of Sales Project is a project for predicting the best model for the coming years 2024 and above, which will be chosen from different models and scenarios about specific outlet sales in 4 supermarkets and stores depending on adata collected for a time series (1985-2009) for specific features appearing in the data frame.

Our stakeholders are: Owners of supermarkets and store.

Their primary goal is: Increase the outlt sales for specific itm whih wer sales in those places.

They plan to:Build the best model to predict the maximum sales and determining the which features affect outlt sales.

What do they need/expect? Actionable insights/recommendations for which modifications they can make to increase the outlt sales.

### Business problem:

The problem with this project is to determine which features affect outlet sales and what is the best model to predict the outlet sales.

### Data:
This data was gathered from these supermarkets and stores, about specific items that the supermarkets and stores sales. It covers two main topics: 
Items (identifier, wight, fat content, visibility, MPR).
Outlet (identifier, establishment year, size, location type) which will be used to predict outlet sales.

There are 7440 record for 11 features as sows in the table below for the outlet sales and some fatures:

|index|Item\_Weight|Item\_Visibility|Item\_MRP|Outlet\_Establishment\_Year|Item\_Outlet\_Sales|
|---|---|---|---|---|---|
|count|6505\.0|7440\.0|7440\.0|7440\.0|7440\.0|
|mean|12\.852909300538046|0\.060494275283064516|141\.09439970430108|1998\.7299731182795|2449\.3402075806453|
|std|4\.644189069695718|0\.044468455081640344|62\.35543195672849|8\.233718947390345|1661\.527021486382|
|min|4\.555|0\.0|31\.29|1985\.0|69\.2432|
|25%|8\.77|0\.02603684875|93\.90215|1987\.0|1193\.1136|
|50%|12\.6|0\.049513225|142\.7483|1999\.0|2075\.9644|
|75%|16\.85|0\.08794341775|185\.8648|2004\.0|3327\.6684|
|max|21\.35|0\.188619537|266\.8884|2009\.0|13086\.9648|


## Methods
The data was collectd from different outlets using the same data templete which includes the features that will be used to predict sales and the actual sales also. The data was prepared and analyse un the following steps:
1-	Before analysis the data and building the model, there is a need to check the data (drop duplicate, find null, fill missing /unlogical values with appropriate values, check data type, Updated column names to match the data frame, convert data from string to numeric as needed, combine/sparated fatures if neded,check if th Is the feature constant or quasi-constant,check the cardinality:is it high or low, encode categorical / ordinal data with the approriate encodrs, ..)
2-	The next step is to define the target and features, processing them using suitable.
3-	Analyze the data using different methods of prediction.
4-	Compare between those methods and determine the method that has the best prediction (evaluation).


![image](https://github.com/user-attachments/assets/39cab705-bedc-48a8-bbac-32a9652d5572)


## Results
To test which features affect the outlet sales, first we will distinguish which items exist in the data frame as shown in graph (1) below:

#### Graph (1): Distribution of outleat slaes
![image](https://github.com/user-attachments/assets/b348784b-99c2-4753-ab7a-78ea20ab6122)

The gaph shows the values of outlet sales and there are cheap outlets and expensive outlets wich cost more than 13,000.

#### Graph (2): Distribution of Items by Visibility
![image](https://github.com/user-attachments/assets/50cb35e8-5f21-4443-a1f7-50c0eabfef6b)

The graph shows the items sales according to their visibility in stores and supermarkets, in which it has the maximum visibilityn is for seafood value in store.

#### Graph (3): Distribution of Items by Establishment Year
![image](https://github.com/user-attachments/assets/4d1a8598-7029-44ef-a052-a2ca3ca9ad3d)

The graph shows the items sales according to their Establishment years, in which there is a missing data for specific years. 

#### Graph (4): Distribution of Outletsales by Outlet Type
The below graph shows the distribution of outletsales by outlet type:
![image](https://github.com/user-attachments/assets/7d64cff5-508c-4f11-907c-0928d7f503fd)

The graph shows the items sales according to their establishment years, in which it has the minimum value in supermarket type2.

## Model

As a result of prediction the best model is the regression prediction (Random Forest Model) because it appears to be the most suitable for production, which have the minimum error with a high accuracy; in which R-squared: 00.8069287081198013, this means that this value describe approximately 81% of the variance for outlet sales variable that's explained by an some features according to the following issues:

For Linear Regression:
R-squared (train): 0.73
R-squared (test): 0.81

For Random Forest:
Training R-squared: 0.7299057809339075
Test R-squared: 0.8069287081198013

The values of R-square in both Linear Regession are approximately the same in Random Forest.

But MAE in Random Forest is much smaller than MAE in Linear Regression (2445.57 < 4177.05), so Random Forest has a smallest error as shown below:
Linear Regression:
MAE (train): 4181.90
MAE (test): 4177.05
MSE (train): 36979860.90
MSE (test): 35478020.68
RMSE (train): 6081.11
RMSE (test): 5956.34

Random Forest:
Best Random Forest MAE: 2445.5727708585323
Best Random Forest MSE: 18120064.019785218
Best Random Forest RMSE: 4256.766850531659

We usd othr modls and eevalute them, then comparing between the result we note the following:

1. Recall Score: While the KNN model and the Logistic Regression model achieved similar results for recall, precision and f1-score, in the classification report of the best model, the Logistic Regression shows better performance in the recall score. In this case, a high recall is crucial because we want to minimize false negatives (predicting no stroke when one actually occurs). A higher recall means we are better at identifying actual stroke cases, which is more important than minimizing false positives.
2. Model Interpretability: Logistic Regression models are generally more interpretable than KNN models. This means that we can understand the factors contributing to the model's predictions, making it easier to identify important variables and potential biases. Interpretability is often critical in healthcare settings for building trust and ensuring ethical decision making.
3. Computational Efficiency: Logistic regression is generally faster to train and predict than KNN, especially with larger datasets. While the dataset in this code is relatively small, this becomes a larger factor in cases where the dataset is larger.
4. Robustness to Outliers: While not explicitly addressed, logistic regression may be more robust to outliers than KNN. KNN's predictions are highly influenced by nearby data points. Outliers can distort these predictions, making logistic regression a safer bet in cases where outliers are present.


## Recommendations:

We recommend to use this model for the next years, also working on improving the features affect outletsales and increase it.


## Limitations & Next Steps

The limittions that need to have in consideration is to have a continious time series in order to have a clear picture, also there is no need to contiue gathering since it sometimes it is a missleading data.

### For further information


For any additional questions, please contact **samaheriqat@gmail.com**


## Methods
The data was collectd from different outlets using the same data templete which includes the features that will be used to predict sales and the actual sales also. The data was prepared and analyse un the following steps:
1-	Before analysis the data and building the model, there is a need to check the data (drop duplicate, find null, fill missing /unlogical values with appropriate values, check data type, Updated column names to match the data frame, convert data from string to numeric as needed, combine/sparated fatures if neded,check if th Is the feature constant or quasi-constant,check the cardinality:is it high or low, encode categorical / ordinal data with the approriate encodrs, ..)
2-	The next step is to define the target and features, processing them using suitable.
3-	Analyze the data using different methods of prediction.
4-	Compare between those methods and determine the method that has the best prediction (evaluation).


![image](https://github.com/user-attachments/assets/39cab705-bedc-48a8-bbac-32a9652d5572)


## Results
To test which features affect the outlet sales, first we will distinguish which items exist in the data frame as shown in graph (1) below:

#### Graph (1): Distribution of outleat slaes
![image](https://github.com/user-attachments/assets/b348784b-99c2-4753-ab7a-78ea20ab6122)

The gaph shows the values of outlet sales and there are cheap outlets and expensive outlets wich cost more than 13,000.

#### Graph (2): Distribution of Items by Visibility
![image](https://github.com/user-attachments/assets/5cc73dc5-91b4-44fb-9f05-8cfab3cdff2d)

The graph shows the items sales according to their visibility in stores and supermarkets, in which it has the maximum visibilityn is for seafood value in store.

#### Graph (3): Distribution of Items by Establishment Year
![image](https://github.com/user-attachments/assets/e2b90d1c-e5cc-42ab-bf09-273f7bf1782a)

The graph shows the items sales according to their Establishment years, in which there is a missing data for specific years. 

#### Graph (4): Distribution of Outletsales by Outlet Type
The below graph shows the distribution of outletsales by outlet type:
![image](https://github.com/user-attachments/assets/9bf7bca8-d97c-4912-90d6-f9a68d257a43)

The graph shows the items sales according to their establishment years, in which it has the minimum value in Grocery store.

## Model

As a result of prediction the best model is the regression prediction (Random Forest Model) because it appears to be the most suitable for production, which have the minimum error with a high accuracy; in which R-squared: 00.8069287081198013, this means that this value describe approximately 81% of the variance for outlet sales variable that's explained by an some features according to the following issues:

For Linear Regression:
R-squared (train): 0.73
R-squared (test): 0.81

For Random Forest:
Training R-squared: 0.7299057809339075
Test R-squared: 0.8069287081198013

The values of R-square in both Linear Regession are approximately the same in Random Forest.

But MAE in Random Forest is much smaller than MAE in Linear Regression (2445.57 < 4177.05), so Random Forest has a smallest error as shown below:
Linear Regression:
Mean Squared Error (MSE): 3.643354698251804e+25
Root Mean Squared Error (RMSE): 6036020790431.2295
R-squared (R2): -1.3404690298105391e+19
Mean Absolute Error (MAE): 357326046526.239

MAE (train): 4181.90
MAE (test): 4177.05
MSE (train): 36979860.90
MSE (test): 35478020.68
RMSE (train): 6081.11
RMSE (test): 5956.34

Random Forest:
Best Random Forest MAE: 2445.5727708585323
Best Random Forest MSE: 18120064.019785218
Best Random Forest RMSE: 4256.766850531659

We used other modls and evalute them, then comparing between the result we note the following:

1. Recall Score: While the KNN model and the Logistic Regression model achieved similar results for recall, precision and f1-score, in the classification report of the best model, the Logistic Regression shows better performance in the recall score. In this case, a high recall is crucial because we want to minimize false negatives (predicting no stroke when one actually occurs). A higher recall means we are better at identifying actual stroke cases, which is more important than minimizing false positives.
2. Model Interpretability: Logistic Regression models are generally more interpretable than KNN models. This means that we can understand the factors contributing to the model's predictions, making it easier to identify important variables and potential biases. Interpretability is often critical in healthcare settings for building trust and ensuring ethical decision making.
3. Computational Efficiency: Logistic regression is generally faster to train and predict than KNN, especially with larger datasets. While the dataset in this code is relatively small, this becomes a larger factor in cases where the dataset is larger.
4. Robustness to Outliers: While not explicitly addressed, logistic regression may be more robust to outliers than KNN. KNN's predictions are highly influenced by nearby data points. Outliers can distort these predictions, making logistic regression a safer bet in cases where outliers are present.


## Recommendations:

We recommend to use this model for the next years, also working on improving the features affect outletsales and increase it.


## Limitations & Next Steps

The limittions that need to have in consideration is to have a continious time series in order to have a clear picture, also there is no need to contiue gathering since it sometimes it is a missleading data.

### For further information


For any additional questions, please contact **samaheriqat@gmail.com**
