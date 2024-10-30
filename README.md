**“The Best Prediction of Sales” Project**

**Author**: Samah Iriqat

**Overview**
The Best Prediction of Sales Project is a project for predicting the best model for the coming years 2024 and above, which will be chosen from different models and scenarios about specific outlet sales in 4 supermarkets and stores depending on adata collected for a time series (1985-2023) for specific features appearing in the data frame.

### Business problem:

The problem with this project is to determine which features affect outlet sales and what is the best model to predict the outlet sales.

### Data:
This data was gathered from these supermarkets and stores, about specific items that the supermarkets and stores sales. It covers two main topics: items (identifier, wight, fat content, visibility, MPR) and outlet (identifier, establishment year, size, location type) which will be used to predict outlet sales.
There are 8523 record for 11 features as sows in the table below for the outlet sales and some fatures:

|index|Item\_Weight|Item\_Visibility|Item\_MRP|Outlet\_Establishment\_Year|Item\_Outlet\_Sales|
|---|---|---|---|---|---|
|count|7060\.0|8523\.0|8523\.0|8523\.0|8523\.0|
|mean|12\.857645184135976|0\.06613202877895108|140\.9927819781767|1997\.8318667135984|2181\.288913575032|
|std|4\.643456499186395|0\.051597822321135196|62\.27506651219039|8\.371760408092706|1706\.499615733832|
|min|4\.555|0\.0|31\.29|1985\.0|33\.29|
|25%|8\.77375|0\.0269894775|93\.8265|1987\.0|834\.2474|
|50%|12\.6|0\.053930934|143\.0128|1999\.0|1794\.331|
|75%|16\.85|0\.0945852925|185\.6437|2004\.0|3101\.2964|
|max|21\.35|0\.328390948|266\.8884|2009\.0|13086\.9648|

The below graph shows the distribution of outletsales by out let type:
![image](https://github.com/user-attachments/assets/9bf7bca8-d97c-4912-90d6-f9a68d257a43)

## Methods
The data was collectd from different outlets using the same data templete which includes the features that will be used to predict sales and the actual sales also. The data was prepared and analyse un the following steps:
1-	Before analysis the data and building the model, there is a need to check the data (drop duplicate, find null, fill missing values with appropriate values, check data type, Updated column names to match the data frame).
2-	The next step is to define the target and features, processing them using suitable.
3-	Analyze the data using different methods of prediction.
4-	Compare between those methods and determine the method that has the best prediction.

## Results


	




### Here are examples of how to embed images from your sub-folder


#### Visual 1 Title
![sample image](project1_sample_image.png)

> Sentence about visualization.

#### Visual 2 Title

## Model

As a result of prediction the best model is the  lqssificqtion regression prediction (Random Forest Technique), which have th minimum error with a high accuracy;in which R-squared: 00.8069287081198013, this means that this value describe approximately 81% of the variance for outlet sales variable that's explained by an some features.But MAE in Random Forest is much smaller than MAE in Linear Regression (2445.57 < 4177.05), so Random Forest has a smallest error as shown below: Linear Regression: MAE (train): 4181.90 MAE (test): 4177.05 MSE (train): 36979860.90 MSE (test): 35478020.68 RMSE (train): 6081.11 RMSE (test): 5956.34

Random Forest: Best Random Forest MAE: 2445.5727708585323 Best Random Forest MSE: 18120064.019785218 Best Random Forest RMSE: 4256.766850531659


## Recommendations:

We recommend to use this model in these supermarket and stores for the next years, also working on improving the features affect outletsales and increase it.


## Limitations & Next Steps

The limittions that need to have in consideration is to have a continious time series in order to have a clear picture, also there is no need to contiuegatheringsince it sometimes t is a missleading data.

### For further information


For any additional questions, please contact **samaheriqat@gmail.com**
