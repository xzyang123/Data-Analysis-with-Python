# Simple Linear Regression

We need a model to describ the points from the plot

The model is used to predict the actual value

But, the model is not already right, we need to fit the model with the actual value

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week4/images/simple%20linear%20regression.png)

# Fitting a simple linear model estimator

* X: predictor variable

* Y: Target variable

    1. Import linear_model from scikit-learn
    
    ```python
    from sklearn.linear_model import LinearRegression
    ```
    
    2. Create a Linear Regression Object using the constructor
    
    ```python
    lm = LinearRegeression()
    ```
* Define the predictor and target variables

	```python
	X = df[['highway-mpg]]
	Y = df['price']
	```

* use lm.fit(X, Y) to fit the model, fine the b0 and b1

	```python
	lm.fit(X, Y)
	```

* Then, we can obtain a prediction
	
	```python
	Yhat = lm.predict(x)
	```
	
![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week4/images/yhat.png?raw=true)

* (b0): lm.intercept_

	38423

* (b1): lm.coef_

	-821.733

* The relationship between *Price* and *Highway-MPG* is:

	Price = 38423 - 821.73 * highway-mpg
	
# Multiple Linear Regression

Y = b0 + b1X1 + b2X2 + b3X3 + b4X4

* b0: intercept (X = 0)

* b1: the coefficient or parameter of X1 and so on..

# Fitting a multiple linear model estimator

1. Extract for 4 predictor variables and store them in the variable Z

	```python
	Z = df[['horsepower', 'curb-weight', 'engine-size', 'highway-mpg']]
	```
2. Train the model as before

	```python
	lm.fit(Z, df['price'])
	
3. we can also obtain a prediction

	```python
	Yhat = lm.predict(x)
	```

4. find the intercept(b0)

	```lm.intercept_```
	
5. find the coefficients(b1, b2, b3, b4)

	```lm.coef_```

    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
