# Sales prediction 
## Performing analysis on [Sales Prediction](https://drive.google.com/file/d/1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw/view) dataset and make prediction using machine learning models.
### Author: Kim Hazed Delfino

### Business problem: 
Uncover some potential KPI's (Key Performance Indicator) between store location, type, item-type and other data collected to accurately predict total sale of an item and ultimately improve revenue by providing data-driven-decision and make "what makes this item/store successful" reproducable for future business iteration.

## Methods
 - remove all duplicates to avoid repeating data
 - correct all data inconsistencies (mislabled, unnecessary extra character)
 - Impute missing values to keep data integrity and avoid model prediction errors
 
 ## Exploratory Data Analysis
 - Quick glance of Item MPR Distribution:
 
 ![checking for avg price distribution](https://github.com/KDcodePy/Sales-prediction/blob/master/images/visuals1.png)
 
 
 Here we can see the normal distribution of item Maximum Retail Price (MRP) and get a better understanding of where majority of our item are priced at
 
 
 ---
 
 
 ![](https://github.com/KDcodePy/Sales-prediction/blob/master/images/visuals.png)
 
 This graph represents the average sales per outlet_type and Location_type (Tier).
 In terms of perfomance it looks like `Supermaket Type3` paired with `Location_type Tier3` outperforms other types and tiers
 

---

![](https://github.com/KDcodePy/Sales-prediction/blob/master/images/explanatory.png)

Here we can see that the top3 ave item_type sales belongs to `Starchy Foods`, `Seafood`, and `Fruits and Vagetables` respectively


---


## Models 
- Linear Regression - Simple linear regression is a regression model that estimates the relationship between one independent variable and one dependent variable using a straight line.


- DecisionTree Regressor - A decision tree is a type of supervised machine learning used to categorize or make predictions based on how a previous set of questions were answered. 


Recommendations: 
 - more data means more opportunity to find commonality for analysis and paterns for model predictions, we can't go wrong with adding more data in our dataset
 - gather more relavant data like `monthly sales` to determine wheter a certain item is better suited as `seasonal item` or `staple item` in the store
 
 Limitations & Next Steps:
 - the use of `simple` machine learning model limits our capability to fine-tune our models to better understand patterns in our dataset
  - next Step - Explore different and more complex machine learning models like `RandomForest Regressor `, `Bagging Regressor` , `Elastic_Net`to get a better feel and benchmark different model performance to one another.

---
  
## Model Observation Plots
![](https://github.com/KDcodePy/Sales-prediction/blob/main/image/Largest_Coefficient.png)
The 3 largest coefficients are for
 - "Outlet_Identifier_OUT027" for every item outlet_027 have, their predicted  Item_outlet_sale Increases by $588.235 
 - "Outlet_Type_Supermarket Type3" items sold in Supermarket Type3 increases the Item_outlet_sale average by $588.235 (similar value to OUT027 because OUT027 is the only Supermarket Type3 in the Dataset)
 - "Outlet_Size_Medium" Items sold in Outlet size medium adds Item_Outlet_sale avg by $421.406

![](https://github.com/KDcodePy/Sales-prediction/blob/main/image/top10_most_important_features.png)
What were your 5 most important features?
- The top 5 most important features are:
    - item_MRP - single most important
    - Outlet_Type_Grocery Store - 2nd most important
    - Item_Visibility - somewhat important
    - Item_Weight - somewhat important
    - Outlet_Type_Supermarket Type3 - somewhat important

 ![](https://github.com/KDcodePy/Sales-prediction/blob/main/image/SHAP_feature_importance.png)
 - As we can see above, SHAP's Top-2 importances are similar with built-in random forest importances but the rest are not the same. 
  
![](https://github.com/KDcodePy/Sales-prediction/blob/main/image/SHAPS_dot.png)
- Reading SHAP Top3 Summary Plots
    - "Item_MRP" - Higher(red) item_MRP have positive impact on our model and opposite can be said to lower(blue) feature value item_MRP
    - "Outlet_Type_Grocery Store" - Items that are sold under outlet_type Grocery store have negative impact on our model output which make sense because based on our EDA Grocery store has the smallest distribution relative to other outlet_type
    - "Outlet_Type_Supermarket Type3" - the opposite of Grocery store, Supermarket Type3 holds the top spot of highest avg item_outlet_sales compared to other outlet_type based on our EDA which explain why it has high possitive impact on our model output

![](https://github.com/KDcodePy/Sales-prediction/blob/main/image/Lime_plot_example1.png)
- As we can see in the LIME explanation above, there were many factors contributing to the predicted Item_Outlet_sale, such as:
    - Is the Outlet type - Grocery store (False - positive impact)
    - Item_MRP (low MRP - negative impact)
    - Is the item sold by OUT027 (True - positive impact)

![](https://github.com/KDcodePy/Sales-prediction/blob/main/image/Force_plot_example1.png)
- Here we can see how much each feature affects the model prediction for example Row 39
    -  54.01(min)~7562.66(max)
    - Item_MRP has the most influence driving our prediction to be on the lower-end relative to base value due to having lower Item_MRP value
    - Outlet_Identifier_OUT027 and Outlet_Type_Supermarket Type3 have the 2nd and 3rd most influence with our model prediction respectively, Pushing our model to stay closer to the base value offsetting the negative impact of item_MRP.
 

![](https://github.com/KDcodePy/Sales-prediction/blob/main/image/Lime_plot_example2.png)
- As we can see in the LIME explanation above, there were many factors contributing to the predicted Item_Outlet_sale, such as:
    - Is the Outlet type - Grocery store (True - Negative impact)
    - Item_MRP (low MRP - negative impact)
    - Is the item sold by OUT027 (False - Negative impact)

![](https://github.com/KDcodePy/Sales-prediction/blob/main/image/Force_plot_example2.png)
- Here we can see how much each feature affects the model prediction for example Row 96:
    - 52.98(min)~7575.22(max) / Predicted Value : 157.18
    - Outlet_Type_Grocery Store has the most influence driving our prediction to be on the lower-end relative to base value due to the item being sold at a grocery store and having lower Item_MRP value

---

### For further information
for any additional question, please contact me at my [email](delfino.kim@yahoo.com)
