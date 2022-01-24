
# WEEK 5
*Model Evaluation*
* Tell us how model perform in the real world
* Training / Testing Sets
```
from sklearn.model_selection import train_test_split

x_train, x_test, y_train, y_test = train_test_split(x_data, y_data, test_size=0.3, random_state=0)
```
* Out of sample error
* Cross validation score
```
from sklearn.model_selection import cross_val_score

scores=cross_val_score(lr, x_data, y_data, cv=3)

np.mean(scores)
```
* Overfitting: When the model is too flexible and fit the noise rather then the function.
* Under-fitting: Model is too simple to fit the data
* Model Selection
* Ridge Regression: Is a regression that is employed in a multiple regression model when multicollinearity occurs.
```
from sklearnn.linear_model import Ridge
RidgeModel=Ridge(alpha=0.1)
RidgeModel.fit(X,y)
Yhat=RidgeModel.predict(X)
```
* Grid Search
In this lesson, you have learned how to:
*Identify over-fitting and under-fitting in a predictive model:*Overfitting occurs when a function is too closely fit to the training data points and captures the noise of the data. Underfitting refers to a model that can’t model the training data or capture the trend of the data.
*Apply Ridge Regression to linear regression models:*Ridge regression is a regression that is employed in a Multiple regression model when Multicollinearity occurs.
*Tune hyper-parameters of an estimator using Grid search:*Grid search is a time-efficient tuning technique that exhaustively computes the optimum values of hyperparameters performed on specific parameter values of estimators.
