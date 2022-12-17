# Explainable-AI-w.-DALEX---SHAP
# Explaining Predictions from XGBoosting Model on Boston Housing
## < Nicole An > 
## Overview of the Model Performance

The XGBoosting model is hyper tuned using 5-fd CV with hyperparameters trees=82; min_n=9; tree_depth=6. The table below shows the metrics that are used to evaluate this  model. XGBoost has the lowest RMSE from previous challenge, which indicates that it has the overall lowest difference between the predicted home values and the actual home values. Therefore, this model is the best fit of the data. It also has the highest RSQ, meaning that about 86.8% of the variation in home values can be explained by the XGBoost model. This is very high in terms of prediction power. Also, it has the lowest MAE as well. That is, the average error that predictions from this model make is only $37,854.08. It is about 8.2% of the average home values, a small percentage of what we are predicting. 

.estimator
<chr>	part
<chr>	rmse
<dbl>	rsq
<dbl>	mae
<dbl>
standard	training	33362.85	0.9495060	25282.56
standard	testing	53126.65	0.8680715	37854.05

## Global Interpretation

### Top 20 Most Important Variables using VIP
 
### Partial Dependance Plots on Top 5 Most Important Variables 
     

The PDPs show how each important variable impacts the prediction on average. As household median income increases, the predicted house value increase as well. Inversely, as the population density decrease, the predicted house value tends to increase. Population of the area drives up the predicted house values as well, with an exception in the middle, which is the population of Jamaica Plain. It is an outlier in the relationship between population and the response variable we are predicting, house value. It can be a phenomenon because Jamaica Plain has a very high median income and since median income has a strong positive relationship with house value. In addition, both higher living area and higher land size increases the home value. That is, when the government predicts house values, measurement of the house and area are important factors the government should take into consideration. 


## Local Interpretation

### Top 10 Best Most Accurate Predictions

 

          
These are the most accurate predictions made by the model, meaning the important variables from each profile make large impact on the predictions. Below are some shared characteristics of the best predictions:
•	These are homes built in the 19th and 20th centuries and with less remodeling. 
•	These are homes that are typical. The external conditions, overall conditions, internal conditions, and views for these homes are all in average category. 
•	The home ages generally revolve around the mean home age, 64.06.
The best prediction is only $53.6 above the actual home value. At the predicted price of $552253.56, the variable population impacts on the prediction for $33797.64, which explains 6% impact of the predicted price. Also, the population density makes a negative impact on the prediction with -$8369. That is, population density explains 2% of the predicted price. 

### Top 10 Worst Under Estimated Predictions
 
          
These are the top 10 worst under estimations, meaning that the important variables in each profile tend to drive the predictions too low. Below are some shared characteristics of the houses:

•	80% of the under estimations are occupied by owners, which is lower than the average percentage of owner-occupied rate (88.2%).
•	All of these homes are from Jamaica Plain, MA, a city with high median income and a relatively low population density. 
•	Most homes tend to have 3 or more bedrooms.
Median income is an very important positive influencer to the prediction, and it contribute a lot in driving the predictions up. However, home age and living area decrease the predicted home value by a large amount. Older house tend to depreciate in values regardless of the area and size of the house. Also, homes with more bedrooms tend to have more living spaces. 

### Top 10 Worst Overestimated Predictions

 
          
 
These are the top 10 over estimations, meaning that the important variables in each profile tend to drive the predictions too high. Below are some shared characteristics of the houses:
•	80% of the homes have very large living areas, significantly higher than the mean living area (mean = 1659 sqft).
•	Most homes (90%) have colonial building style (mean = 60%).
These homes tend to have living area as an important positive influencer of the predictions. From the worst over estimated house, we can see that living area and median income are the top 2 factors that inflate the predictions while home age in the top negative influencer. This outlier house is a luxurious large house which is very old, and the prediction did not take into consideration of its depreciation through time. 
