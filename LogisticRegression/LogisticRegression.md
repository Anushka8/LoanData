# Logistic Regression
Predict binary outcome (if a loan will be provided T/F) depending on the independent variable interest rate 

## Data Cleaning and Normalization
* Same as before

## Defining a new variable
* Define a new variable to display the binary output. (True/False)
* Output is determined by the Interest Rate
* If the interest rate is <= 12, the loan will be provided (output True)

## Using Logistic Regression for prediction
* Implementation steps similar to Linear Regression
 
## Evaluating the performance of the model
* Accuracy (ratio of correctly predicted instances to the total instances) is 62.6%
* Confusion Matrix shows the counts of TP, TN, FP and FN
  
___ | Predicted False | Predicted True
| :--- | ---: | :---:
Actual False  | 226 | 74
Actual True  | 113 | 87

* TN: 226, TP: 87, FN: 113, FP: 74
* Precision = TP / (TP + FP): Of all the instances predicted False, 67% were False and of all the instances predicted True, 54% were True
* Recall (Sensitivity = TP / (TP + FN)): The model identified 75% of the actual False and 43% of actual True instances.
* F1-Score is the weighted average of Precision and Recall = 2 * (Precision * Recall) / (Precision + Recall)
* Support: Number of actual occurrences of the class in the specified dataset
