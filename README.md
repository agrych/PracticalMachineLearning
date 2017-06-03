# Introduction
Advances in technology have made it possible to collect data about a person's activity using devices such Jawbone Up, Nike FuelBand, and Fitbit.  Individuals wearing this type of device record various types of measurements relating to physical activity.  This information can then be used to assist in improving one's health. However, while the measurements quantify how much of the physical activity was completed, the device does not quantify how well the individual did. Therefore, the goal of this project is to use the data from accelerometers on the belt, forearm, arm, and dumbell of 6 participants to predict the manner in which they did the exercise. 
More information is available from the website here: http://groupware.les.inf.puc-rio.br/har (see the section on the Weight Lifting Exercise Dataset)."

## Cross Validation
We learn that it is not advisable to compare the predictive accuracy of the model using the same dataset used for estimating the model.  Therefore, in order to assess the model's predictive performance, an independent set of data, the test dataset, will be used.
Since this dataset appears to be medium-sized, the original dataset pml-training.csv dataset will be randomly sliced into two parts: a training set (60%) and a test set (40%).  The training set will be used to fit the models.  The test set will be used for assessment of the generalization (out-of-sample) error of the final chosen model. The final prediction model will be used to predict 20 different test cases.

## Data Cleaning
It is assumed that the observations with missing values are missing completely at random; therefore, columns with a large amount of missing values are discarded.  In addition, variables that have very little variability in them will be removed since they are not useful predictors.

## Prediction Model Consideration
According to Hastie, Tibshirani, and Friedman (2009), "random forests do remarkably well, with very little tuning required" (p. 590).  This project compares the two most widely used and accurate prediction models Random Forest and Boosting. 

## Prediction Model Selection
### The comparison of the Random Forest and Generalized Boosting models revealed that the Random Forest model was more accurate than the Generalized Boosting model. 
Prediction using the Random Forest model will be used for Validation (the project quiz).

## Prediction Quiz using Random Forest
Prediction on Quiz dataset resulted in 100% Accuracy.

### References
Hastie, T., Tibshirani, R., & Friedman, J. H. (2009). The elements of statistical learning data mining, inference, and prediction (2nd ed.). New York, NY: Springer.
