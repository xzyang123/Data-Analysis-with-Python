# Correlation

**when one variable changes, how does this affect change in other variable?**

## Correlation - example

Let's see how does the engine-size affect the price

```sns.regplot(x = 'engine-size', y = 'price', data = df)```

```plt.ylim(0,)```

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week3/images/correlation.png?raw=true)

From the plot, we can see the correlation between the engine-size and the price is *pisitive linear relationship*.

# Correlation statistics

## Pearson correlation

* Measure the strength of the correlation between two variables
  
  * Correlation coefficient
  
  * P-value
  
* Correlation coefficient
  
  * Close to +1: Large positive relationship
  
  * Close to -1: Large negative relationship
  
  * Close to 0: No relationship
  
* P-value

  * P-value < 0.001 Strong certainty in the reslut
  
  * P-value < 0.05 Moderate certainty in the reslut
  
  * P-value < 0.1 Weak certainty in the reslut
  
  * P-value > 0.1 No certainty in the reslut
  
* **Strong Correlation**

  * Correlation coefficient close to 1 or -1
  
  * P value less than 0.001
