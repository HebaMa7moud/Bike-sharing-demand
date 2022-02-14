# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE
Heba Abdelhai
## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
TODO: Add your explanation

I realize that I need to check predictions for negative values.
The changes that were needed is to set negative values to zero.

### What was the top ranked model that performed?
TODO: Add your explanation

WeightedEnsemble model has the top score value.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: Add your explanation

The models scores increased after adding additional features compared to the scores before which mean increasing the effectivness of the models.
 
Added features are:
1-change data types from 'int64' to 'category' for both features columns "season" and "weather".
2-Parsing date column to datetime type and parse the date column to parsed "year", "month", "day" and "hour".


### How much better did your model preform after adding additional features and why do you think that is?
TODO: Add your explanation

The model score after adding additional features increased to be -35.107319 compared to the model score before adding additional features which equals -116.187513 so the model performance has improved.



## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: Add your explanation

The model score increased to be -34.278285 after changing the individual model hyperprameters compared to the model score before which equals to -35.107319. This means that changing hyper parameters is doing so well to increase model performance.

 
### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation

I would excute more hyperparameters tuning for the models to optimize them.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|None|None|None|1.38918|
|add_features|None|None|None|0.47469|
|hpo|{'GBM':{'num_iterations':300, 'learning_rate':0.15}}|{'XGB':{'objective':'reg:squarederror', 'max_depth':8, 'eta':0.37}}|{'CAT':{'depth':10,'learning_rate':0.11}}|0.52957|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.


![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.
https://github.com/HebaMa7moud/Bike-sharing-demand/blob/main/model_test_score.png
![model_test_score.png](img/model_test_score.png)

## Summary
TODO: Add your explanation

Training the models without features engineering decrease the effectiveness of the models this can be seen by comparing the models scores before and after applying features engineering. So parsing date values and changing the types of two features of the datasets increase the models scores. Another way to increase the models perfomance is hyperparameters tuning as well as changing hyperparameters values for few models of the top performers models. Taking the scores of three models, scores after feature engineering applied with default parameters, as a baseline and changing the individual model hyperprameters many times with different values to find the right combination of parametters to increase the models performance. 
