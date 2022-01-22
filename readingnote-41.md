# Reading 13 - Linear Regressions

## Linear Regression

**scikit-learn** - contians function for regression, classification, clustering, model selection and dimensionality reduction.

sklearn.model_selection - module that have regressive methods with a target value that is a linear combination of the variables implemented.

  import numpy as np
  import pandas as pd
  import scrip.stats as stats
  import matlib.pyplot as plt
  import sklearn

Can import data set from *sklearn*

  from sklearn.datasets import load_boston
  boston = load_boston()

The object (boston) is a dictionary so use *.keys* method to discover the keys of the *dictionary*.

  boston.keys()

  #OUTPUT
    ['data' , 'feature_names' , 'DESCR' , 'target']

**.feature_names** - display feature names of data set

**.data.shape** - OUTPUT (rows, columns)

to replace titled numbers to the actual feature names:

  bos.columns = boston.feature_names
  bos.head()

### Linear Regression Import

    from sklearn.linear_model import LinearRegression
    lm = LinearRegression() <-- linear regression object

### Linear Regression Model Functions

**lm.fit()** - *fits* a linear model

**lm.predict()** - *predicts* the value using linear model with estimated numerical, constant quantity (coefficients)

**lm.score()** - returns the numerical constant quantity of determination.

**.coef_** - coefficients (R^2); it is the amount of variation in Y can be determined by x with regression model. 

**.intercept** - estimated intercepts

### Fitting a Linear Model

**fit_intercept** - to calculate the intercept or not (returns boolean)

**normalize** - regressors X will be "normal" if fit_intercept is True

  lm.fit(DF, data column)

  import numpy as np
  from sklearn.linear_model import LinearRegression

  lm = LinearRegression()

  Coefficent
  len(lm.coef_)

  Intercept

  lm.intercept_

### Predicting Prices

  lm.predict(x)[0:_] <-- predict numerical value fro the first to desired amount

### Scatter Plot 

**plt.scatter** - scatters the plot. It takes in the (x value, and lm.predict(x))

**plt.xlabel** - labels the x-axis

**plt.ylabel** - labels the y-axis

**plt.title** - labels above the plt with title

**mse** - mean square error
-Determines how clos fitted line is to data points

  mse - np.mean((dp.PRICE_lm.predict(x)) ** 2)
  print mse

  Output: 21.897

*note* single feature is *not* a good predictor of data.

### Training and Validation Data Sets

You have to *split* data sets into *training* and *tests* sets.
-First train the model on data
-Then test it to see performance quality.

### Train-Test Split

**train_test_split** - scikit function

  from skilearn.model_selection import train_test_split
  
  X_train, X_test, Y_train, Y_test = sklearn.cross_validation.train_test_split(X, bos.PRICE, test_size = 0.33, random_state =5)

### Residual Plots

**residual plots** - identify errors in data
-great implementation and displaying data should have scattered data around line zero.

-see structure, data is not correctly getting and displaying something.

## Linear Regression in Python

**regression** - locates variable relationships
-forecast a response using new set

**LinearRegression** - easy interpreting results
-calculates predicted weights

### Multiple Linear Regression

**multiple regression** - linear regression with two or more independent variables

### Polynomial Regression

**polynomial regression** - generalized linear regression

**Underfitting** - model can't capture dependencies amongst data

**Overfitting** - model knows the data too well

  from sklearn.preprocessing import PolynomialFeatures
  transformer = PolynomialFeatures(degrees = 2, include_bias = False)

### Advance Linear Regression 

**statsmodel** - more detailed results

  import statsmodels.api as sm
  sm.add_constant(x)

**ordinary least squares** - sm.OLS(y,x)

[<==BACK](README.md)
