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
