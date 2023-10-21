# Tree Model
Decision tree is a decision support hierarchical model that uses a tree-like model of decisions and their possible consequences, including chance event outcomes, resource costs, and utility.
Random forests or random decision forests is an ensemble learning method for classification, regression and other tasks that operates by constructing a multitude of decision trees at training time.
This is a model on California housing dataset using decision tree and Random forest. 
Data cleaning 
Only the records where ocean_proximity is either '<1H OCEAN' or 'INLAND', I filled the missing values with zero and Applied the log transformation to median_house_value.
Data validation framework
I did train/validation/test split with 60%/20%/20% distribution and used the train_test_split function and set the random_state parameter to 1, also DictVectorizer(sparse=True) to turn the dataframes into matrices. I trained a decision tree regressor to predict the median_house_value variable, trained  a model with max_depth=1. ocean_proximity feature is used for splitting the data. 
I trained a random forest model with these parameters:n_estimators=10,,random_state=1,
n_jobs=-1 and the RMSE of this model on validationwas 0.244. Then i experiment with the n_estimators parameter Tried different values of this parameter from 10 to 200 with step 10.Set random_state to 1.Evaluate the model on the validation dataset.After which value of n_estimators does RMSE stop improving at 50. I also tried to  select the best max_depth:Try different values of max_depth: [10, 15, 20, 25]
For each of these values, tried different values of n_estimators from 10 till 200 (with step 10)
Fixed the random seed: random_state=1, the best max_depth was 25.
 I also trained an XGBoost model,  I tune the eta parameter:
Installed XGBoost
Created DMatrix for train and validation
Created a watchlist
Trained a model with these parameters for 100 rounds change eta from 0.3 to 0.1.
The eta that leads to the best RMSE score on the validation dataset is 0.1

