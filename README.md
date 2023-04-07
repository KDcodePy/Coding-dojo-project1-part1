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

### For further information
for any additional question, please contact me at my [email](delfino.kim@yahoo.com)
