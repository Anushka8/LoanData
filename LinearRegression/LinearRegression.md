# Linear Regression
Linear regression shows how much one variable affects another and how to predict, estimate, or explain its behavior
Difference between correlation and Linear Regression to get a better understanding:

![image](https://github.com/Anushka8/LoanData/assets/26516821/d4846edf-d64b-4cae-a21a-14eb102bd780)

* If swapping X and Y does not change the outcome, use correlation analysis. If changing X and Y affects the output, perform Linear Regression
* If analysis aims to answer if there is a relationship between X and Y, use correlation. If the aim is to answer how X affects Y or have X predict Y, use regression.

## Data Normalization and Cleaning
* Load CSV data into a data frame using Python Pandas Library
* Get an overview of the data:
  * .head() displays the first few rows with column headings
  * .describe() gives statistical data overview
  * .info() displays the number of non-null rows and their data types
* Perform data normalization and data cleaning:
  * Fields (Interest.Rate, Loan.Length, Debt.To.Income.Ratio, FICO.Range) with datatype 'object' is changed to either string, int, or float values depending on the usage
  * Unwanted symbols like '%' or text like 'month' are removed from the row values
  * Rows with null values and duplicate values are dropped
 
## Determining the relationship between variables
* Plot Interest.Rate vs FICO.Score graph purely (since, in the real world, interest rates depend on FICO Score).
* As observed from the graph, there is no strong relation between the two variables.
* Plot scatter matrix to determine which variable to consider for the model
* There is a relationship between FICO.Score and Loan.Amount as per the scatter matrix.

## Performing Multivariate Linear Regression
* Get the independent and dependent variables
* Split data into training and testing data. In this case, the testing data is 20% of the total data
* Fit training data into the model and predict the outcome of the dependent variable

## Evaluate the performance of the model
* Perform Mean Square Error (average squared difference between the actual value and the predicted values). In this case, the error is 6.35
* Calculate R-squared (represents the proportion of the variance in the dependent variable that is predictable from the independent variables)
* R² value is approximately 0.627. This means that about 62.7% of the variability in the interest rate can be explained by the FICO score and loan amount.
* This indicates a moderately strong relationship between the variables
