# WEEK 4
*Model Development*
> A model can be though of as a mathematical equation used to predict a value given one or more other values

1. Simple and Multiple Linear Regression
	* Linear regression will refer to one independent variable to make prediction
```
from sklearn.linear_model import LinearRegression
lm = LinearRegression()

# we define the predictor variable and target variable
X = df['highway-mpg']
Y = df['price']

lm.fit(X, Y)

#prediction
Yhat = lm.predict(X)
```
	* Multiple Linear Regression will refer to multiple independent variables to make a prediction 
2. Model Evaluation using Visualization
```
import seaborn as sns

sns.regplot(x="highway-mpg", y="price", data=df)
plt.ylim(0,)
```
3. Polynomial Regression and Pipelines
	* Useful for describing curvilinear relationshiips
```
pr=PolynomialFeatures(degree=2)
pr.fit_transform([1,2], include_bias=False)
```

4. R-squared and MSE for In-Sample Evaluation
	* A way to numerically determine how good the model fits on dataset.
	* Two important measures to determine the fit of a model:
		* Mean Squared Error (MSE)
```
from sklearn.metrics import mean_squared_error
mean_squared_error(df['price'], Y_predict_simple_fit)

316.3435
```
		* R-squared (R^2) or Coefficient of Determination
			* Is a measure to determine how close the data is to the fitted regression line.
```
X = df[['highway-mpg']]
Y = df['price']

lm.fit(X, Y)

lm.score(X,y)
0.496591188
```
6. Prediction and Decision Making
	* Do the predicted values make sense
	* Visualization
	* Numerical measures for evaluation
	* Comparing Models

In this lesson, you have learned how to:
*Define the explanatory variable and the response variable:*Define the response variable (y) as the focus of the experiment and the explanatory variable (x) as a variable used to explain the change of the response variable. Understand the differences between Simple Linear Regression because it concerns the study of only one explanatory variable and Multiple Linear Regression because it concerns the study of two or more explanatory variables.
*Evaluate the model using Visualization:*By visually representing the errors of a variable using scatterplots and interpreting the results of the model.
*Identify alternative regression approaches:*Use a Polynomial Regression when the Linear regression does not capture the curvilinear relationship between variables and how to pick the optimal order to use in a model.
*Interpret the R-square and the Mean Square Error:*Interpret R-square (x 100) as the percentage of the variation in the response variable /y/  that is explained by the variation in explanatory variable(s) /x./The Mean Squared Error tells you how close a regression line is to a set of points. It does this by taking the average distances from the actual points to the predicted points and squaring them.
