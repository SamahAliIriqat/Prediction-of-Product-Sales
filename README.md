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



## Methods
The data was collectd from different outlets using the same data templete which includes the features that will be used to predict sales and the actual sales also. The data was prepared and analyse un the following steps:
1-	Before analysis the data and building the model, there is a need to check the data (drop duplicate, find null, fill missing values with appropriate values, check data type, Updated column names to match the data frame).
2-	The next step is to define the target and features, processing them using suitable.
3-	Analyze the data using different methods of prediction.
4-	Compare between those methods and determine the method that has the best prediction.

## Results
Th 

	



I recomend Logistic Regressio for production, because it appears to be the most suitable for production.

1. Recall Score: While the KNN model and the Logistic Regression model achieved similar results for recall, precision and f1-score, in the classification report of the best model, the Logistic Regression shows better performance in the recall score. In this case, a high recall is crucial because we want to minimize false negatives (predicting no stroke when one actually occurs). A higher recall means we are better at identifying actual stroke cases, which is more important than minimizing false positives.
2. Model Interpretability: Logistic Regression models are generally more interpretable than KNN models. This means that we can understand the factors contributing to the model's predictions, making it easier to identify important variables and potential biases. Interpretability is often critical in healthcare settings for building trust and ensuring ethical decision making.
3. Computational Efficiency: Logistic regression is generally faster to train and predict than KNN, especially with larger datasets. While the dataset in this code is relatively small, this becomes a larger factor in cases where the dataset is larger.
4. Robustness to Outliers: While not explicitly addressed, logistic regression may be more robust to outliers than KNN. KNN's predictions are highly influenced by nearby data points. Outliers can distort these predictions, making logistic regression a safer bet in cases where outliers are present.

### Here are examples of how to embed images from your sub-folder


#### Visual 1 Title
![sample image](project1_sample_image.png)

> Sentence about visualization.

#### Visual 2 Title

## Model

Describe your final model

Report the most important metrics

Refer to the metrics to describe how well the model would solve the business problem

## Recommendations:

More of your own text here


## Limitations & Next Steps

More of your own text here


### For further information


For any additional questions, please contact **samaheriqat@gmail.com**
