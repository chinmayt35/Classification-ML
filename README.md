# Classification-ML
Supervied Machine Learning Classification algorithms to predict whether a grocery store customer will Purchase Citrus Hill (CH) or Minute Maid (MM) orange juice.

## Dataset
The dataset contained the following list of features:

 No. | Feature | Non-null | Dtype
------------ | ------------- | ------------- | -------------
1 |  Purchase     |   1070 non-null |  object 
2 | WeekofPurchase|  1070 non-null | int64   
 3  | StoreID      |   1070 non-null  | int64  
 4  | PriceCH     |    1070 non-null |  float64
 5 |  PriceMM     |    1070 non-null |  float64
 6 |  DiscCH     |     1070 non-null|   float64
 7  | DiscMM  |        1070 non-null |  float64
 8 |  SpecialCH   |    1070 non-null |  int64  
 9  | SpecialMM    |   1070 non-null |  int64  
 10 | LoyalCH       |  1070 non-null |  float64
 11 | SalePriceMM   |  1070 non-null |  float64
 12 | SalePriceCH   |  1070 non-null |  float64
 13 | PriceDiff  |     1070 non-null  | float64
 14 | Store7      |    1070 non-null |  object 
 15  |PctDiscMM   |    1070 non-null|   float64
 16 | PctDiscCH     |  1070 non-null  | float64
 17 | ListPriceDiff  | 1070 non-null |  float64
 18  |STORE        |   1070 non-null  | int64  
 

 ## Model Training and Results
* The target column - Purchase, was converted to binary for classification with 1 indicating purchase of CH juice and 0 indicating purchase of MM juice.
* Highly correlated columns were dropped and certain columns which did not add value as numbers were converted to categorical features.
* After a random 80:20 split for generating train and test datasets, Random Forest, Gradient Bossting and Support Vector Classifier algorithms were built with 5 fold cross validation to predict the target column
 
 ## Evaluation Metrics and Results
 The metric chosen to evaluate the models built is AUC. As we want to be able to evaluate the model’s overall performance under different thresholds and be able to differentiate between the two classes, AUC is an appropriate metric to evaluate the model’s performance.
  
 Algorithm | AUC | Macro Average F1 Score
 ------------- | ------------- | -------------
 Random Forest | 86.8% | 80%
 Gradient Boosting | 87.5% | 78%
 SVC | 88.6% | 82%
 
