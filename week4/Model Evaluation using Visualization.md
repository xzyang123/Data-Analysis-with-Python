# Regression plot

```python
import seaborn as sns
sns.regplot(x = 'highway-mpg', y = 'price', data = df)
plt.ylim(0,)
```
![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week4/images/regression.png?raw=true)

# Residual plot

how do we know if the linear model is correct?

the residual plot will tell you if the model fits the accurate values

1. Here is how we get the residual plot. We get the substraction of predicted and actrual Y value, then put them in a new plot.

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week4/images/residual%20plot.png?raw=true)

2. Here is the plot of the spread of the residuals.

	* The points randomly spread out around x-axis means the **linear model is GOOD**
	
![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week4/images/spread%20plot.png?raw=true)

3. Here is how to get the residual plot in Python

```python
import seaborn as sns
sns.residplot(df['highway-mpg'], df['price'])
```
# Distribution Plots

Here is the code to create the distribution plot

```python
import seaborn as sns
ax1 = sns.distplot(df['price'], hist = False, color = 'r', label = 'Actual Value')
sns.distplot(Yhat, hist = False, color = 'b', label = 'Fitted Values', ax = ax1)
```




















































































