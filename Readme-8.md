**“The Best Prediction of Sales” Project**
https://colab.research.google.com/drive/19qOqJMtzuyDXu2TIPS9lM_P63ffJ6GmY

**Author**: Samah Iriqat

**Overview**
The Best Prediction of Sales Project is a project for predicting the best model for the coming years 2024 and above, which will be chosen from different models and scenarios about specific outlet sales in 4 supermarkets depending on adata collected for a time series (1985-2009) for specific features appearing in the data frame.

Our stakeholders are: Owners of supermarkets.

Their primary goal is: Increase the outlt sales for specific itm whih wer sales in supermarkets.

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

As a result of prediction the best model is the regression prediction (Random Forest Model) because it appears to be the most suitable for production, which have the minimum error with a high accuracy; and it describes more than the half of the variance for outlet sales and also it has the minimum error in the other metricsvariable that's explained by an some features according to the following issues:

**Model 1: Linear Regression**:
The following are the metrics found for the best estimater for Linear Regression train and test data: Mean Squared Error (MSE), Root Mean Squared Error (RMSE), R-squared (R2) and Mean Absolute Error (MAE): 
R-squared (train): 0.65
R-squared (test): -6064525988327.72
MAE (train): 752.48
MAE (test): 179573195.29
MSE (train): 1027287.28
MSE (test): 16483200104496646144.00
RMSE (train): 1013.55
RMSE (test): 4059950751.49

**Graph (5): Affected features in Outlet Sales**
![image](https://github.com/user-attachments/assets/1032c69d-9234-43c0-ab3d-39b2e730ef2f)

The best 3 coefficients that affect the prediction of outlet sales are reasons related to outlet not item, these coefficients are; outlet type supermarket, outlet idntidier (OUT035) and outlet location type tier.
, and thir affect depends on the value of the cosfficient, so the most affect is outlet type supermarket, then outlet location type tier, then utlet idntidier (OUT035).
1- Outlet_Type_Supermarket Type3: 1249988156654456.25
2- Outlet_Identifier_OUT035: 1278535293288521.25
3-Outlet_Location_Type_Tier 1: 1288675199406667.25

**Model 2: Random Forest**:
The following are the metrics found for the best estimater for Random Forest train and test data: Mean Squared Error (MSE), Root Mean Squared Error (RMSE), R-squared (R2) and Mean Absolute Error (MAE): 
R-squared (train): 0.52
R-squared (test): 0.51
MAE (train): 855.29
MAE (test): 843.99
MSE (train): 1348922.18
MSE (test): 1315080.08
RMSE (train): 1161.43
RMSE (test): 1146.77

**Graph (6): Affected features in Outlet Sales**
![image](https://github.com/user-attachments/assets/9040dbba-ff48-40ad-bc2e-eef4ef021fae)

The best 5 coefficients that affect the prediction of outlet sales are reasons related to outlet not item, these coefficients are: item type soft drinks, outlet estableshment year, item type others), outlet identifier (OUT049) and outlet identifier (OUT046), and their affect depends on the value of the cosfficient, so the most affect is item type (other), then outlet establishment year, then outlet identifier (OUT046), thn with a negative affect:Outlet Identifier (OUT049) and itm typ soft drink.
Item_Type_Soft Drinks: -54606955382288.55
Outlet_Establishment_Year: 1563157510754344.50
Item_Type_Others: 76296992397315.31
Outlet_Identifier_OUT049: -54606955385767.59
Outlet_Identifier_OUT046: 117967247047643.22

## Recommendations:
We recommend to use this model for the next years, also working on improving the features affect outletsales and increase it.

## Limitations & Next Steps
The limittions that need to have in consideration is to have a continious time series in order to have a clear picture, also there is no need to contiue gathering since it sometimes it is a missleading data.

### For further information
For any additional questions, please contact **samaheriqat@gmail.com**


