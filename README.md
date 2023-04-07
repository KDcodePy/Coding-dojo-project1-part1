# Sales prediction 
## Performing analysis on [Sales Prediction](https://drive.google.com/file/d/1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw/view) dataset and make prediction using machine learning models.
### Author: Kim Hazed Delfino

### Business problem: 
Uncover some potential KPI's (Key Performance Indicator) between store location, type, item-type and other data collected to accurately predict total sale of an item and ultimately improve revenue by providing data-driven-decision and make "what makes this item/store successful" repeatable for future business iteration.

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
 
